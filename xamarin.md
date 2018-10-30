# Gomb eseménykezelő
```csharp
  goButton.Click += (sender, e) =>
  {
      //Toast.MakeText(this, string.Format($"Hello {inputText.Text}!"), ToastLength.Short).Show();
      string[] splitted = inputText.Text?.Split(new[] { ' ' }, StringSplitOptions.RemoveEmptyEntries);
      if (splitted == null || splitted.Length < 3 || !double.TryParse(splitted[0], out double amount))
      {
          Toast.MakeText(this, "Invalid input!", ToastLength.Short).Show();
          return;
      }

      string searchCurrency;
      bool invert = false;
      if (splitted[1].Equals("EUR", StringComparison.InvariantCultureIgnoreCase))
      {
          searchCurrency = splitted[2];
      }
      else if (splitted[2].Equals("EUR", StringComparison.InvariantCultureIgnoreCase))
      {
          searchCurrency = splitted[1];
          invert = true;
      }
      else
      {
          Toast.MakeText(this, "Invalid input!", ToastLength.Short).Show();
          return;
      }
      Stream rateXMLStream = Assets.Open("eurofxref-daily.xml");
      XDocument ratesXML = XDocument.Load(rateXMLStream);

      var rateString = ratesXML.Descendants(nsa + "Cube")
                              .FirstOrDefault(xe => string.Equals(((string)xe.Attribute("currency"))
                                                  , searchCurrency
                                                  , StringComparison.InvariantCultureIgnoreCase))
                              ?.Attribute("rate");
      if (rateString == null || !double.TryParse((string)rateString, out double rate))
      {
          Toast.MakeText(this, "Invalid input!", ToastLength.Short).Show();
          return;
      }
      if (invert)
          rate = 1 / rate;
      Toast.MakeText(this, string.Format($"{amount} {splitted[1]} = {rate * amount:F3} {splitted[2]}")
          , ToastLength.Long).Show();
  };

```

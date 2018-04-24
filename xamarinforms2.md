## DetailsPage v1

```xaml
  <TabbedPage xmlns="http://xamarin.com/schemas/2014/forms"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             x:Class="CookBookXamarin.Views.DetailsPage"
              xmlns:l="clr-namespace:AiForms.Layouts;assembly=AiForms.Layouts"
             Title="{Binding Recipe.Title}">
  <ContentPage Title="Images">
      <l:RepeatableWrapLayout	ItemsSource="{Binding Recipe.ExtraImages}">
          <l:RepeatableWrapLayout.ItemTemplate>
              <DataTemplate>
                  <Grid HorizontalOptions="Start">
                      <Grid.WidthRequest>
                          <OnPlatform x:TypeArguments="x:Double">
                              <On Platform="UWP" Value="250" />
                              <On Platform="Android" Value="125" />
                          </OnPlatform>
                      </Grid.WidthRequest>
                      <Grid.HeightRequest>
                          <OnPlatform x:TypeArguments="x:Double">
                              <On Platform="UWP" Value="250" />
                              <On Platform="Android" Value="125" />
                          </OnPlatform>
                      </Grid.HeightRequest>
                      <Image Source="{Binding}" Aspect="AspectFill"/>
                  </Grid>
              </DataTemplate>
          </l:RepeatableWrapLayout.ItemTemplate>
      </l:RepeatableWrapLayout>
  </ContentPage>
  <ContentPage Title="Ingredients">
      <ListView ItemsSource="{Binding Recipe.Ingredients}">
          <ListView.ItemTemplate>
              <DataTemplate>
                  <TextCell Text="{Binding}" />
              </DataTemplate>
          </ListView.ItemTemplate>
      </ListView>
  </ContentPage>
  <ContentPage Title="Directions">
      <Label Text="{Binding Recipe.Directions}" />   
  </ContentPage>
</TabbedPage>
```

## Comment fül

```xaml
<ContentPage Title="Comments">
            <ListView ItemsSource="{Binding Recipe.Comments}" 
                      HasUnevenRows="True" 
                      Header="{Binding}">
                <ListView.Header>
                    <StackLayout>
                        <Entry Placeholder="Email" 
                               Keyboard="Email" 
                               Text="{Binding EmailAddress, Mode=TwoWay}"/>
                        <Editor Text="{Binding NewComment, Mode=TwoWay}" 
                                VerticalOptions="FillAndExpand" 
                                HeightRequest="80"/>
                        <Button Text="Send" 
                                Command="{Binding SendCommentCommand}" />
                    </StackLayout>
                </ListView.Header>
                <ListView.ItemTemplate>
                    <DataTemplate>
                        <ViewCell>
                            <StackLayout Margin="0,10">
                                <Label Text="{Binding Name}" 
                                       Style="{DynamicResource ListItemTextStyle}"/>
                                <Label Text="{Binding Text}" 
                                       Style="{DynamicResource BodyStyle}"/>
                            </StackLayout>
                        </ViewCell>
                    </DataTemplate>
                </ListView.ItemTemplate>
            </ListView>
        </ContentPage>
```


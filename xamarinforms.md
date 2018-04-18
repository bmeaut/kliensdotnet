# RecipeHeader
```
public class RecipeHeader
{
    public int Id { get; set; }
    public string Title { get; set; }
    public string BackgroundImage { get; set; }
    public string TileImage { get; set; }
}
```

# RecipeGroup
```
public class RecipeGroup
{
    public string Id { get; set; }
    public string Title { get; set; }
    public List<RecipeHeader> Recipes { get; set; }
}
```
# ICookbookApiService
```
public interface ICookbookApiService
{
     [Get("/api/Recipes/Groups")]
     Task<List<RecipeGroup>> GetRecipeGroupsAsnyc();
}
```
# Korábbi UWP-s labor RecipeHeader GridView-s data template-je
```
<DataTemplate>
     <Grid Width="250" Height="250">
         <Image Source="{Binding BackgroundImage}"
                Stretch="UniformToFill" 
                VerticalAlignment="Center" />
         <Border VerticalAlignment="Bottom" Background="#AA000000">
             <TextBlock Text="{Binding Title}" Margin="12" Foreground="White"/>
         </Border>
     </Grid>
 </DataTemplate>
```
# Xamarin Forms-os ListView-s RecipeHeader DataTemplate
```
 <ViewCell>
     <Grid WidthRequest="250" HeightRequest="250" HorizontalOptions="Start">
         <Image Source="{Binding BackgroundImage}" Aspect="AspectFill"/>
         <Frame BackgroundColor="#AA000000" VerticalOptions="End">
             <Label Text="{Binding Title}" Margin="12" TextColor="White"/>
         </Frame>
     </Grid>
 </ViewCell>
```




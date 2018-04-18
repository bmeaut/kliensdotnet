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




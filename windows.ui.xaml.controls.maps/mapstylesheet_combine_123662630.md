---
-api-id: M:Windows.UI.Xaml.Controls.Maps.MapStyleSheet.Combine(Windows.Foundation.Collections.IIterable{Windows.UI.Xaml.Controls.Maps.MapStyleSheet})
-api-type: winrt method
---

<!-- Method syntax.
public MapStyleSheet MapStyleSheet.Combine(IIterable<MapStyleSheet> styleSheets)
-->

# Windows.UI.Xaml.Controls.Maps.MapStyleSheet.Combine

## -description
Combines the rules defined in two custom [MapStyleSheet](mapstylesheet.md) instances.

## -params

## -param styleSheets
The custom [MapStyleSheet](mapstylesheet.md) instances that you want to combine.

## -returns
A [MapStyleSheet](mapstylesheet.md) instance that contains the combined rules defined in each [MapStyleSheet](mapstylesheet.md) instance that you passed to the *styleSheets* parameter.

## -remarks

## -see-also

## -examples
The following example combines rules from two [MapStyleSheet](mapstylesheet.md) instances into one [MapStyleSheet](mapstylesheet.md) instance.

```csharp
string jsonString = @"{
""settings"": {
 ""rasterRegionsVisible"":true,
 ""spaceColor"":""#000000""
    },
""elements"":
    {
     ""majorRoad"": {
         ""labelColor"":""#490B7D"",
      ""labelScale"":1.5,
      ""font"": ""Comic Sans MS""
                   }
 }
}";

 string jsonString2 = @"{
""settings"": {
     ""landColor"":""#FFC8DD""
    },
""elements"":
    {
 }
}";

MapStyleSheet myCustomStyleSheet = MapStyleSheet.ParseFromJson(jsonString);
MapStyleSheet myCustomStyleSheet2 = MapStyleSheet.ParseFromJson(jsonString2);

List<MapStyleSheet> myList = new List<MapStyleSheet>();
myList.Add(myCustomStyleSheet);
myList.Add(myCustomStyleSheet2);

myMap.StyleSheet = MapStyleSheet.Combine(myList);

```

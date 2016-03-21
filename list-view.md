# ListView

## Official Docs
- [API](https://docs.nativescript.org/ApiReference/ui/list-view/ListView)
- [How To](http://docs.nativescript.org/ApiReference/ui/list-view/HOW-TO)
- [Source](https://github.com/NativeScript/NativeScript/tree/master/ui/list-view)

## XML
```xml
<Page>
 <ListView items="{{ myItems }}">
    <ListView.itemTemplate>
       <Label text="{{ title || 'Downloading...' }}" textWrap="true" class="title" />
    </ListView.itemTemplate>
 </ListView>
</Page>
```

## Cookbook

### Why isn't the listview fullscreen?
The listview doesn't know how big to make itself, its container needs to have a set size
#### Only item in the page
``` xml
<Page>
 <ListView items="{{ myItems }}">
    <ListView.itemTemplate>
       <Label text="{{ title || 'Downloading...' }}" textWrap="true" class="title" />
    </ListView.itemTemplate>
 </ListView>
</Page>
```
#### Part of a grid
``` xml
<Page>
    <GridLayout rows="auto, *">
        <!-- AutoSized Row -->
        <SearchBar row="0" hint="{{ searchHint }}" /> 
        <!-- Fill Row, so listview fills the rest of the screen-->
        <ListView row="1" items="{{ myItems }}"> 
            <ListView.itemTemplate>
            <Label text="{{ title || 'Downloading...' }}" textWrap="true" class="title" />
            </ListView.itemTemplate>
        </ListView>
    </GridLayout>
</Page>
```

### Remove Separator Line ###
Set it to the same color as the background
``` xml
<ListView items="{{ listItems }}" separatorColor="#FFF">
```

### Remove the listview selection color on click ###
``` xml
<ListView itemLoading="onListViewLoadingFixSelectState">
```
``` js
exports.onListViewLoadingFixSelectState = function (args) {
    if (frame.topmost().ios) {
        var cell = args.ios;
        cell.selectionStyle = UITableViewCellSelectionStyle.UITableViewCellSelectionStyleNone;
    }
}
```
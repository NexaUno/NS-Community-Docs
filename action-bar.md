# Action Bar

## Official Docs
- [API](https://docs.nativescript.org/ApiReference/ui/action-bar/ActionBar)
- [How To](https://docs.nativescript.org/ApiReference/ui/action-bar/HOW-TO)
- [Source](https://github.com/NativeScript/NativeScript/tree/master/ui/action-bar)

## XML
```xml
<Page>
	<Page.actionBar>
		<ActionBar title="{{ title }}" android.icon="res://is_custom_home_icon"/>
	</Page.actionBar>
	...
</Page>
```

## Cookbook

### How do I hide the the Action Bar from a specific page?
```xml
<Page actionBarHidden="true">
	...
</Page>	
```

### How do I make the statusbar the same color?
``` js
    if (app.ios) {
        var navigationBar = frame.topmost().ios.controller.navigationBar;;
        navigationBar.barStyle = 1;
        navigationBar.tintColor = UIColor.whiteColor();
        
        //Optional, stops the AB from being transparent
        navigationBar.translucent = false;
    }
```

### How do I change the color of the Action Items?
```xml
<ActionBar>
    <ActionBar.actionItems> 
        <ios>
            <ActionItem text="CANCEL" ios.position="left" tap="cancelEvent" />
        </ios>
        <ActionItem ios:text="DONE" android:text="SAVE" android.color="white" ios.position="right" tap="saveDate" style="color: white" />
    </ActionBar.actionItems>
</ActionBar>
```
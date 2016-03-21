# Action Bar

## Official Docs
- [API](https://docs.nativescript.org/ApiReference/ui/action-bar/ActionBar)
- [How To](https://docs.nativescript.org/ApiReference/ui/action-bar/HOW-TO)

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
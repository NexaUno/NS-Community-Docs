# Change CSS Style Dynamically
```javascript
var application = require(“application”);

...

application.cssSelectorsCache = application.loadCss(“./app-dark.css”);
application.cssFile = (“./app-dark.css”);
this.reload();
```

**WARNING:** Calling this.reload() will reset the app's navigation stack;

Contribution found at [https://medium.com/the-rank-amateur/theme-switching-in-nativescript-a26c6aff7ac5#.7u10zs726](https://medium.com/the-rank-amateur/theme-switching-in-nativescript-a26c6aff7ac5#.7u10zs726)
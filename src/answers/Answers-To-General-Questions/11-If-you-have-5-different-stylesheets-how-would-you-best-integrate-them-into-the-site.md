# If you have 5 different stylesheets, how would you best integrate them into the site ?

I would refactor them as the following files
 - `vendors` - 3rd-party libraries
 - `base` - basic style settings
 - `mixins` - for sass mixin
 - `variables` -  for sass variables
 - `components` - if using a frontend framework, this might goes to separated component folder
 
 And use webpack to pack them into one file and put it to `<head></head>`.
 CSS files are only served as they're needed, other files that will likely to be used may be served by `prefetch` technique.

# Backbone Adapter for local persistency 


This is a fork of mikeedwards Backbone.domStorage module which is based on jeromegn's excellent Backbone.localStorage module.

## Usage

Include Backbone.localPersist after having included Backbone.js:

```html
<script type="text/javascript" src="backbone.js"></script>
<script type="text/javascript" src="backbone.localPersist.js"></script>
```

Create your collections:

```javascript
var SomeCollection = Backbone.Collection.extend({
  
  localPersist: new Backbone.localPersist("SomeLocalCollection"), // Unique name within your app.
  // or 
  localPersist: new Backbone.localPersist("SomeLocalCollection", true), // the second parameter is used to change from local storage to session storage
  // ... everything else is normal.
  
});
//you can disable the Adapter by setting following flag. 
SomeCollection.disableLocalPersist = true;
```

*or*

```javascript
window.SomeCollection = Backbone.Collection.extend({
  
  localPersist: new Backbone.localPersist("SomeLocalCollection"), // Unique name within your app.
  //or
  localPersist: new Backbone.localPersist("SomeLocalCollection", true), // the second parameter is used to change from local storage to session storage
  // ... everything else is normal.
  
});
//you can disable the Adapter by setting following flag. 
SomeCollection.disableLocalPersist = true;
```

## Todo
* optional fetch from local storage


## Credits
Thanks to [mikeedwards](https://github.com/mikeedwards) for the domStorage module
Thanks to [Jerome Gravel-Niquet](https://github.com/jeromegn) for the localStorage module 

## License

Licensed under MIT license

Copyright (c) 2010 Jerome Gravel-Niquet

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
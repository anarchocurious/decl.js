**This is the classic version of Decl. The new version can be found [here](https://github.com/anarchocurious/decl).**


# decl.js
Decl is a simple library designed to enable more declarative and unobtrusive JavaScript.

## Usage

```javascript
// Automatically adds select2 to all <select data-uses-select2 />
Decl({
  matcher: 'select[data-uses-select2]',
  matches: function(node) {
    $(node).select2();
  },
  unmatches: function(node) {
    var select2 = $(node).data('select2');
    
    if(select2) {
      select2.destroy();
    }
  }
});
```

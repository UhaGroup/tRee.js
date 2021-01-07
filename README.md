# tRee.js
Treeview library

## Usage
Note that almost all options are default.

## css
your default font and other affected the tRee elements.

like :
```css
    button {
      background-color: #E6E8F3;
    }
    
    * {
         font-family: tahoma; 
         font-weight: 500; 
         font-size: 12px;   
      }
    
```


## Installation Instructions
```html
  <script type="text/javascript" src="tRee-min.js"></script>
```

## Quick Start

```js

// empty tree
let tree_obj;
let treeView = new tRee();
treeView.show( (id,path,change) => {
 // id : string
 // path : string
 // change : bool
 
 // for update tree
 if(change) {
  tree_obj = treeView.tree();
 }
 
});
```

## on change listener
```js
treeView.onChange( tree => {
  tree_obj = tree;
})
```

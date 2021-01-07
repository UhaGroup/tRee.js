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
## options

```js
// empty tree
let tree_obj;
let treeView = new tRee();
let options = treeView.options();
   
   log : {
            id : 'tRee-container', // id of root element
            titleText : "choose target folder...", // title of dialog
            className : "tRee", // css class name
            doneText : 'done',
            newFolderText : "new folder",
            cancelText : "cancel",
            error1 : "first choose target folder!",
            error2 : "you can't create this folder!",
            error3 : "this folder not exist!",
            error4 : 'id not found!',
            prompTitle : "enter name folder ...",
            prompRenameTitle : "new name ...",
            libNameHide : false, // if you want hide title (tRee.js) = true | show = false  
        }
        
  // for change
  
  options.titleText = 'some thing else...';
  options.doneText : 'add';
  options.newFolderText : "new branch";
  treeView.options(options);
```

## Everything in tRee.js
```js
treeView.onChange( tree => {
  tree_obj = tree;
})
```

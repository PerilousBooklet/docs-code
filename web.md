# Web

## HTML/CSS

### Centering divs

```html
<!DOCTYPE html>
<html>
  
  <head>
    <title>Ex1: Centering</title>
  </head>
  
  <body>
    
    <!-- PLAYGROUND -->
    <!-- TODO: the 3 rules below center a div inside a body -->
    <div style="display: flex; 
                align-items: center; 
                justify-content: center;">
      
      <div style="background: #409000; color: #FFFFFF; font-size: 20q; padding: 10px; margin: 5px;">Square</div>
      <div style="background: #409000; color: #FFFFFF; font-size: 20q; padding: 10px; margin: 5px;">Square</div>
      <div style="background: #409000; color: #FFFFFF; font-size: 20q; padding: 10px; margin: 5px;">Square</div>
      <div style="background: #409000; color: #FFFFFF; font-size: 20q; padding: 10px; margin: 5px;">Square</div>
      
    </div>
    
  </body>
  
</html>
```

### Aligning div columns at the top of a div

```html
<!DOCTYPE html>
<html>
  
  <head>
    <title>Ex2 - Columns</title>
    
  </head>
  
  <body>
    
    <div style="display: flex; align-items: flex-start;">
      
      <div style="background: #005000; height: 900px; width: 400px;"></div>
      
      <div style="width: 50px;"></div>
      
      <div style="background: #005000; height: 900px; width: 400px;"></div>
      
      <div style="width: 50px;"></div>
      
      <div style="background: #005000; height: 900px; width: 400px;"></div>
      
    </div>
    
  </body>
  
</html>
```

TODO: place divs one after the other, dynamic repositioning

TODO: round a div's corners

### Navbar

```html
<!DOCTYPE html>
<html>
  
  <head>
    <title>Ex3 - navbar</title>
  </head>
  
  <style>
    .navbar {
      top: 0;
      position: sticky;
      position: -webkit-sticky;
      overflow: hidden;
      display: flex;
      text-align: center;
      justify-content: center;
      background-color: #21252B;
      /* z-index: 10; */
    }
    .navbar a {
      display: inline-block;
      color: #FFFFFF;
      padding: 14px 20px;
    }
    .navbar a:hover {
      background-color: #282c34;
      color: #FFFFFF;
    }
    .navbar a.active {
      background-color: #282c34;
      color: #FFFFFF;
    }
  </style>
  
  <body>
    
    <!-- NAVBAR -->
    <div class="navbar">
      <a href="" class="active">Item 1</a>
      <a href="">Item 2</a>
      <a href="">Item 3</a>
      <a href="">Item 4</a>
    </div>
    
  </body>
  
</html>
```

### Sidebar

TODO: togglable sidebar, mobile-friendly

### Treeview

TODO: treeview

## Javascript

### Open a new page

Inside same tab:

```javascript
function openPage(url) {
  window.open(url, '_blank');
};
```

Inside new tab:

```javascript
function openPage(url) {
  window.location.href = url;
};
```

## PHP

...

# Alignment and centering

## HTML used:
```
<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>FlexBox Tutorial</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <div class="container">
    <div class="box box1">1</div>
    <div class="box box2">2</div>
    <div class="box box3">3</div>
    <div class="box box4">4</div>
    <div class="box box5">5</div>
    <div class="box box6">6</div>
    <div class="box box7">7</div>
    <div class="box box8">8</div>
    <div class="box box9">9</div>
    <div class="box box10">10</div>
  </div>
</body>
</html>
```

## Shared CSS:
```
/* CSS Normalize */
article,aside,details,figcaption,figure,footer,header,hgroup,nav,section,summary{display:block;}audio,canvas,video{display:inline-block;}audio:not([controls]){display:none;height:0;}[hidden]{display:none;}html{font-family:sans-serif;-webkit-text-size-adjust:100%;-ms-text-size-adjust:100%;}a:focus{outline:thin dotted;}a:active,a:hover{outline:0;}h1{font-size:2em;}abbr[title]{border-bottom:1px dotted;}b,strong{font-weight:700;}dfn{font-style:italic;}mark{background:#ff0;color:#000;}code,kbd,pre,samp{font-family:monospace, serif;font-size:1em;}pre{white-space:pre-wrap;word-wrap:break-word;}q{quotes:\201C \201D \2018 \2019;}small{font-size:80%;}sub,sup{font-size:75%;line-height:0;position:relative;vertical-align:baseline;}sup{top:-.5em;}sub{bottom:-.25em;}img{border:0;}svg:not(:root){overflow:hidden;}fieldset{border:1px solid silver;margin:0 2px;padding:.35em .625em .75em;}button,input,select,textarea{font-family:inherit;font-size:100%;margin:0;}button,input{line-height:normal;}button,html input[type=button],/* 1 */
input[type=reset],input[type=submit]{-webkit-appearance:button;cursor:pointer;}button[disabled],input[disabled]{cursor:default;}input[type=checkbox],input[type=radio]{box-sizing:border-box;padding:0;}input[type=search]{-webkit-appearance:textfield;-moz-box-sizing:content-box;-webkit-box-sizing:content-box;box-sizing:content-box;}input[type=search]::-webkit-search-cancel-button,input[type=search]::-webkit-search-decoration{-webkit-appearance:none;}textarea{overflow:auto;vertical-align:top;}table{border-collapse:collapse;border-spacing:0;}body,figure{margin:0;}legend,button::-moz-focus-inner,input::-moz-focus-inner{border:0;padding:0;}

/* Box-sizing border-box */
* { -moz-box-sizing: border-box; -webkit-box-sizing: border-box; box-sizing: border-box; }


/* Some default styles to make each box visible */
.box {
  color:white;
  font-size: 100px;
  text-align: center;
  text-shadow:4px 4px 0 rgba(0,0,0,0.1);
  padding:10px;
}

/* Colours for each box */
.box1 { background:#1abc9c;}
.box2 { background:#3498db;}
.box3 { background:#9b59b6;}
.box4 { background:#34495e;}
.box5 { background:#f1c40f;}
.box6 { background:#e67e22;}
.box7 { background:#e74c3c;}
.box8 { background:#bdc3c7;}
.box9 { background:#2ecc71;}
.box10 { background:#16a085;}
```

### justify-content: flex-start (aligned to the start of the container)

#### CSS
```
.container {
  display:flex;
  justify-content: flex-start;
}
```
![justify-content: flex-start](img/flex-start.png)

### justify-content: flex-end (aligned to the end of the container)

#### CSS
```
.container {
  display:flex;
  justify-content: flex-end;
  border: 10px solid mistyrose;
}
```
![justify-content: flex-end](img/flex-end.png)

### justify-content: center (aligned to the center of the container)

#### CSS
```
.container {
  display:flex;
  justify-content: center;
  border: 10px solid mistyrose;
}
```
![justify-content: center](img/center.png)

### justify-content: space-between

#### CSS
```
.container {
  display:flex;
  justify-content: space-between;
  border: 10px solid mistyrose;
}
```
![justify-content: space-between](img/space-between.png)

### justify-content: space-around

#### CSS
```
.container {
  display:flex;
  justify-content: space-around;
  border: 10px solid mistyrose;
}
```
![justify-content: space-around](img/space-around.png)

### justify-content: space-around (flex-direction: column + no container height set)

#### CSS
```
.container {
  display:flex;
  justify-content: space-around;
  border: 10px solid mistyrose;
  flex-direction: column;
}

.box {
  font-size: 20px; /* override 100px from above */
}
```
![justify-content: space-around + flex-direction: column + no container height](img/space-around-col-no-height.png)

### justify-content: space-around (flex-direction: column)

#### CSS
```
.container {
  display:flex;
  justify-content: space-around;
  border: 10px solid mistyrose;
  flex-direction: column;
  min-height: 100vh;
}

.box {
  font-size: 20px; /* override 100px from above */
}
```
![justify-content: space-around + flex-direction: column](img/space-around-col.png)

### justify-content: flex-start (flex-direction: column)

#### CSS
```
.container {
  display:flex;
  justify-content: flex-start;
  border: 10px solid mistyrose;
  flex-direction: column;
  min-height: 100vh;
}

.box {
  font-size: 20px; /* override 100px from above */
}
```
![justify-content: flex-start + flex-direction: column](img/flex-start-col.png)

### justify-content: flex-end (flex-direction: column)

#### CSS
```
.container {
  display:flex;
  justify-content: flex-end;
  border: 10px solid mistyrose;
  flex-direction: column;
  min-height: 100vh;
}

.box {
  font-size: 20px; /* override 100px from above */
}
```
![justify-content: flex-end + flex-direction: column](img/flex-end-col.png)

### justify-content: center (flex-direction: column)

#### CSS
```
.container {
  display:flex;
  justify-content: center;
  border: 10px solid mistyrose;
  flex-direction: column;
  min-height: 100vh;
}

.box {
  font-size: 20px; /* override 100px from above */
}
```
![justify-content: centert + flex-direction: column](img/center-col.png)
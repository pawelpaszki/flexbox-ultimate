# Alignment and centering with align-content

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

### no align-content (or align-content: stretch)

#### CSS
```
.container {
  display:flex;
  border: 10px solid mistyrose;
  min-height: 100vh;
  flex-wrap: wrap;
}

.box {
  width: 33.33333%;
}
```
![no align-content](img/no-align-content.png)

### align-content: flex-start

#### CSS
```
.container {
  display:flex;
  border: 10px solid mistyrose;
  min-height: 100vh;
  flex-wrap: wrap;
  align-content: flex-start;
}

.box {
  width: 33.33333%;
}
```
![align-content: flex-start](img/align-content-flex-start.png)

### align-items: flex-end

#### CSS
```
.container {
  display:flex;
  border: 10px solid mistyrose;
  min-height: 100vh;
  flex-wrap: wrap;
  align-content: flex-end;
}

.box {
  width: 33.33333%;
}
```
![align-content: flex-end](img/align-content-flex-end.png)

### align-content: space-between

#### CSS
```
.container {
  display:flex;
  border: 10px solid mistyrose;
  min-height: 100vh;
  flex-wrap: wrap;
  align-content: space-between;
}

.box {
  width: 33.33333%;
}
```
![align-content: space-between](img/align-items-space-between.png)

### align-content: space-around

#### CSS
```
.container {
  display:flex;
  border: 10px solid mistyrose;
  min-height: 100vh;
  flex-wrap: wrap;
  align-content: space-around;
}

.box {
  width: 33.33333%;
}
```
![align-content: space-around](img/align-items-space-around.png)

### align-content: center

#### CSS
```
.container {
  display:flex;
  border: 10px solid mistyrose;
  min-height: 100vh;
  flex-wrap: wrap;
  align-content: center;
}

.box {
  width: 33.33333%;
}
```
![align-content: center](img/align-items-center.png)

### align-content: center + justify-content: center

#### CSS
```
.container {
  display:flex;
  border: 10px solid mistyrose;
  min-height: 100vh;
  flex-wrap: wrap;
  align-content: center;
  justify-content: center;
}

.box {
  width: 33.33333%;
}
```
![align-content: center + align-content: center + justify-content: center](img/align-items-center-justify-content-center.png)
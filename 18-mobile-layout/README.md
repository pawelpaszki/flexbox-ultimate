# Mobile app layout with flexbox

## HTML used:
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>FlexBox Nav</title>
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.3.0/css/font-awesome.min.css">
  <link rel="stylesheet" href="style.css">
</head>
<body>
  
  <div class="app-wrap">
    
    <header class="app-header">
      <a href="#" class="button">
        <i class="fa fa-arrow-left"></i>
        Back
      </a>

      <h1>FlexBox App Layout</h1>

      <a href="#" class="button">
        <i class="fa fa-cog"></i>
      </a>
    </header>

    <div class="content">
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequatur, beatae?</p>

      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Doloremque deserunt quisquam repellendus quia autem saepe culpa fugit nulla distinctio hic, beatae cum, perspiciatis iusto natus nesciunt itaque quaerat, earum ex.</p>
      
      <img src="https://avatars2.githubusercontent.com/u/176013">

      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ullam quo ipsa excepturi sunt, quibusdam, quos!

      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Modi natus dolores placeat esse ratione fugiat voluptatum impedit blanditiis consequuntur quos debitis consequatur ea beatae fuga perspiciatis vero, mollitia, molestias omnis. Dolorum quas iusto, molestiae ut at architecto dolorem nulla est!</p>

      <p>lorem ipsum dolor sit amet, consectetur adipisicing elit. nulla, illum ea consectetur!</p>

      <p>lorem ipsum dolor sit amet, consectetur adipisicing elit. cumque ea, mollitia sequi quo consequatur dolor itaque numquam, aut tempore suscipit, ut quaerat. qui!</p>

      <p>lorem ipsum dolor sit amet, consectetur adipisicing elit. aliquam id rem numquam, illum atque ducimus maiores assumenda dolorum ut.</p>

      <p>lorem ipsum dolor sit amet, consectetur adipisicing elit. accusantium cum unde animi, obcaecati, minima odio.</p>

      <p>lorem ipsum dolor sit amet, consectetur adipisicing elit. nulla, illum ea consectetur!</p>

      <p>lorem ipsum dolor sit amet, consectetur adipisicing elit. cumque ea, mollitia sequi quo consequatur dolor itaque numquam, aut tempore suscipit, ut quaerat. qui!</p>

      <p>lorem ipsum dolor sit amet, consectetur adipisicing elit. aliquam id rem numquam, illum atque ducimus maiores assumenda dolorum ut.</p>

      <p>lorem ipsum dolor sit amet, consectetur adipisicing elit. accusantium cum unde animi, obcaecati, minima odio.</p>

      <p>lorem ipsum dolor sit amet, consectetur adipisicing elit. nulla, illum ea consectetur!</p>

      <p>lorem ipsum dolor sit amet, consectetur adipisicing elit. cumque ea, mollitia sequi quo consequatur dolor itaque numquam, aut tempore suscipit, ut quaerat. qui!</p>

      <p>lorem ipsum dolor sit amet, consectetur adipisicing elit. aliquam id rem numquam, illum atque ducimus maiores assumenda dolorum ut.</p>

      <p>lorem ipsum dolor sit amet, consectetur adipisicing elit. accusantium cum unde animi, obcaecati, minima odio.</p>
    </div>

    <div class="icon-bar">
      <a href="#">
        <i class="fa fa-home"></i>
        Home
      </a>
      <a href="#">
        <i class="fa fa-bell"></i>
        Notifications
      </a>
      <a href="#">
        <i class="fa fa-envelope"></i>
        Messages
      </a>
      <a href="#">
        <i class="fa fa-user"></i>
        Me
      </a>
    </div>


  </div>

</body>
</html>
```

### init version

#### CSS
```
/* Some CSS Setup - nothing to do with flexbox */
html {
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: inherit;
}

html {
  font-size: 10px;
}

body {
  font-family: sans-serif;
  margin: 0;
  font-size: 1.5rem;
  background-image: linear-gradient(260deg, #2376ae 0%, #c16ecf 100%);
}

a {
  color:white;
  text-decoration: none;
}

a.button {
  background:rgba(0,0,0,0.1);
  padding:1rem 1.5rem;
  border-radius:4px;
}


.app-wrap {
  max-width:540px;
  height: 90vh;
  margin: 5vh auto 5vh auto;
  border:10px solid rgba(0,0,0,0.8);
  border-bottom-width: 70px;
  border-radius:10px;
  box-shadow:0 0 50px  rgba(0,0,0,0.3);
}


.content {
  padding:20px;
  background:white;
  box-shadow:inset 0 5px 0 rgba(0,0,0,0.1);
  line-height: 1.6;
}

.content img {
  max-width:50%;
  float:left;
  margin-right: 10px;
}


.icon-bar a {
  flex:1;
  text-align: center;
  padding:1.5rem;
  border-left:1px solid rgba(0,0,0,0.1);
  background:#EFCA51;
  color:rgba(0,0,0,0.5);
}

.icon-bar a:first-child {
  border-left: 0;
}

.icon-bar a:first-child, .icon-bar a:hover {
  border-bottom: 5px solid rgba(0,0,0,0.1);
}

.icon-bar {
  border-top:1px solid #E6E6E6;
}

.icon-bar i {
  display: block;
  font-size: 2.5rem;
  color:white;
  text-shadow:3px 3px 0 rgba(0,0,0,0.1);
  padding-bottom: 1rem;
}

.app-header {
  background:#F0CB45;
  color:rgba(0,0,0,0.5);
  padding:1rem;
}


/*
  Everything So far is Cosmetic styling 
  Flexbox + Important CSS Starts Here
*/


/*
  Overall Layout
*/
```
![initial view](img/init.png)

### added flex grow, shrink and basis (auto - take as much as needed) and added scroll to the main content

#### CSS
```
/* Some CSS Setup - nothing to do with flexbox */
html {
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: inherit;
}

html {
  font-size: 10px;
}

body {
  font-family: sans-serif;
  margin: 0;
  font-size: 1.5rem;
  background-image: linear-gradient(260deg, #2376ae 0%, #c16ecf 100%);
}

a {
  color:white;
  text-decoration: none;
}

a.button {
  background:rgba(0,0,0,0.1);
  padding:1rem 1.5rem;
  border-radius:4px;
}


.app-wrap {
  max-width:540px;
  height: 90vh;
  margin: 5vh auto 5vh auto;
  border:10px solid rgba(0,0,0,0.8);
  border-bottom-width: 70px;
  border-radius:10px;
  box-shadow:0 0 50px  rgba(0,0,0,0.3);
}


.content {
  padding:20px;
  background:white;
  box-shadow:inset 0 5px 0 rgba(0,0,0,0.1);
  line-height: 1.6;
}

.content img {
  max-width:50%;
  float:left;
  margin-right: 10px;
}


.icon-bar a {
  flex:1;
  text-align: center;
  padding:1.5rem;
  border-left:1px solid rgba(0,0,0,0.1);
  background:#EFCA51;
  color:rgba(0,0,0,0.5);
}

.icon-bar a:first-child {
  border-left: 0;
}

.icon-bar a:first-child, .icon-bar a:hover {
  border-bottom: 5px solid rgba(0,0,0,0.1);
}

.icon-bar {
  border-top:1px solid #E6E6E6;
}

.icon-bar i {
  display: block;
  font-size: 2.5rem;
  color:white;
  text-shadow:3px 3px 0 rgba(0,0,0,0.1);
  padding-bottom: 1rem;
}

.app-header {
  background:#F0CB45;
  color:rgba(0,0,0,0.5);
  padding:1rem;
}


/*
  Everything So far is Cosmetic styling 
  Flexbox + Important CSS Starts Here
*/


/*
  Overall Layout
*/

/* flex container */
.app-wrap {
  display: flex;
  flex-direction: column;
}

/* flex items */
.app-wrap > * {
  flex: 1 1 auto;
}

.content {
  overflow-y: scroll;
}
```
![flex added along with init sizing](img/init-flex.png)

### Formatted app header

#### CSS
```
/* Some CSS Setup - nothing to do with flexbox */
html {
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: inherit;
}

html {
  font-size: 10px;
}

body {
  font-family: sans-serif;
  margin: 0;
  font-size: 1.5rem;
  background-image: linear-gradient(260deg, #2376ae 0%, #c16ecf 100%);
}

a {
  color:white;
  text-decoration: none;
}

a.button {
  background:rgba(0,0,0,0.1);
  padding:1rem 1.5rem;
  border-radius:4px;
}


.app-wrap {
  max-width:540px;
  height: 90vh;
  margin: 5vh auto 5vh auto;
  border:10px solid rgba(0,0,0,0.8);
  border-bottom-width: 70px;
  border-radius:10px;
  box-shadow:0 0 50px  rgba(0,0,0,0.3);
}


.content {
  padding:20px;
  background:white;
  box-shadow:inset 0 5px 0 rgba(0,0,0,0.1);
  line-height: 1.6;
}

.content img {
  max-width:50%;
  float:left;
  margin-right: 10px;
}


.icon-bar a {
  flex:1;
  text-align: center;
  padding:1.5rem;
  border-left:1px solid rgba(0,0,0,0.1);
  background:#EFCA51;
  color:rgba(0,0,0,0.5);
}

.icon-bar a:first-child {
  border-left: 0;
}

.icon-bar a:first-child, .icon-bar a:hover {
  border-bottom: 5px solid rgba(0,0,0,0.1);
}

.icon-bar {
  border-top:1px solid #E6E6E6;
}

.icon-bar i {
  display: block;
  font-size: 2.5rem;
  color:white;
  text-shadow:3px 3px 0 rgba(0,0,0,0.1);
  padding-bottom: 1rem;
}

.app-header {
  background:#F0CB45;
  color:rgba(0,0,0,0.5);
  padding:1rem;
}


/*
  Everything So far is Cosmetic styling 
  Flexbox + Important CSS Starts Here
*/


/*
  Overall Layout
*/

/* flex container */
.app-wrap {
  display: flex;
  flex-direction: column;
}

/* flex items */
.app-wrap > * {
  flex: 1 1 auto;
}

/* header */
.app-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

/* content */
.content {
  overflow-y: scroll;
  -webkit-overflow-scrolling: touch;
}
```
![formatted app header](img/header.png)

### Formatted icon bar (footer)

#### CSS
```
/* Some CSS Setup - nothing to do with flexbox */
html {
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: inherit;
}

html {
  font-size: 10px;
}

body {
  font-family: sans-serif;
  margin: 0;
  font-size: 1.5rem;
  background-image: linear-gradient(260deg, #2376ae 0%, #c16ecf 100%);
}

a {
  color:white;
  text-decoration: none;
}

a.button {
  background:rgba(0,0,0,0.1);
  padding:1rem 1.5rem;
  border-radius:4px;
}


.app-wrap {
  max-width:540px;
  height: 90vh;
  margin: 5vh auto 5vh auto;
  border:10px solid rgba(0,0,0,0.8);
  border-bottom-width: 70px;
  border-radius:10px;
  box-shadow:0 0 50px  rgba(0,0,0,0.3);
}


.content {
  padding:20px;
  background:white;
  box-shadow:inset 0 5px 0 rgba(0,0,0,0.1);
  line-height: 1.6;
}

.content img {
  max-width:50%;
  float:left;
  margin-right: 10px;
}


.icon-bar a {
  flex:1;
  text-align: center;
  padding:1.5rem;
  border-left:1px solid rgba(0,0,0,0.1);
  background:#EFCA51;
  color:rgba(0,0,0,0.5);
}

.icon-bar a:first-child {
  border-left: 0;
}

.icon-bar a:first-child, .icon-bar a:hover {
  border-bottom: 5px solid rgba(0,0,0,0.1);
}

.icon-bar {
  border-top:1px solid #E6E6E6;
}

.icon-bar i {
  display: block;
  font-size: 2.5rem;
  color:white;
  text-shadow:3px 3px 0 rgba(0,0,0,0.1);
  padding-bottom: 1rem;
}

.app-header {
  background:#F0CB45;
  color:rgba(0,0,0,0.5);
  padding:1rem;
}


/*
  Everything So far is Cosmetic styling 
  Flexbox + Important CSS Starts Here
*/


/*
  Overall Layout
*/

/* flex container */
.app-wrap {
  display: flex;
  flex-direction: column;
}

/* flex items */
.app-wrap > * {
  flex: 1 1 auto;
}

/* header */
.app-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

/* content */
.content {
  overflow-y: scroll;
  -webkit-overflow-scrolling: touch;
}

/* icon bar */
.icon-bar {
  display: flex;
}

.icon-bar a {
  flex: 1;
}
```
![formatted app footer](img/footer.png)
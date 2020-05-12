# navigation bar with flexbox

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
  
  <div class="wrapper">
    
    <header class="top">
      <h1><a href="#">What The Flexbox?!</a></h1>
    </header>

    <nav class="flex-nav">
      <a href="#" class="toggleNav">☰ Menu</a>
      <ul>
        <li><a href="#">Item 01</a></li>
        <li><a href="#">Item 02</a></li>
        <li><a href="#">Item 03</a></li>
        <li><a href="#">Item 04</a></li>
        <li><a href="#">Item 05</a></li>
        <li><a href="#">Item 06</a></li>
        <li class="social">
          <a href="http://twitter.com/wesbos"><i class="fa fa-twitter"></i></a>
        </li>
        <li class="social">
          <a href="http://facebook.com/wesbos.developer"><i class="fa fa-facebook"></i></a>
        </li>
        <li class="social">
          <a href="http://github.com/wesbos"><i class="fa fa-github"></i></a>
        </li>
        <li class="social">
          <a href="http://instagram.com/wesbos"><i class="fa fa-instagram"></i></a>
        </li>
      </ul>
    </nav>

    <section class="hero">
      <img src="http://lorempixel.com/1000/600/abstract">
    </section>

    <section class="details">
      <p>A simple video course to help you master FlexBox.</p>
      <p>Sign up today to grab all the videos and exercises!</p>
    </section>

    <section class="signup">
      <form action="" class="signup">
        <input type="text" placeholder="Your Name">
        <input type="email" placeholder="Email Address">
        <input type="submit" value="Sign me up!">
      </form>
    </section>

    <footer>
      <p>&copy; Wes Bos</p>
    </footer>


  </div>

  <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js"></script>
  <script>
    
    $(function() {
      $('.toggleNav').on('click',function() {
        $('.flex-nav ul').toggleClass('open');
      });
    });

  </script>
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

body {
  font-family: sans-serif;
  margin: 0;
  background-image: linear-gradient(260deg, #2376ae 0%, #c16ecf 100%);
}

a {
  color:white;
  font-weight: 100;
  letter-spacing: 2px;
  text-decoration: none;
  background:rgba(0,0,0,0.2);
  padding:20px 5px;
  display: inline-block;
  width: 100%;
  text-align: center;
  transition:all 0.5s;
}

a:hover {
  background:rgba(0,0,0,0.3);
}

.toggleNav {
  display: none;
}

img {
  width:100%;
}

.wrapper {
  max-width: 1000px;
  margin: 0 auto;
}

input {
  padding:10px;
  border:0;
}


section, footer {
  text-align: center;
  background:rgba(0,0,0,0.2);
  padding:20px;
  margin:20px 0;
  color:white;
  font-weight: 100;
}

/* Flex Container */
.flex-nav ul {
  border:1px solid black;
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
}

.flex-nav li {
  flex: 3;
}

.flex-nav .social {
  flex: 1;
}


@media all and (max-width:1000px) {
  
  .flex-nav ul {
    flex-wrap: wrap;
  }

  .flex-nav li {
    flex: 1 1 50%;
  }

  .flex-nav .social {
    flex: 1 1 25%;
  }

}

@media all and (max-width:500px) {
  
  .flex-nav li {
    flex: 1 1 100%;
  }

}
```
![initial view](img/init.png)

### added menu reordering and toggling

#### CSS
```
html {
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: inherit;
}

body {
  font-family: sans-serif;
  margin: 0;
  background-image: linear-gradient(260deg, #2376ae 0%, #c16ecf 100%);
}

a {
  color:white;
  font-weight: 100;
  letter-spacing: 2px;
  text-decoration: none;
  background:rgba(0,0,0,0.2);
  padding:20px 5px;
  display: inline-block;
  width: 100%;
  text-align: center;
  transition:all 0.5s;
}

a:hover {
  background:rgba(0,0,0,0.3);
}

.toggleNav {
  display: none;
}

img {
  width:100%;
}

.wrapper {
  max-width: 1000px;
  margin: 0 auto;
}

input {
  padding:10px;
  border:0;
}


section, footer {
  text-align: center;
  background:rgba(0,0,0,0.2);
  padding:20px;
  margin:20px 0;
  color:white;
  font-weight: 100;
}

/* Flex Container */
.flex-nav ul {
  border:1px solid black;
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
}

.flex-nav li {
  flex: 3;
}

.flex-nav .social {
  flex: 1;
}


@media all and (max-width:1000px) {
  
  .flex-nav ul {
    flex-wrap: wrap;
  }

  .flex-nav li {
    flex: 1 1 50%;
  }

  .flex-nav .social {
    flex: 1 1 25%;
  }

}

@media all and (max-width:500px) {
  
  .flex-nav li {
    flex: 1 1 100%;
  }

  /* flex container */
  .wrapper {
    display: flex;
    flex-direction: column;
  }

  /* flex item */
  .wrapper > * {
    order: 9999;
  }

  .flex-nav {
    order: 1;
  }

  .toggleNav {
    display: block;
  }

  .flex-nav ul {
    display: none;
  }

  .flex-nav ul.open {
    display: flex;
  }

}
```
![menu toggle and reorder](img/menu-toggle-reorder.png)

![menu toggle and reorder less than 500px width](img/menu-toggle-reorder-mobile.png)

![menu toggle and reorder less than 500px width (open)](img/menu-toggle-reorder-mobile-open.png)

### other items reordered

#### CSS
```
/* Some CSS Setup - nothing to do with flexbox */
html {
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: inherit;
}

body {
  font-family: sans-serif;
  margin: 0;
  background-image: linear-gradient(260deg, #2376ae 0%, #c16ecf 100%);
}

a {
  color:white;
  font-weight: 100;
  letter-spacing: 2px;
  text-decoration: none;
  background:rgba(0,0,0,0.2);
  padding:20px 5px;
  display: inline-block;
  width: 100%;
  text-align: center;
  transition:all 0.5s;
}

a:hover {
  background:rgba(0,0,0,0.3);
}

.toggleNav {
  display: none;
}

img {
  width:100%;
}

.wrapper {
  max-width: 1000px;
  margin: 0 auto;
}

input {
  padding:10px;
  border:0;
}


section, footer {
  text-align: center;
  background:rgba(0,0,0,0.2);
  padding:20px;
  margin:20px 0;
  color:white;
  font-weight: 100;
}

/* Flex Container */
.flex-nav ul {
  border:1px solid black;
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
}

.flex-nav li {
  flex: 3;
}

.flex-nav .social {
  flex: 1;
}


@media all and (max-width:1000px) {
  
  .flex-nav ul {
    flex-wrap: wrap;
  }

  .flex-nav li {
    flex: 1 1 50%;
  }

  .flex-nav .social {
    flex: 1 1 25%;
  }

}

@media all and (max-width:500px) {
  
  .flex-nav li {
    flex: 1 1 100%;
  }

  /* flex container */
  .wrapper {
    display: flex;
    flex-direction: column;
  }

  /* flex item */
  .wrapper > * {
    order: 9999;
  }

  .flex-nav {
    order: 1;
  }

  .toggleNav {
    display: block;
  }

  .flex-nav ul {
    display: none;
  }

  .flex-nav ul.open {
    display: flex;
  }

  .top {
    order: 2;
  }

  .details {
    order: 3;
  }

  .signup {
    order: 4;
  }
  
}
```
![display: flex + flex: 1](img/final-reordering.png)

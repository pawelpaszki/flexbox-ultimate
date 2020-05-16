# Pricing grid

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

  <!-- Flex Container! -->
  <div class="pricing-grid">

    <div class="plan plan1">
      
      <h2>Cat</h2>
      <p>Common, yet regarded by many as the worst house pet.</p>
      <ul class="features">
        <li>Scratches everything</li>
        <li>Easily lost for days</li>
        <li>Kind of a bummer</li>
      </ul>

      <p class="price">free</p>

      <a href="#" class="cta">😾 Really?</a>
    </div>

    <div class="plan plan2">
      
      <h2>Dog</h2>
      <p>Loving, gentle and caring. Dogs are the best house pet to have and will increase happiness ten fold. </p>
      <ul class="features">
        <li>Super Fun</li>
        <li>Friends love them</li>
        <li>Plays games</li>
        <li>Not a cat</li>
      </ul>

      <p class="price">$90</p>

      <a href="#" class="cta">🐶 Best Deal →</a>
    </div>

    <div class="plan plan3">
      
      <h2>Fish</h2>
      <p>Cheap n' easy.</p>
      <ul class="features">
        <li>Eats flakes</li>
        <li>Cop out</li>
        <li>Replaceable</li>
      </ul>

      <p class="price">$3</p>

      <a href="#" class="cta">🐠</a>
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

body {
  font-family: sans-serif;
  margin: 0;
  background-image: linear-gradient(260deg, #2376ae 0%, #c16ecf 100%);
}

a {
  color:white;
}

.plan ul {
  margin: 0;
  padding: 0;
  list-style: none;
}

.plan ul li {
  border-bottom: 1px solid rgba(0,0,0,0.1);
  padding:10px;
}

.plan ul li:last-child {
  border-bottom: 0;
}

.plan a {
  text-decoration: none;
  background:#FEFF00;
  padding:10px;
  color:black;
  border-radius:4px;
}


.plan h2 {
  text-transform: uppercase;
  color:white;
  letter-spacing: 2px;
  text-shadow:3px 3px 0 rgba(0,0,0,0.1);
}

.price {
  font-size: 50px;
  font-family: serif;
  margin: 10px 0;
}


.pricing-grid {
  max-width:750px;
  margin: 0 auto;
  
}
```
![initial view](img/init.png)

### added display: flex

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
}

.plan ul {
  margin: 0;
  padding: 0;
  list-style: none;
}

.plan ul li {
  border-bottom: 1px solid rgba(0,0,0,0.1);
  padding:10px;
}

.plan ul li:last-child {
  border-bottom: 0;
}

.plan a {
  text-decoration: none;
  background:#FEFF00;
  padding:10px;
  color:black;
  border-radius:4px;
}


.plan h2 {
  text-transform: uppercase;
  color:white;
  letter-spacing: 2px;
  text-shadow:3px 3px 0 rgba(0,0,0,0.1);
}

.price {
  font-size: 50px;
  font-family: serif;
  margin: 10px 0;
}

/* flex container */
.pricing-grid {
  max-width:750px;
  margin: 0 auto;
  display: flex;
}
```
![flex container](img/flex.png)

### added equal widto + margin/ padding and text-align

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
}

.plan ul {
  margin: 0;
  padding: 0;
  list-style: none;
}

.plan ul li {
  border-bottom: 1px solid rgba(0,0,0,0.1);
  padding:10px;
}

.plan ul li:last-child {
  border-bottom: 0;
}

.plan a {
  text-decoration: none;
  background:#FEFF00;
  padding:10px;
  color:black;
  border-radius:4px;
}


.plan h2 {
  text-transform: uppercase;
  color:white;
  letter-spacing: 2px;
  text-shadow:3px 3px 0 rgba(0,0,0,0.1);
}

.price {
  font-size: 50px;
  font-family: serif;
  margin: 10px 0;
}

/* flex container */
.pricing-grid {
  max-width:750px;
  margin: 0 auto;
  display: flex;
}

/* flex item */
.plan {
  flex: 1;
  background: rgba(255, 255, 255, 0.2);
  margin: 20px;
  padding: 20px;
  border-radius: 4px;
  text-align: center;
}
```
![added equal widto + margin/ padding and text-align](img/center-init.png)

### equal height flex-items

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
}

.plan ul {
  margin: 0;
  padding: 0;
  list-style: none;
}

.plan ul li {
  border-bottom: 1px solid rgba(0,0,0,0.1);
  padding:10px;
}

.plan ul li:last-child {
  border-bottom: 0;
}

.plan a {
  text-decoration: none;
  background:#FEFF00;
  padding:10px;
  color:black;
  border-radius:4px;
}


.plan h2 {
  text-transform: uppercase;
  color:white;
  letter-spacing: 2px;
  text-shadow:3px 3px 0 rgba(0,0,0,0.1);
}

.price {
  font-size: 50px;
  font-family: serif;
  margin: 10px 0;
}

/* flex container */
.pricing-grid {
  max-width:750px;
  margin: 0 auto;
  display: flex;
}

/* flex item */
.plan {
  background: rgba(255, 255, 255, 0.2);
  margin: 20px;
  padding: 20px;
  border-radius: 4px;
  text-align: center;
  flex: 1;
  display: flex;
  flex-wrap: wrap;
}

.plan > * {
  flex: 1 1 100%;
}

.plan .cta {
  align-self: flex-end;
}
```
![equal height items with button at the bottom](img/equal-height.png)

### non stretched flex items

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
}

.plan ul {
  margin: 0;
  padding: 0;
  list-style: none;
}

.plan ul li {
  border-bottom: 1px solid rgba(0,0,0,0.1);
  padding:10px;
}

.plan ul li:last-child {
  border-bottom: 0;
}

.plan a {
  text-decoration: none;
  background:#FEFF00;
  padding:10px;
  color:black;
  border-radius:4px;
}


.plan h2 {
  text-transform: uppercase;
  color:white;
  letter-spacing: 2px;
  text-shadow:3px 3px 0 rgba(0,0,0,0.1);
}

.price {
  font-size: 50px;
  font-family: serif;
  margin: 10px 0;
}

/* flex container */
.pricing-grid {
  max-width:750px;
  margin: 0 auto;
  display: flex;
  align-items: center;
}

/* flex item */
.plan {
  background: rgba(255, 255, 255, 0.2);
  margin: 20px;
  padding: 20px;
  border-radius: 4px;
  text-align: center;
  flex: 1;
  display: flex;
  flex-wrap: wrap;
}

.plan > * {
  flex: 1 1 100%;
}

.plan .cta {
  align-self: flex-end;
}
```
![non stretched flex items](img/non-stretched-items.png)

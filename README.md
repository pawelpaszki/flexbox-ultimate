# flexbox-ultimate 

```
display: flex # make the container flex
```

[intro - display: flex/ inline-flex](01-intro/README.md)

[flex-direction: row / column / row-reversed / column-reversed](02-direction/README.md)

[flex-wrap: nowrap / wrap / wrap-reverse](03-wrapping/README.md)

[order](04-ordering/README.md)

## display
`inline-flex` - wraps around the content

`flex` - all the way across

`flex-items` -> all immediate children of container with `display: flex`

## flex-direction
`flex-direction: row` - `default direction` (flex-items placed left to right). Height of the flex-items to match the container. **main axis** - left to right and **cross axis** - top to bottom

`flex-direction: column` - flex-items placed top to bottom. **main axis** - top to bottom and **cross axis** - left to right

`flex-direction: row-reverse` - flex-items placed right to left. Height of the flex-items to match the container. **main axis** - right to left and **cross axis** - top to bottom

`flex-direction: column-reverse` - flex-items placed bottom to top. **main axis** - bottom to top and **cross axis** - left to right

## flex-wrap
`flex-wrap: nowrap` - `default setting` - if there are multiple `flex-items` with their width set inside a container without any other properties set (see below), they will fill up only the available space, despite their overall width being larger than the container width:

```
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
```

```
.container {
  display:flex;
  border:10px solid goldenrod;
  min-height: 100vh;
}

.box {
  width: 300px;
}
```

`flex-wrap: wrap` - the items will fill the container vertically and will be broken into multiple lines, if their combined width is greater than container's width

Note.
There will be gap between the last flex-item and the end of the browser viewpost, unless the width of the browser is exactly n * width of the flex-item and n is less than the number of the flex-items

`flex: 1` - when set for all `flex-items`, will spread them evenly inside the container

`order` - orders `flex-items` inside a flex container. **Default** order is **0**: `order: 0`

Negative order is also allowed, e.g. `order: -1`
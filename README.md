# flexbox-ultimate 

```
display: flex # make the container flex
```

[intro - display: flex/ inline-flex](01-intro/README.md)

[flex-direction: row / column / row-reversed / column-reversed](02-direction/README.md)

[flex-wrap: nowrap / wrap / wrap-reverse](03-wrapping/README.md)

[order](04-ordering/README.md)

[justify-content: flex-start / flex-end / center / space-between / space-around](05-alignment-centering/README.md)

[align-items: flex-start / flex-end / center / baseline / stretch](06-align-items/README.md)

[align-content: flex-start / flex-end / center / space-between / space-around](07-align-content/README.md)

[align-self: flex-start / flex-end / center / baseline / stretch](08-align-self/README.md)

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

## order

`flex: 1` - when set for all `flex-items`, will spread them evenly inside the container

`order` - orders `flex-items` inside a flex container. **Default** order is **0**: `order: 0`

Negative order is also allowed, e.g. `order: -1`

## alignment and centering

`justify-content` - how are the items aligned on the `main axis`

`justify-content: flex-start` - items aligned to the start of the container

`justify-content: flex-end` - items aligned to the end of the container

`justify-content: center` - items aligned to the center of the container

`justify-content: space-between` - start first item at the start of the container, last one at the end and divide up the rest of the space between remaining flex-items

`justify-content: space-around` - the white space divided evenly around all flex-items

**Important** - when using `flex-direction: column` to take effect when using `justify-content`, height of the container has to be set

## align-items

`align-items` is concerned about the `cross axis`

default value for `align-items` is `stretch`

`align-items: center` - vertically aligns items (in default flex-direction) or horizontally aligns items in `flex-direction: column`

`align-items: flex-start` - aligns items at the start of the container (on the `cross axis`)

`align-items: flex-end` - aligns items at the end of the container (on the `cross axis`)

`align-items: baseline` - align bottom of the letters at the same line

## align-content

`align-content` - takes the extra space on the `cross axis`. This only works if there are multiple lines of content + if wrapping is enabled

default value for `align-content` is `stretch`

`align-items: flex-start` - aligns content at the start of the container on the `cross axis`. Flex-items only take as much space as needed (e.g. there might be extra room at the bottom). If there is an item that takes more space than other ones, those items will still use the same height across the row

`align-items: flex-end` - aligns content at the end of the container on the `cross axis`

`align-items: space-between` - leftover space will be shared evenly between the end of the first item, beginning of the last item and all remaining items

`align-items: space-around` - leftover space will be shared evenly between to the left and right of each flex-item

## align-self

`align-self` - allows to override align-items property for individual flex-item(s). By default `align-self` is equal to `align-items`, when not set

`align-self: center` - vertically aligns item (in default flex-direction) or horizontally aligns item in `flex-direction: column`

`align-self: flex-start` - aligns item at the start of the container (on the `cross axis`)

`align-self: flex-end` - aligns item at the end of the container (on the `cross axis`)

`align-self: baseline` - align bottom of the letters at the same line
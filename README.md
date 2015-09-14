Left aligned and centered grid with flexbox

I'd like to implement a responsive grid-like layout using flexbox (without media queries). There can be variable number of elements in the grid. Each item should have fixed and equal width. Items should be aligned to the left. Whole group should have equal left and right margins.

It should look like that:



This is how I tried to achieve it:


    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="utf-8" />
      <style>
        .container {
          display: flex;
          flex-wrap: wrap;
          justify-content: flex-start;
          margin: auto;
        }
        .item {
          height: 200px;
          width: 200px;
          background-color: purple;
          padding: 10px;
          margin: 10px;
        }
      </style>
    </head>

    <body>
      <div class="container">
        <div class="item">Flex item 1</div>
        <div class="item">Flex item 2</div>
        <div class="item">Flex item 3</div>
        <div class="item">Flex item 4</div>
        <div class="item">Flex item 5</div>
      </div>
    </body>

    </html>


It didn't work:



I was hoping that setting `margin: auto` on a container will force it to have width just enough to fit optimal number of items in each row.

I know I can make it easily using framework like Bootstrap or Foundations but I wonder if it's possible to use flexbox as well.

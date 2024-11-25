<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>grid</title>
  </head>
  <body>
    <style>
      .header {
        grid-area: main-header;
        background-color: aqua;
        border-radius: 4px;
        text-align: center;
      }
      .menu {
        grid-area: menu;
        background-color: antiquewhite;
        border-radius: 4px;
      }
      .main {
        grid-area: main;
        background-color: rgb(236, 177, 105);
        border-radius: 4px;
      }
      .content {
        grid-area: content;
        background-color: aquamarine;
        border-radius: 4px;
      }
      .footer {
        grid-area: footer;
        background-color: cadetblue;
        border-radius: 4px;
      }
      .grid-container {
        display: grid;
        grid-template-areas:
          "main-header main-header main-header"
          "menu main content"
          "menu main content"
          "menu main content"
          "menu main content"
          "menu footer footer";
        column-gap: 10px;
        row-gap: 10px;
      }
      .footer {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 3px;
      }
      .footer h1 {
        border: 1px solid black;
        padding: 0px;
        background-color: red;
      }
      @media (max-width: 500px) {
        .grid-container {
          display: grid;
          grid-template-areas:
            "main-header main-header main-header"
            "menu menu menu "
            "main main main"
            "content content content"
            "footer footer footer";
          column-gap: 10px;
          row-gap: 10px;
        }
      }
    </style>
    <div>
      <div class="grid-container">
        <div class="header">
          <h1>Header</h1>
        </div>
        <div class="menu">
          <h1>Menu</h1>
        </div>
        <div class="main">
          <h1>Main</h1>
          <h1>Main</h1>
          <h1>Main</h1>
          <h1>Main</h1>
        </div>
        <div class="content">
          <h1>content</h1>
        </div>
        <div class="footer">
          <h1>Footer</h1>
          <h1>Footer</h1>
          <h1>Footer</h1>
        </div>
      </div>
    </div>
  </body>
</html>


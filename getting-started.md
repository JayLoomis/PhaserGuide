# Getting Started with Phaser

Phaser is a JavaScript library for making 2D games in HTML 5.

## Build environment
To get started, you need:

-   A copy of the library (phaser.js) which you can get
    [here](https://phaser.io/download/stable).
    -   Download the **js** file while developing, because it has comments and
        such to help.
    -   Use the **min.js** file in production, because it's been minified to
        download faster.
-   A local web server to test your work.
    -   The easiest way to get one is to use:
    
        ```bash
        sudo npm install http-server
        ```
        
        Provided you're set up to use `npm`.
    -   Any web server will do (you just need to be able to load local files
        with http).
-   A text editor or IDE.

## Program structure
You can structure your game however you like, within the usual limits of
JavaScript.

For a simple game, the setup that the Zenva course uses is fine. It has a root
directory for the game (web page) that contains:

-   An `index.html` file defining the page that contains your game.
-   An `assets` directory containing the media required for your game.
-   A `js` directory containing the latest `phaser.js` and a `game.js` file
    that contains your game's code.

### Index.html
A simple HTML page is all you need to host your game, but you might also want
to include instructions or other information for players. Here's a template:

```html
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <title>My Awesome Game</title>
    <style>
      /* 
        The Phaser window is a canvas object.
        Adding this CSS makes sure that it sizes with your browser window.
      */
      canvas {
        width: 100%;
      }
    </style>
</head>
<body>
  <!-- Always include the script at the bottom of the page's body. -->
  <script src="js/phaser.js"></script>
  <script src="js/game.js"></script>
</body>
</html>
```

## Setting up Phaser
To start working with Phaser, you need to:

1.  Define one or more scenes.
2.  Set some configuration details (including the scenes you defined) in an
    object.
3.  Create a Phaser game object using the configuration object.

Here's a simple example:

```javascript
// Create a new scene. Names need to be more specific in multi-scene games.
let gameScene = new Phaser.Scene('Game');

// Define the configuration of the game
let config = {
  type: Phaser.AUTO, // Phaser will use WebGL if available, Canvas if not.
  width: 640,
  height: 360,
  scene: gameScene
};

// Create a new game, pass the configuration
let game = new Phaser.Game(config);
```

<!--
0---|--10|----|--20|----|--30|----|--40|----|--50|----|--60|----|--70|----|--80|
-->

# Sprites

Sprites in Phaser are asociated with scenes.

Here's how you make one (with an image that you've preloaded for the scene):

```javascript
let gameScene = new Phaser.Scene('Game');

// Load assets during scene preload.
gameScene.preload = function(){
  // Load images.
  this.load.image('background', 'assets/background.png');
  this.load.image('player', 'assets/player.png');
};

// The create method gets called once preload is finished.
gameScene.create = function(){
  // Create a background sprite.
  let bg = this.add.sprite(0, 0, 'background');
  
  // Change the origin to the top-left corner.
  bg.setOrigin(0, 0);
```

By default, the origin of a sprite is its center. 


<!--
0---|--10|----|--20|----|--30|----|--40|----|--50|----|--60|----|--70|----|--80|
-->

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
  let background = this.add.sprite(0, 0, 'background').setOrigin(0, 0);
  
  let player = this.add.sprite(0, 0, 'player').setOrigin(0, 0);
  player.depth = 1;
};
```

## Origin

By default, the origin of a sprite is its center.

Use `sprite.setOrigin(0)` to set it to the upper left corner. The parameter
(you can also use two for different X and Y) is a value from 0 to 1, a fraction
of the sprite dimensions.

## Layering

Images and sprites are layered in the order they are added.
    
You can set explicit layer order by using the `depth` property of the
sprite/image ogject, which defaults to 0. Higher values go on top.

## Flipping

Flipping on either axis is a state of the object.

To flip, set `sprite.flipX` or `sprite.flipY` to `true`.

## Rotating

Rotate sprites by either setting the `sprite.angle` property directly or by
calling `sprite.setAngle()`.

Sprites rotate around their origin.

Positive angles are clockwise.

You can also set `sprite.rotation` or call `sprite.setRotation()` to use radians
instead of degrees.


<!--
0---|--10|----|--20|----|--30|----|--40|----|--50|----|--60|----|--70|----|--80|
-->

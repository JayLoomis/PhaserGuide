# Scenes

Each Scene in Phaser is a contained part of your game, like a level.

When you start a scene, it goes through a set lifecycle, using these methods:

-   `init()` is called when the scene is initialized. It isn't always used.
-   `preload()` is called to load all of the assets that you need for the scene.
-   `create()` is called when you're ready to start the scene.
-   `update()` is called every frame.

<!--
0---|--10|----|--20|----|--30|----|--40|----|--50|----|--60|----|--70|----|--80|
-->

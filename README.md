# wInput v1.1.0
 
**wInput** is a simple but also powerful **input management** library for **GameMaker Studio 2.3** that allows you to create actions and assign them to different inputs with ease. It also includes a bunch of other helpful extra features, like detecting double and long presses, and input recording/playback.

[API Reference](https://github.com/MorsGames/wInputAPIReference/wiki) | [itch.io](https://mors-games.itch.io/wInput)

This library is only tested on the Windows, HTML5, and GXC targets, but it should work on other platforms as well. It also comes with an example project that will show you the basics.

Since I made this library primarily for my own personal projects, I will keep updating it on a regular basis.

**This repo only contains the API reference. Head to the itch.io page to get the library itself.**

This library is made by **Mors** ([Website](http://mors-games.com) | [Patreon](https://www.patreon.com/MorsGames)).


## Features
- Support for keyboard, controller, and mouse input.
- Support for multiple players.
- Easy input remapping.
- Detecting double and long presses.
- Detecting the hold time and the last pressed action.
- Mapping analog sticks as digital inputs.
- Getting the input name as a string.
- Input recording and playback.
...and more!


## Basic Usage

```gml
enum key {
    left,
    right,
    up,
    down,
    jump,
}
input_system_init(1);
input_action_add(0, key.left, vk_left, gp_stickll);
input_action_add(0, key.right, vk_right, gp_sticklr);
input_action_add(0, key.up, vk_up, gp_sticklu);
input_action_add(0, key.down, vk_down, gp_stickld);
input_action_add(0, key.jump, ord("Z"), gp_face1);
```

```gml
if (input_check(key.left)) {
    x -= 2;
}
if (input_check(key.right)) {
    x += 2;
}
if (input_check(key.up)) {
    y -= 2;
}
if (input_check(key.down)) {
    y += 2;
}
```

To learn more about how to use this library, check out the [API Reference](https://github.com/MorsGames/wInputAPIReference/wiki).


## Patreon
If you're supporting me on **Patreon** for the $5 tier or higher you will get this library for free. Head to my [Patreon page](https://www.patreon.com/MorsGames) to learn how to get your copy.


## License
This product is licensed under the following terms:
- You are allowed to use and modify this product for both **personal** and **commercial** purposes.
- You are **not** allowed to redistribute this product or any parts of it in any shape or form if the source code is easily accessible.
- I **cannot** be held liable for any claim, damages, or other liabilities that may arise from, out of, or in connection with the product or the use or other dealings in the product.
- I do **not** offer any warranty for this product, and therefore cannot guarantee any kind of official support. That being said, if you end up having any questions I will still try to answer them.
- You're **not** required to give me any credit, you paid for the product after all. That being said, it would still be nice. :)


## Changelog
v1.1.0 (09/11/2021):
- Rebranded the library.
- Added "input_system_set_block_mouse_input_when_unfocused" and "input_system_get_block_mouse_input_when_unfocused", which is enabled by default.
- Added "mouse_in_window".
- Fixed some minor issues with the documentation and comments.
- Optimized the extension better for YYC targets.
- Made use of GameMaker's optional arguments when applicable.
- Fixed a bug that would prevent you from binding multiple gamepad buttons into one action.
  
v1.0.1 (12/03/2021):
- Made some minor changes to the comments and the description.
- Added the [API Reference](https://github.com/MorsGames/wInputAPIReference/wiki).

v1.0.0 (02/10/2020):
- Initial release.

If you have any questions, you can ask them in this project's [itch.io page](https://mors-games.itch.io/wInput).
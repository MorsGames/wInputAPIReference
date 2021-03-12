# WalrusInput v1.0.1
 
**WalrusInput** is a simple but also powerful **input management** library for **GameMaker Studio 2.3+** that allows you to create actions and assign them different inputs them with ease. It also includes a bunch of other helpful extra features, like detecting double and long presses, and input recording/playback.

[API Reference](https://github.com/MorsGames/WalrusInputAPIReference/wiki) | [itch.io](https://mors-games.itch.io/WalrusInput)

The usage of this library is very similar to Javascript's "setInterval()" and "setTimeout()" methods, so if you're familiar with Javascript this will also feel very familiar.

This library is only tested on the Windows and HTML5 targets, but it should work on other platforms as well. It also comes with an example project that will teach you the basics.

This repo only contains the API reference. Head to the itch.io page to get the library itself.


## Features
- Support for keyboard, controller, and mouse input.
- Support for multiple players.
- Easy input remapping.
- Detecting double and long presses.
- Detecting the hold time and the last pressed action.
- Mapping analog sticks as digital input.
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

To learn more about how to use this library, check out the [API Reference](https://github.com/MorsGames/WalrusInputAPIReference/wiki).


## Patreon
If you're supporting me on **Patreon** for the $5 tier or higher you will get this library for free. Head to my [Patreon page](https://www.patreon.com/MorsGames) to learn how to get your copy.


## License
This product is licensed under the following terms:
- You are allowed to use and modify this product for both **personal** and **commercial** purposes.
- You are **not** allowed to redistribute this product or any parts of it in any shape or form if the source code is easily accessible.
- I **cannot** be held liable for any claim, damages, or other liabilities that may arise from, out of, or in connection with the product or the use or other dealings in the product.
- I do **not** offer warranty for this product, and therefore cannot guarantee any kind of official support. That being said, if you end up having any questions I will still try to answer them.
- You're **not** required to give me any credit, you paid for the product after all. That being said, it would still be nice. :)


## Changelog
v1.0.1 (12/03/2021):
- Made some minor changes to the comments and the description.
- Added the [API Reference](https://github.com/MorsGames/WalrusInputAPIReference/wiki).

v1.0.0 (02/10/2020):
- Initial release.
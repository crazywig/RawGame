# RawGame
RawGame is a modern C# game framework that allows you to make 2D games that can target any platform that modern C# is supported on. RawGame itself has no dependencies and never will, so it can easily be bundled into your existing C# project or used as a DLL. RawGame uses a plugin based architecture to keep any platform dependent code out of the main codebase and out of your game.

Plugins are needed to make use of most of RawGame's features and plugins for sound, graphics and input are available for the common systems. They are also relatively easy to develop due to RawGame itself managing as many aspects of the engines that are not platform dependent. This means you will get more reliable results on all platforms.

A big advantage of this plugin system is that you can choose what sound backend to use, what graphics to use, what input to use without changing any of your code base. At run time you can choose the backend you want to use which will give you the ability to work around bugs that may exist in OpenGL/DirectX/Sound drivers on your users systems. Your game will not care whether it is running on MacOS, Windows or an Android phone.

By using RawGame you can remove any platform dependent code from your own codebase which will allow you to concentrate purely on making your game be available on as many systems as possible. It also means if you only want to use a subset of RawGame there will be no overhead in the things you don't use because they simply won't be loaded.

## 2D Rendering
- Vulkan and OpenGL supported currently through a Veldrid plugin.
- Supports scaling, rotation, texturing, depth testing, tinting, linear and point sampling.
- Can draw millions of differently textured, scaled, rotated, etc quads in a single draw call
- Texture switching and sampling changes are "Free" and have no impact on performance
- Supports custom shaders to apply further effects
- Efficient and modern, only 32 bytes per quad and uses geometry shader to create quads from points. Nearly all the work is done on the GPU

## Sound
- DirectSound and OpenAL plugins currently available
- No limit on number of simultaneous sounds playing
- Unique volume and panning for each sound instance
- Mixing is done in RawGame and not in the backends, giving a more consistent performance and sound across all platforms
- Very low overhead per sound instance
- Sound is mixed as 32bit floats in a separate thread
- Supports different output samplerates and 16/32 bit samples
- Streaming support with Ogg already done

## Input
- Joysticks and gamepads supported
- Multiple keyboard and mouse supported internally (backends often only support a single mouse and keyboard though)
- Integer identification system allows easy mapping of input

## Utilities
- PNG/JPG image decoders
- WAV/Ogg sound decoders
- Game related math helpers
- BMFont loader

## Examples
[![RawGame 1 million quads](http://img.youtube.com/vi/0ewft5baBkY/0.jpg)](https://www.youtube.com/watch?v=0ewft5baBkY "1 million quads")

## Current system requirements
- Graphics: Vulkan or OpenGL v3.30 or higher
- Sound: DirectSound and OpenAL make most platforms viable
- Input: Currently relying on SDL2 through Veldrid so supports most platforms


## Philosophy
RawGame is designed to facilitate easier development of games using a modern and efficient system that can work on many different platforms. C# is an easy to use programming language that still offers very good performance. Combined with a multiplatform framework like RawGame it will allow developers to target many platforms with a single codebase and get a consistent look, feel and performance across them all.

Another big focus for RawGame is performance. 

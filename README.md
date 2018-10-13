# RawGame
Modern C# 2D Game Framework
RawGame is a pure C# modern framework that allows you to make 2D games that can target many platforms. RawGame itself has no dependencies and can easily be bundled into your existing C# project or be used as a DLL.

RawGame uses a plugin based architecture to keep any platform dependent code out of the main codebase. Anywhere C# can run RawGame can run, however plugins would need to be available to make use of most of RawGame's features. Plugins for sound, graphics and input are available for the common systems and are relatively easy to develop due to RawGame itself managing as many aspects of the engines that are not platform dependent. This means you will get more reliable results on all platforms.

A big advantage of this plugin system is that you can choose what sound backend to use, what graphics to use, what input to use without changing any of your code base. At run time you can choose the backend you want to use which will give you the ability to work around bugs that may exist in OpenGL/DirectX/Sound drivers on your users systems. By using RawGame you can remove any platform dependent code from your own codebase which will allow you to concentrate purely on making your game be available on as many systems as possible.

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
- Volume and Panning
- Mixing is done in RawGame and not in the backends, giving a more consistent performance and sound across all platforms
- Very low overhead per sound instance
- Sound is mixed as 32bit floats in a separate thread
- Supports different output samplerates and 16/32 bit samples

## Music
- Ogg streaming

## Input
- Joysticks and gamepads supported
- Multiple keyboard and mouse supported internally (backends often only support a single mouse and keyboard though)
- Integer identification system allows easy mapping of input

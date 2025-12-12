# Mode Development

Text Forge have a powerful and feature rich API to add support for any language in the fastest way. We provide modes to
help developers and users work with any file just with plug one module. In this page, we will show a standard way for
mode development to you and best practices.

!!! Note
    
    Reading [Modes Guide](modes.md) is highly recommended before develop modes, please read that document before this.

## Text Forge Mode API

To handle external modules we need an API, so we provide **Text Forge Mode API** (TFM API in short) as modes' connection
way. TFM is a feature packed API for any mode, so it have a lot of features.

!!! Note

    We have multiple versions of TFM API, and each editor version just supports one TFM API version (but a TFM API 
    version can be shared between a lot of editor versions). Currently, the latest stable TFM API version is 2.2,
    and it supports Text Forge 0.2-stable and newer versions.

To use all features of modes, you should know about its API, so we will explain it a little more. TFM API consists of 
two parts, the first part is in EditorAPI that connect editor to modes, the second part is the `TextForgeMode` class, 
which keeps this connection standard and provides some ready-made features.

You will work with **TextForgeMode** to complete your mode, this will define your mode and EditorAPI will do the rest.
So a mode have a very important part, its script. This script extends TextForgeMode class and customizes behaviors to 
provide your mode logic.

## Make your first mode with template

We provide a mode template to help mode developers, specially for first time testing. You can find it [here](https://github.com/text-forge/mode-template), 
you can download, clone or fork it to have a simple initialization, you can find guides in template.

## Useful examples

You can see our official modes like [Web Mode Kit](https://github.com/text-forge/web-mode-kit) and 
[GDScript Mode](https://github.com/text-forge/gdscript-mode) to find solutions for most important challenges.
AGS-wrapper-string-size
=======================

> [AutoIt Gui Skeleton](https://autoit-gui-skeleton.github.io/) package for wrapping the library [StringSize.au3](https://www.autoitscript.com/forum/topic/148114-a-non-strict-json-udf-jsmn/) created by Melba23 (thanks to tranxexx for the default DC code). See this package on [npmjs.com](https://www.npmjs.com/package/@autoit-gui-skeleton/ags-wrapper-string-size/)



<br/>

## StringSize

The StringSize library takes a text string and calculates the size of label required to hold it as well as formatting the string to fit.

```autoit
Local $stringSize = _StringSize($text, $fontsize, $fontweight, $fontattribute, $fontfamily, $GUI_width - $marginLeftRight*2)

If(Not @error) Then
      $label_TEXT_reformated = $stringSize[0]
      $label_WIDTH_calculated = $stringSize[2] ; ($stringSize[2] / $dpi)
      $label_HEIGHT_calculated = $stringSize[3] ; ($stringSize[3] / $dpi)
    
      GUISetFont($fontsize, $fontweight, $fontattribute, $fontfamily)
      GUICtrlSetData($label_ID, $label_TEXT_reformated)
      GUICtrlSetPos($label_ID, $marginLeftRight, $top, $label_WIDTH_calculated, $label_HEIGHT_calculated)
EndIf
```

<br/>

## How to install AGS-wrapper-wrapper-string-size ?

We assume that you have already install [Node.js](https://nodejs.org/) and [Yarn](https://yarnpkg.com/lang/en/), for example by taking a [Chocolatey](https://chocolatey.org/). AGS framework use Yarn for manage dependencies.

To add this package into your AutoIt project, just type in the root folder of your AGS project where the `package.json` is stored. You can also modify the `dependencies` property of this json file and use the yarn [install](https://yarnpkg.com/en/docs/usage) command. It is easier to use the add command :

```
λ  yarn add @autoit-gui-skeleton/ags-wrapper-string-size --modules-folder vendor
```

The property `dependencies` of the  `package.json` file is updated consequently, and all package dependencies, as well as daughter dependencies of parent dependencies, are installed in the `./vendor/@autoit-gui-skeleton/` directory. Note that with an AGS project, it is not necessary to explicitly write this option `--modules-folder vendor` on the command line, thanks to the `.yarnrc` file stored at the root of the project. Yarn automatically use `.yarnrc` file to add an additional configuration of options.

```
 #./.yarnrc
 --modules-folder vendor
 ```

Finally to use this library in your AutoIt program, you need to include this library in the main program. There is no need for additional configuration to use it.

```autoit
#include './vendor/@autoit-gui-skeleton/ags-wrapper-string-size/StringSize.au3'
```



<br/>

## What is AGS (AutoIt Gui Skeleton) ?

[AutoIt Gui Skeleton](https://autoit-gui-skeleton.github.io/) give an environment for developers, that makes it easy to build AutoIt applications. To do this AGS proposes to use conventions and a standardized architecture in order to simplify the code organization, and thus its maintainability. It also gives tools to help developers in recurring tasks specific to software engineering.

> More information about [AGS framework](https://autoit-gui-skeleton.github.io/)

AGS provides a dependency manager for AutoIt library. It uses the Node.js ecosystem and its dependency manager npm and its evolution Yarn. All AGS packages are hosted in npmjs.org repository belong to the [@autoit-gui-skeleton](https://www.npmjs.com/search?q=autoit-gui-skeleton) organization. And in AGS you can find two types of package :

- An **AGS-component** is an AutoIt library, that you can easy use in your AutoIt project built with the AGS framework. It provides some features for application that can be implement without painless.
- An **AGS-wrapper** is a simple wrapper for an another library created by another team/developer.

> More information about [dependency manager for AutoIt in AGS](https://autoit-gui-skeleton.github.io//2018/07/10/ags_dependencies_manager_for_AutoIt.html)


<br/>

## About

### Acknowledgments

Acknowledgments for [Melba23](https://www.autoitscript.com/forum/topic/114034-stringsize-m23-new-version-16-aug-11/) work and its library StringSize.au3.


### Contributing

Comments, pull-request & stars are always welcome !

### License

Copyright (c) 2018 by [v20100v](https://github.com/v20100v). Released under the MIT license.

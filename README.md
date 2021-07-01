<br>
<br>
<br>
<br>
<br>
<br>
<div align=center>
<a href="https://github.com/dyrdadev/first-person-controller-for-unit">
    <img src="./Media/icon.png" alt="An icon of the first person controller for unity project." width="148px"/>
</a>
</div>
<h6 align=center>
    First-Person Controller <br/> for Unity
</h6>
<br>
<br>
<br>
<br>
<br>
<br>

# First-Person Controller for Unity

> A First-Person Controller for Unity.

> 🧪 **EXPERIMENTAL** This project is experimental. It is still under development. It may be unstable. It is not optimized and largely untested . Do **not** use this project in critical projects.

This package includes a First-Person Controller for Unity. Check out the [Features](#features) section for a detailed list of all features of the controller. The footage below shows the open-source sample project ["Mapper's Peak"](https://github.com/dyrdadev/mappers-peak) using the First-Person Controller.

<p align=center>
    <br>
    <br>
    <a href="https://github.com/dyrdadev/first-person-controller-for-unity">
        <img src="./Media/first_person_controller_github_preview.gif" alt="Gameplay footage from the 'Mapper's Peak' sample project using the First-Person Controller"/>
    </a>
    <br>
    <br>
</p>

## Quick Start

1. **Install the First Person Controller:** Install this package as described [below](#install-the-package).
2. **Install UniRx:** The package depends on [UniRx](https://github.com/neuecc/UniRx). Unfortunately, this dependency cannot be included automatically. The reason is described below in the ["Special Dependencies"](#unirx) section. You have to include UniRx in your project. UniRx is available [via Asset Store](https://assetstore.unity.com/packages/tools/integration/unirx-reactive-extensions-for-unity-17276) or you can include it [as UPM package](https://github.com/neuecc/UniRx#upm-package).
3. **Update to Unity's new Input System** This package uses Unity's [Input System](https://docs.unity3d.com/2020.2/Documentation/Manual/com.unity.inputsystem.html) package. When asked from Unity, update to Unity's new Input System. Alternatively, you can implement your own ```FirstPersonControllerInput``` class and ignore the existing PlayerInput folder.
4. **Explore your scene:** Add the "FirstPersonPlayer" prefab from the package to your scene. Now you can explore your scene with the First-Person Controller.

## Special Dependencies

## UniRx

The controller depends on UniRx. UniRx is the implementation of ReactiveX for Unity. Unfortunately, it is not possible to add it as dependency because Unity doesn’t support Git URLs for indirect dependencies. UniRx has to be installed manually in your project that uses the First Person Controller.

If you want to learn UniRx to extend the controller or use it for other components, I recommend you the tutorial series ["ReactiveX and Unity3D"](https://ornithoptergames.com/reactiverx-in-unity3d-part-1/) by Tyler Coles. Also check out the official material of [UniRx](https://github.com/neuecc/UniRx) and [ReactiveX](http://reactivex.io/).

## Input System Package

The project includes player input and uses Unity's new [Input System Package](https://docs.unity3d.com/2020.2/Documentation/Manual/com.unity.inputsystem.html). The new system replaces the classic input system with the Input Manager in ```UnityEngine.Input```. On import, Unity asks you if your project should be updated to the new Input System. If you need the ```UnityEngine.Input``` input system, you can set the "Active Input Handling" option in the Player settings (Project Settings -> Player -> Other Settings) to ```Both```. Then you can use the new Input System Package System and the old Input Manager with the ```UnityEngine.Input``` class.

If you do not want to switch to the new input system, you can implement your own ```FirstPersonControllerInput``` class that uses the input system of your choice.

## Features

### Support of Various Input Devices

The First-Person Controller supports a mouse + keyboard input scheme and a gamepad input scheme. You can edit the input schemes and add new ones in the "FirstPersonInputAction" Input Action Asset. Check out the [manual](https://docs.unity3d.com/2020.2/Documentation/Manual/com.unity.inputsystem.html) of the Input System for further information.

### Full Locomotion

The First-Person Controller implements physics based locomotion so you can move around, and run, and jump.

### Character Effects

The controller implements a ```ICharacterSignals``` interface for character effects such as character audio or camera effects. The interface offers you an easy way to implement your own effects. The package includes the following effects, which are already implemented:

#### Head Bob

The package includes an optional head bob effect for walking and running. The effect moves the camera slightly up and down to simulate the movement.

#### Sound Effects

The package includes an optional component for sound effects of the character.

## Install the Package

You can install this package with unity's [package manager](https://docs.unity3d.com/Manual/PackagesList.html).

### Install the Package from a Git URL

You can install the package using a Git URL. This is possible for direct dependencies of a project specified in its ```manifest.json```. Add a new package with the git-HTTPS URL to the version you want to install in the form ``https://github.com/dyrdadev/first-person-controller-for-unity.git#{version}``, where {version} is the actual version of the release you want to install. For example, if you want to install version "0.0.3" of this package, you can refer to ``https://github.com/dyrdadev/first-person-controller-for-unity.git#0.0.3``.

You can do this by using the Package Manager window or the manifest.json directly:

1. **Installing from a Git URL using the Package Manager window.** Open the Package Manager window. Click "+", then "Add package from git URL" and enter the git URL from above. You can find more information [here](https://docs.unity3d.com/Manual/upm-ui-giturl.html).
2. **Installing from a Git URL using the manifest.json.** You can add a new entry to the manifest.json file in the ``Packages`` folder of your unity project: ```"dev.dyrda.first-person-controller": "https://github.com/dyrdadev/first-person-controller-for-unity.git#0.0.3"```. You can find more information [here](https://docs.unity3d.com/Manual/upm-git.html).

## License

This package is licensed under a MIT license. See the [LICENSE](/LICENSE.md) file for details.

## Support & Contribute

This project was created by [Daniel Dyrda](https://dyrda.io).

> Daniel: _If you want to support me and my projects, you can follow me on [github (dyrdadev)](https://github.com/dyrdadev) and [twitter (@daniel_dyrda)](https://twitter.com/daniel_dyrda). Just come by and say hello, I would love to hear how you use the project._

If you want to contribute to this project, you are welcome to do so. Just write me and we will find a way to collaborate.

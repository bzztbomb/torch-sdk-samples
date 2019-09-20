
# TorchKit Sample Application - Project Chooser

## Modifications

This is a modified version of the sample project to skip setting an anchor and allow a tracked image to start up a project.  The torch project was set up this way to allow this to happen:

1. Create a blank scene as the first scene.
2. Create a second scene with your content to display when a tracked image has been detected.
3. Touch the Scene Pill.
4. Touch `Tracked Images`, set up a tracked image.
5. Touch `Interactions` (from the scene menu).
6. Touch `Add Interaction`.
7. Touch `Image Found`.
8. Touch the tracked image set up in step 4.
9. Touch `Action Response`
10. Touch `Scene Change`
11. Touch the scene created in step 2.
12. Exit out of the interaction drawer, test this in play mode.
13. Once that works, export the project and use it in this SDK example.

## Original README below.

This is a simple example of how to load and unload Torch projects inside of a Swift based iOS application.  It could be the basis of a product catalog application with AR preview, or a chapter based training application with different Torch projects mapping to different tasks.

## Features

* Loads and displays multiple Torch projects.
* Has simple project anchoring.
* It gracefully handles devices that do not support ARKit by not allowing them to view the project.

## Project overview

1. In `AppDelegate.swift` we initialize and shutdown the TorchSDK.
2. In `ProjectGalleryViewController.swift` we display the project list and launch a `TorchProjectViewer` view controller to display the selected project.
3. `TorchProjectViewer.swift` is meant to be a template for displaying/executing Torch projects.
4. `WorldAnchorManager.swift` is a simple example strategy for setting a world anchor for the Torch project.

## Notes on building/running

1. Be sure to run `pod install` in the sample directory to download and install the TorchKit pod.
2. Login to the Torch dashboard and [generate an API key](https://home.torch.app/account/api)
3. Open `AppDelegate.swift` and replace the API key in this line: `TorchKit.shared.initSDK(apiKey: "INSERT API KEY HERE")`
4. Update the `Signing Settings` under `Build Settings` to use your Apple account.
5. Run the sample application on a device.

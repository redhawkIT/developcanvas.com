---
title: Basic Cameras
template: tutorial-page.tmpl.html
position: 3
---

## Camera Entities

To view the scene created by your PlayCanvas application a Camera Entity is used to render it to the screen.

In order to run your Pack from the PlayCanvas Designer, you must add at least one active Camera Entity to your Pack.

## Creating a Camera Entity

To create a new Camera Entity, you need to add a Camera [Component][component] to an Entity.

* Select the root Entity of your Pack in the Entity Explorer
* Create a new Entity by selecting *New Entity* from the *Entity* menu.
* Add a Component by selecting *New Component* from *Component* menu
* Choose *Camera* when you are prompted to choose which type of Component to create

As making a Camera Entity is a common task there is a shortcut: Select *Create Camera Entity* in the *Entity* menu.
This is equivalent to creating a new Entity and adding a Camera Component to it.

## Camera Properties

Like all Components, the Camera Component has a set of properties which alter it's behaviour.

### `fov`

The field of view of a camera determines how much of the scene the camera shows. It is measured in degrees (°) so the default value of 45° means that the top edge of the view to the bottom edge of the view form an arc of 45° from the position of the camera

![Field of view](/images/platform/field_of_view.png)

You can see in this diagram that because the `fov` value is independent of the width of the display a wide screen view (light blue) shows the same amount vertically but more horizontally than a narrow screen view (dark blue).

### `nearClip`

The near clipping distance is the distance, in metres, from the camera before which nothing will be drawn.

### `farClip`

The far clipping distance is the distance, in metres, from the camera after which nothing will be drawn.

### `projection`

The projection type determines which type of matrix projection is used to convert the 3D scene in to the 2D view rendered to the page.

The **perspective** projection is the most common type for games. Alternatively, you can use an **orthographic** projection, which renders the scene without perspective so is useful for design-type applications.

### `activate`

If the activate property is true, then the camera will be set as the current camera when the Pack loads. Note that usually only one camera can be active at a time. If more than one camera has the activate property set to true, which camera is active at start time is undefined.


[component]: /user-manual/glossary#component
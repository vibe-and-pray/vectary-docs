# February 2026



### February 20



{% tabs %}
{% tab title="Improvements" %}
{% hint style="success" %}
### February 20



* Improved [**Boolean**](../documentation/design-process/design-mode/modifiers/boolean.md) modifier: now supports animations and dynamic changes in the viewer
* Added new `Projection` type for applying [**Decals**](../documentation/design-process/decals.md) to objects
* Added support for importing `WebP` format
{% endhint %}
{% endtab %}

{% tab title="Bug fixes" %}
{% hint style="success" %}
### February 20



* Fixed issue where [background](../documentation/design-process/background.md) color was not updating instantly when changed via [variable](../documentation/3d-configurator/variables-and-expressions/)
* Fixed issue where [interaction prompt](../documentation/project-settings/interaction-prompt.md) was visible when switching to [WebXR](../documentation/project-settings/webxr-beta.md) experience
* Fixed bug where [Material](../documentation/3d-configurator/floating-ui/materials-ui.md) element (Floating UI) became unresponsive to clicks in some cases
* Fixed issue where mask remained in [Opacity](../documentation/design-process/materials-and-textures/basic-materials/opacity.md) property after deleting texture in `Mask` mode
* Fixed issue where texture resolution changes were not applied after project reload in some situations
* Fixed issue causing texture size to increase when importing texture into [Normal map](../documentation/design-process/materials-and-textures/basic-materials/normal-map.md) property
{% endhint %}
{% endtab %}

{% tab title="Details" %}
{% hint style="info" %}
#### Improved Boolean



* Previously, [**Boolean**](../documentation/design-process/design-mode/modifiers/boolean.md) modifiers were baked on export, which meant any dynamic changes (animations, show/hide, transforms) simply wouldn't work with Boolean geometry in the viewer. Now Booleans stay live, so you can animate them, toggle visibility, and apply transformations just like any other object. No more baking, no more limitations!
{% endhint %}

{% hint style="info" %}
#### Projected Decals



* We added a new `Projection` type for [**Decals**](../documentation/design-process/decals.md) - an alternative to the default wrapping method that projects the texture straight onto the surface. Try both and see which works better for your specific geometry.
{% endhint %}
{% endtab %}
{% endtabs %}





### February 3



{% tabs %}
{% tab title="New features" %}
{% hint style="success" %}
### February 3



* Added new Floating UI element – [**Color**](../documentation/3d-configurator/floating-ui/color.md)
* Added new `Color` parameter for [**Input**](../documentation/3d-configurator/floating-ui/input.md#color-input-example)
{% endhint %}
{% endtab %}

{% tab title="Details" %}
{% hint style="info" %}
#### Color Palette for Floating UI!



* This release adds support for a Color Palette in configurators, enabling interactive color selection in scenes. Colors can now be chosen not only from predefined options but also defined freely.\
  More details here: [color.md](../documentation/3d-configurator/floating-ui/color.md "mention")
{% endhint %}
{% endtab %}
{% endtabs %}




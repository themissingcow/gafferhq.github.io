---
layout: post
title: "Shader Connection Components"
subtitle: "Tip of the Day"
icon: /resources/images/2019-02-12-tip-shader-connection-components/splash-shader-connection-components.png
---

When building shader networks, you can split a multi-value parameter in the ''Graph Editor'', to mix and match its individual components. 

<!-- Add an image path macro for implicit page-based file paths -->
{% assign post-directory = page.path | remove: '_posts/' | remove: '.md' %}
{% assign images = site.images | append: "/" | append: post-directory %}

### Expanding Parameter Components ###
A multi-value parameter, such as a color, can have its plug expanded into component child plugs: right-click the plug, then select ''Expand RGB Components''. Then, you can freely manipulate each channel, and, for example, swizzle colors:

![Swizzling shader components.]({{ images }}/swizzling-shader-componentsAnimation.gif)

### Collapsing Components ###
Once a parameter plug has been expanded, you can collapse it back into a single plug: right-click one of the component plugs, then select ''Collapse RGB Components''. If you collapse components that are connected, they will appear as green auxiliary connections:

![Collapsing shader components.]({{ images }}/collapsing-shader-componentsAnimation.gif)

### Multi-value to Single-value Parameters ###
When connecting a multi-value parameter to a single-value parameter, a context menu will automatically open, letting you choose which component to use for the input:

![Expanding shader components.]({{ images }}/expanding-shader-componentsAnimation.gif)

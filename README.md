# Grav Page Loader Plugin

**Page Loader** is a [Grav](http://github.com/getgrav/grav) plugin that adds a simple loader animation on loading page.

#### Available Animations

* Round Pulse
* Round Bounce
* Bounce Dot
* Spin Big Dot
* Rotate Cube
* Rotate Double Cube

# Manual installation

Download the latest [release](https://github.com/StellarisStudio/grav-plugin-pageloader/releases)  of this repository, unzip to `/your-grav/user/plugins` and rename the folder to `pageloader`.

# Configuration and Usage

Simply go to the plugin settings from the [Admin Panel](https://github.com/getgrav/grav-plugin-admin).. Or copy the `pageloader.yaml` file, which contains the settings, into your `user/config/plugins` folder and make your modifications.

`enabled:` which turns the plugin on/off. _(default: true)_<br>
`built_in_css:` which activate the default plugin CSS. _(default: true)_<br>
`select_anime:` choose between the animations. _(default: round_pulse)_<br>
Available : `round_pulse`, `round_bounce`, `bounce_dot`, `spin_bdot`, `rotate_cube`, `rotate_dcube`<br>
`fadeout:` which define the duration of the loader fade out. _(default: 1500)_

Place the following lines of code in the `base.html.twig` file of your theme, just below the `body` tag:
```twig
{# PRE-LOADER #}
{% if config.plugins.pageloader.enabled %}
  {% include 'partials/pageloader.html.twig' %}
{% endif %}
```

# ToDo list

* Add some animations... _**(In progress)**_

# License

MIT license. See [LICENSE](LICENSE)

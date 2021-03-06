<p align="center">
  <img src="https://dl.dropboxusercontent.com/u/26678671/haxeui2-warning.png"/>
</p>

<h2>haxeui-openfl</h2>
`haxeui-openfl` is the `OpenFL` backend for haxeui.

<h2>Installation</h2>
`haxeui-openfl` has a dependency to <a href="https://github.com/haxeui/haxeui-core">`haxeui-core`</a>, and so that too must be installed.

Eventually all these libs will become haxelibs, however, currently in their alpha form they dont even contain a `haxelib.json` file (for dependencies, etc) and therefore can only be used by downloading the source and using the `haxelib dev` command or by directly using the git versions using the `haxelib git` command (recommended). Eg:

```
haxelib git haxeui-core https://github.com/haxeui/haxeui-core
haxelib dev haxeui-openfl path/to/expanded/source/archive
```

<h2>Usage</h2>
The simplest method to create a new `OpenFL` application that is haxeui ready is simply to use one of the <a href="https://github.com/haxeui/haxeui-templates">haxeui-templates</a>. These templates will allow you to start a new project rapidly with haxeui support baked in. 

If however you already have an existing application, then incorporating haxeui into that application is straight forward:

<h3>project/application.xml</h3>
Assuming `haxeui-core` and `haxeui-openfl` have been installed then adding haxeui to your existing application is  as simple as adding these two lines to your `project.xml` or your `application.xml`:

```xml
<haxelib name="haxeui-core" />
<haxelib name="haxeui-openfl" />
```

_Note: Currently you must also include `haxeui-core` explicitly during the alpha, eventually `haxelib.json` files will exist to take care of this dependency automatically._ 

<h3>Toolkit initialisation and usage</h3>
Initialising the toolkit is very simple, simply add this line somewhere _before_ you start to actually use haxeui in your application:

```
Toolkit.init();
```
Once the toolkit is initialised you can add components using the methods specified <a href="https://github.com/haxeui/haxeui-core#adding-components-using-haxe-code">here</a>.

<h2>OpenFL specifics</h2>

 * As well as using the generic `Screen.instance.addComponent` it is also possible to simply add components directly to any other `OpenFL` sprite (eg: `Lib.current.stage.addChild`)

<h2>Addtional resources</h2>
* <a href="http://haxeui.github.io/haxeui-api/">haxeui-api</a> - The haxeui api docs.
* <a href="https://github.com/haxeui/haxeui-guides">haxeui-guides</a> - Set of guides to working with haxeui and backends.
* <a href="https://github.com/haxeui/haxeui-demo">haxeui-demo</a> - Demo application written using haxeui.
* <a href="https://github.com/haxeui/haxeui-templates">haxeui-templates</a> - Set of templates for IDE's to allow quick project creation.
* <a href="https://github.com/haxeui/haxeui-bdd">haxeui-bdd</a> - A behaviour driven development engine written specifically for haxeui (uses <a href="https://github.com/haxeui/haxe-bdd">haxe-bdd</a> which is a gherkin/cucumber inspired project).
* <a href="https://www.youtube.com/watch?v=L8J8qrR2VSg&feature=youtu.be">WWX2016 presentation</a> - A presentation given at WWX2016 regarding haxeui.


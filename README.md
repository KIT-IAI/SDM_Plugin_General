# PlugIn Repository for KITModelViewer
KITModelViewer has a plugin mechanism that allows you to develop your own extensions.
Two plug-ins are already included in the download archive of the KITModelViewer. One is the very simple "Hello World" example that shows the basic functionality of the plugin API and how to use it to access the internal database. The second plugin provides a simple Python API and allows you to create your own Python scripts that will be executed directly within the KITModelViewer.
## 


[PlugIn Template](https://github.com/KIT-IAI/SDM_Plugin_Template) (publicly available soon)

[Hello World](https://github.com/KIT-IAI/SDM_Plugin_HelloWorld) (publicly available soon)

[Python API PlugIn](https://github.com/KIT-IAI/SDM_Plugin_Python) (publicly available soon)

[Papermodel Generator](https://github.com/KIT-IAI/SDM_Plugin_Papermodel) (publicly available soon)


## PlugIn Features

### Document Feature

* Provide full access to the internal IfcDB population of the active document.

### LiveLog Feature

* Enables the output of messages in the LiveLog Toolbar of the application.

### Message Dialog Feature

* Allows to use a standard dialog of the application to output messages.

### Renderer Feature

* Allows to create ScreenShots of the scene from a plugin.

### Idel Feature

* The Idle feature is needed to use custom UI frameworks like wxWidgets in a plugin.

### File Save Feature

* Allows saving objects from the PlugIn in different graphic formats such as OBJ, 3DS or STL.

### Color Coding Feature

* The ColorCoding feature can be used to control the coloring of objects in the scene.

# PlugIn Repository for KITModelViewer
KITModelViewer has a plugin mechanism that allows you to develop your own extensions.
Two plug-ins are already included in the download archive of the KITModelViewer. One is the very simple "Hello World" example that shows the basic functionality of the plugin API and how to use it to access the internal database. The second plugin provides a simple Python API and allows you to create your own Python scripts that will be executed directly within the KITModelViewer.

[Hello World](https://github.com/KIT-IAI/SDM_Plugin_HelloWorld)

[Python API PlugIn](https://github.com/KIT-IAI/SDM_Plugin_Python)

[Papermodel Generator](https://github.com/KIT-IAI/SDM_Plugin_Papermodel) (publicly available soon)

[Glaser Calc](https://github.com/KIT-IAI/SDM_Plugin_GlaserCalc)

[Print 3D Model](https://github.com/KIT-IAI/SDM_Plugin_Print3DModel)

[EnergyADE Enrichment](https://github.com/KIT-IAI/SDM_Plugin_EnergyADE_Enrichment) (coming soon)

[IfcTruss](https://github.com/KIT-IAI/SDM_Plugin_IfcTruss) (coming soon)

## PlugIn Features

A plugin has multiple features that are used to communicate with the host application. 

### DocumentFeature

The ``DocumentFeature`` provides full access to the internal IfcDB population of the active document and a mechanism to notify the host application when changes occur.

Example:

```c++
class PluginWithDocumentObserver : public Plugin
{
public:
    PluginWithDocumentObserver()
    {
        // when the document (IfcDB) changes, the lambda is called
        m_documentObServer.attach([&](IfcDB::Populationi* db)
        {
            // the db is forwarded to another feature in the same plugin
            m_anotherFeature.setDb(db);
        });
    }
    
private:
    DocumentObserverImpl m_documentObserver;
    AnotherFeature m_anotherFeature;
};
```

### LiveLogFeature

The ``LiveLogFeature`` enables the output of messages in the LiveLog Toolbar of the application.

### MessageDialogFeature

The ``MessageDialogFeature`` shows a message dialog in the host application.

### RendererFeature

The ``RendererFeature`` allows to create screenshots of the scene from a plugin.

### IdleFeature

The ``IdleFeature`` provides a callback to the plugin from the host application's message loop. This callback may e.g. be used to feed the message loop of a UI library 

### FileSaveFeature

The ``FileSaveFeature`` triggers the host application so save objects in different graphic formats (e.g. OBJ, 3DS or STL).

### ColorCodingFeature

The ``ColorCodingFeature`` can be used to control the coloring of objects in the scene.

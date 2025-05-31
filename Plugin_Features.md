## Plugin Features

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

### ProgressBarFeature

The ``ProgressBarFeature`` shows a progress bar in the applications status bar.

### RendererFeature

The ``RendererFeature`` allows to create screenshots of the scene from a plugin.

### IdleFeature

The ``IdleFeature`` provides a callback to the plugin from the host application's message loop. This callback may e.g. be used to feed the message loop of a UI library 

### FileSaveFeature

The ``FileSaveFeature`` triggers the host application so save objects in different graphic formats (e.g. OBJ, 3DS or STL).

### ColorCodingFeature

The ``ColorCodingFeature`` can be used to control the coloring of objects in the scene.

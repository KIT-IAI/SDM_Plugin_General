# Plugin Repository for KITModelViewer
[KITModelViewer](https://github.com/KIT-IAI/SDM_KITModelViewer) has a plugin mechanism that allows the development of own extensions.
Two plugins are already included in the download archive of the KITModelViewer. One is the very simple "Hello World" example that shows the basic functionality of the plugin API and how to use it to access the internal database. The second plugin provides a simple Python API and allows to create own Python scripts that will be executed directly within the KITModelViewer.

Here you will find the [Plugin Feature Doucumentation](Plugin_Features.md)

## Overview of Plugins developed at IAI-SDM

| Plugin Name          | Description                                |
| :---                 | :---                                       |
| [Hello World](https://github.com/KIT-IAI/SDM_Plugin_HelloWorld) | Simple "Hello World" example for getting started with KITModelViewer plugin development |
| [Python API Plugin](https://github.com/KIT-IAI/SDM_Plugin_Python) | Plugin that provides a python API for the KITModelViewer |
| [Papermodel Generator](https://github.com/KIT-IAI/SDM_Plugin_Papermodel) | Generation of paper models for individual CityGML buildings |
| [Glaser Calc](https://github.com/KIT-IAI/SDM_Plugin_GlaserCalc) | Calculation of the Glaser diagram for individual IFC building elements |
| [Print 3D Model](https://github.com/KIT-IAI/SDM_Plugin_Print3DModel) | Preparation and checking of IFC models for 3D printing |
| [EnergyADE Enrichment](https://github.com/KIT-IAI/SDM_Plugin_EnergyADE_Enrichment) <br>(coming soon)| Enrichment of CityGML building models for thermal simulation through the use of EnergyADE |
| [IfcTruss](https://github.com/KIT-IAI/SDM_Plugin_IfcTruss) | Python plugin for the calculation of trusses based on IFC structural analysis elements |
| [OSM BuildingCreator LoD1](https://github.com/KIT-IAI/SDM_Plugin_OSM_BuildingCreator_LoD1) | Creating 3D CityGML buildings based on OpenStreetMap (OSM) |
| [OSM BuildingCreator LoD2](https://github.com/KIT-IAI/SDM_Plugin_OSM_BuildingCreator_LoD2) <br>(coming soon)| Creating 3D CityGML buildings based on OpenStreetMap (OSM) |
| [ETHOS.BUILDA BuildingCreator](https://github.com/KIT-IAI/SDM_Plugin_ETHOS-BUILDA-BuildingCreator) | Creating 3D CityGML buildings based on [ETHOS.BUILDA](https://ethos-builda.fz-juelich.de/api/v8_20240916/swagger/) |
| [GlobalBuildingAtlas BuildingCreator](https://github.com/KIT-IAI/SDM_Plugin_GlobalBuildingAtlas-BuildingCreator) | Creating 3D CityGML buildings based on [GlobalBuildingAtlas](https://github.com/zhu-xlab/GlobalBuildingAtlas) |
| [Google 3D Tiles](https://github.com/KIT-IAI/SDM_Plugin_3DTiles)<br>(coming soon)| Plugin for integrating Google Maps 3D Tiles |
| [PolyVR](https://github.com/KIT-IAI/SDM_Plugin_polyvr_client)<br>(coming soon)| Plugin for connecting to the scene authoring system [PolyVR](https://github.com/Victor-Haefner/polyvr) |

## Plugin installation

KITModelViewer plugins available on GitHub can be downloaded as a zip archive in the corresponding GitHub project.
In the main menu, under Plugin, there is a menu item for installing plugins. For manual installation, copy the complete folder within the plugin archive into the “plugins” folder of the KITModelViewer directory.

## Plugin developement
Two APIs are available for the KITModelViewer. One is a [Python API](https://github.com/KIT-IAI/SDM_Plugin_Python) for the rapid development of compact scripts to evaluate the imported data or for the development of more complex Python plugins with integration of external modules. The Python Plugin is available as open source and is realized as a plugin based on the C++ plugin SDK.
For more experienced developers with C++ knowledge, a [plugin SDK](https://github.com/KIT-IAI/SDM_Plugin_SDK) is available that provides full access to the internal data structures and functionalities.

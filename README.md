# PlugIn Repository for KITModelViewer
KITModelViewer has a plugin mechanism that allows you to develop your own extensions.
Two plug-ins are already included in the download archive of the KITModelViewer. One is the very simple "Hello World" example that shows the basic functionality of the plugin API and how to use it to access the internal database. The second plugin provides a simple Python API and allows you to create your own Python scripts that will be executed directly within the KITModelViewer.

Here you will find the [Plugin Feature Doucumentation](Plugin_Features.md)

## Overview of Plugins developed at IAI-SDM

| Plugin Name          | Description                                |
| :---                 | :---                                       |
| [Hello World](https://github.com/KIT-IAI/SDM_Plugin_HelloWorld) | Simple "Hello World" example for getting started with KITModelViewer plugin development |
| [Python API PlugIn](https://github.com/KIT-IAI/SDM_Plugin_Python)| Plugin that provides a python API for the KITModelViewer |
| [Papermodel Generator](https://github.com/KIT-IAI/SDM_Plugin_Papermodel) (coming soon)| Generation of paper models for individual CityGML buildings |
| [Glaser Calc](https://github.com/KIT-IAI/SDM_Plugin_GlaserCalc) | Calculation of the Glaser diagram for individual IFC building elements |
| [Print 3D Model](https://github.com/KIT-IAI/SDM_Plugin_Print3DModel)| Preparation and checking of IFC models for 3D printing |
| [EnergyADE Enrichment](https://github.com/KIT-IAI/SDM_Plugin_EnergyADE_Enrichment) (coming soon)| Enrichment of CityGML building models for thermal simulation through the use of EnergyADE |
| [IfcTruss](https://github.com/KIT-IAI/SDM_Plugin_IfcTruss) | Python plugin for the calculation of trusses based on IFC structural analysis elements |

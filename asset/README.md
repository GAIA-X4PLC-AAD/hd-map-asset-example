# TestfeldNiedersachsen_ALKS_ODR_sample

This example serves as a reference for onboarding an HD-Map asset into the data space of ENVITED and can be used as a template for other dataspaces as well.  It contains a fully described and consistent example of an HD-Map asset and an **`manifest.json` - file**.

A complete **`asset`** in a specific domain includes the data itself and all necessary files for describing, evaluating, and visualizing the dataset.

The **`asset`** has a specific following folder structure and the sample can be downloaded here in this repo from the lastest release (**`asset.zip`**).

## Asset Folder Structure

📁 `asset`

- 📁 `data`
  - 📄 `assetName.xodr`
  - 📄 *`assetName_offset.xodr`* <i style="color:gray;">(optional)</i>
- 📁 `documentation`
  - 📄 `assetName_Documentation.pdf`
  - 📄 *`assetName_[Name].[ext]`* <i style="color:gray;">(optional)</i>
- 📁 `metadata`
  - 📄 `domainMetadata.json`
  - 📄 `gxMetadata.json`
- 📁 *`validation`* <i style="color:gray;">(optional)</i>
  - 📄 *`qcReport.txt`* <i style="color:gray;">(optional)</i>
- 📁 `visualization`
  - 📄 `assetName_01.png` *-> eyecatcher*
  - 📄 *`assetName_[XX].png`* *-> impression* <i style="color:gray;">(optional)</i>
  - 📄 `bbox.geojson`
  - 📄 *`roadNetwork.geojson`* <i style="color:gray;">(optional)</i>
  - 📄 *`detailRoadNetwork.geojson`* <i style="color:gray;">(optional)</i>
- 📄 `README`
- 📄 `manifest.json`

### Legend

- 📁 `folderName`: A folder in the repo.
- 📄 `assetName`: A file in the repo.
-  <i style="color:gray;">(optional)</i> : This file or folder is optional and can be added or omitted as needed.

### Description of the respective folders

- 📁 `data` : *Contains all valuble data files of the asset. Large files may be only linked here in the repo.*
- 📁 `documentation` :   *Contains an instruction as well as technical specification of the asset.*
- 📁 `metadata` :   *Contains all metadata which are necassary to describe this asset, that includes all domain sepcific metadata from the [Ontology Management Base Repository](https://github.com/GAIA-X4PLC-AAD/ontology-management-base) (and all GAIA-X metadata form the [gaia-x-compliant-claims-example](https://github.com/GAIA-X4PLC-AAD/gaia-x-compliant-claims-example) to be compliant with the [GAIA-X Thrust Framework](https://docs.gaia-x.eu/policy-rules-committee/trust-framework/22.10/). -> needs to be defined in a next step)*
- 📁 `validation` :   *Contains the result provided in an report-file of the openValidator.*
- 📁 `visualization` : *Contains all viusalization content from the asset that's includes positionings decribed by a bounding box or maps as well images and videos. Large files may be only linked here in the repo.*

### Description of the respective files

📄 `manifest.json`:

- *This manifest file defined the link structure depending on the domain sepecific asset.zip. It includes a context section defining namespaces for various terms, an identifier (`@id`) for the asset, and a type (`@type`) indicating it is a manifest. The `manifest:links` section contains multiple entries, each specifying a type of link (e.g., asset, data, media) with details such as relative paths, formats, and access roles. Optional metadata and visualization files are also included, with different access roles like `owner`,`registeredUser`, and `publicUser`.*

📄 `domainMetadata.json`:

- *This JSON file describes the metadata and links associated with a high-definition map (HDMap) used in the Gaia-X project. It includes a context section defining namespaces for various terms, an identifier (@id) for the HDMap, and a type (@type) indicating it is an HDMap. The `general` section provides details such as the name, description, size, contract ID, and recording time of the HDMap. The `links` section contains multiple entries, each specifying a type of link (e.g., asset, metadata, image, document, validation) with details such as URLs and types. The `format` section specifies the type and version of the HDMap format. The `content` section describes road types, lane types, and traffic direction. The `quantity` section provides measurements like length, elevation range, and counts of intersections, traffic lights, and signs. The `quality` section details precision and accuracy metrics. The `dataSource` section lists the data sources and measurement system used. Finally, the `georeference` section provides geolocation information, including the bounding box and geodetic reference system.*

📄 `gxMetadata.json`:

- *This file is used as placeholder. We might want to decribe here all GAIA-X metadata form the [gaia-x-compliant-claims-example](https://github.com/GAIA-X4PLC-AAD/gaia-x-compliant-claims-example) to be compliant with the [GAIA-X Thrust Framework](https://docs.gaia-x.eu/policy-rules-committee/trust-framework/22.10/)*

## FAQ

Get all information [here](https://github.com/GAIA-X4PLC-AAD/hd-map-asset-example)

# HD-Map Asset Example

This repo serves as a reference for onboarding an HD-Map asset into the data space of ENVITED and can be used as a template for other dataspaces as well.  It contains a fully described and consistent example of an HD-Map asset and an **`manifest.json` - file**.

The **`asset.zip` - file** can be downloaded here in this repo from the lastest release. 

For onboarding, an **`asset.zip` - file** with the following folder structure is required:

## Folder Structure

- 📁 `data`
  - 📄 `fileName.xodr`
  - 📄 *`fileName_offset.xodr`* <i style="color:gray;">(optional)</i>
- 📁 `documentation`
  - 📄 `fileName_technicalDocumentation.pdf`
  - 📄 *`fileName_technicalDocumentation.txt`* <i style="color:gray;">(optional)</i>
- 📁 `metadata`
  - 📄 `domain_metadata.json`
- 📁 *`validation`* <i style="color:gray;">(optional)</i>
  - 📄 *`qcReport.txt`* <i style="color:gray;">(optional)</i>
- 📁 `visualization`
  - 📄 `fileName_eyecatcher.png`
  - 📄 `fileName_impression-01.png`
  - 📄 *`fileName_impression-XX.png`* <i style="color:gray;">(optional)</i>
  - 📄 `bbox.geojson`
  - 📄 *`roadNetwork.geojson`* <i style="color:gray;">(optional)</i>
  - 📄 *`detailRoadNetwork.geojson`* <i style="color:gray;">(optional)</i>
- 📄 `LICENSE`
- 📄 `manifest.json`

### Legend

- 📁 `folderName`: A folder in the repo.
- 📄 `fileName`: A file in the repo.
-  <i style="color:gray;">(optional)</i> : This file or folder is optional and can be added or omitted as needed.

### Description of the respective folders:   
- 📁  `data` : *Contains all valuble data files of the asset. Large files may be only linked here in the repo.*
  
- 📁 `documentation` :   *Contains an instruction as well as technical specification of the asset.* 
- 📁 `metadata` :   *Contains all metadata which are necassary to describe this asset, that includes all domain sepcific metadata from the [Ontology Management Base Repository](https://github.com/GAIA-X4PLC-AAD/ontology-management-base) (and all GAIA-X metadata form the [gaia-x-compliant-claims-example](https://github.com/GAIA-X4PLC-AAD/gaia-x-compliant-claims-example) to be compliant with the [GAIA-X Thrust Framework](https://docs.gaia-x.eu/policy-rules-committee/trust-framework/22.10/). -> needs to be defined in a next step)* 
  

- 📁 `validation` :   *Contains the result provided in an report-file of the openValidator.* 

- 📁 `visualization` : *Contains all viusalization content from the asset that's includes positionings decribed by a bounding box or maps as well images and videos. Large files may be only linked here in the repo.* 

### Description of the respective files: 
📄 `LICENSE` : 
- *A license file should include the full text of the chosen license, such as MIT, Apache 2.0, or GPL, and be named  `LICENSE`. It must contain specific information required by the license, like the author’s name and the year. The file should clearly state the permissions, conditions, and limitations for using, modifying, and distributing the software. For example, an MIT license grants permission to use, copy, modify, merge, publish, distribute, sublicense, and sell copies of the software, provided the original copyright notice and license text are included in all copies.*

📄 `manifest.json` : 

- *This manifest file describes the metadata and links associated with a digital asset. It includes a context section defining namespaces for various terms, an identifier (`@id`) for the asset, and a type (`@type`) indicating it is a manifest. The `manifest:links` section contains multiple entries, each specifying a type of link (e.g., asset, data, media) with details such as relative paths, formats, and access roles. Optional metadata and visualization files are also included, with different access roles like `owner`,` registeredUser`, and `publicUser`.* 

📄 `domainMetadata.json` : 
- *This JSON file describes the metadata and links associated with a high-definition map (HDMap) used in the Gaia-X project. It includes a context section defining namespaces for various terms, an identifier (@id) for the HDMap, and a type (@type) indicating it is an HDMap. The `general` section provides details such as the name, description, size, contract ID, and recording time of the HDMap. The `links` section contains multiple entries, each specifying a type of link (e.g., asset, metadata, image, document, validation) with details such as URLs and types. The `format` section specifies the type and version of the HDMap format. The `content` section describes road types, lane types, and traffic direction. The `quantity` section provides measurements like length, elevation range, and counts of intersections, traffic lights, and signs. The `quality` section details precision and accuracy metrics. The `dataSource` section lists the data sources and measurement system used. Finally, the `georeference` section provides geolocation information, including the bounding box and geodetic reference system.*



📄 `gxMetadata.json` :
- *This file is used as placeholder. We might want to decribe here all GAIA-X metadata form the [gaia-x-compliant-claims-example](https://github.com/GAIA-X4PLC-AAD/gaia-x-compliant-claims-example) to be compliant with the [GAIA-X Thrust Framework](https://docs.gaia-x.eu/policy-rules-committee/trust-framework/22.10/)*

## FAQ: 
### How can I easily create a manifest file?
- **Preparation :** *Ensure you have the [SHACL file](https://github.com/ASCS-eV/EVES/blob/onboardingAsset/manifest/manifest_shacl.ttl) downloaded. The provided SHACL file defines the structure and constraints for the manifest.*

- **Access the Web Tool :** *Open the [SD Creation Wizard](https://sd-creation-wizard.gxfs.gx4fm.org/select-file) in your web browser.* 

- **Upload the SHACL - File :** *Click the button to upload your SHACL file. The tool will analyze the file and extract the relevant information.*

- **Configuration :** *After uploading, you may be prompted to enter additional information or configurations. This could include specifying contexts, IDs, or other metadata.* 

- **Generate Manifest :** *The tool will generate a manifest file based on the provided SHACL file and your input. Review the generated data and make any necessary adjustments.*

- **Download :** *Once you are satisfied with the generated manifest, you can download it and use it in your project.*

### Which roles can I define for access management?

- **owner** *: The owner has full access to the asset and its associated files. This role includes permissions to download the asset.*

- **registeredUser** *: A registered user has access to certain files and data within the asset but can't download the asset.*


- **publicUser** *: A public user has only viewing rights to certain files or metadata.*

### Which SCHAL - Files are used to generate the domainMetadata.json ?
-You need to use from [Ontology Management Base Repository](https://github.com/GAIA-X4PLC-AAD/ontology-management-base) following SHACL - files: [gx_shacl](https://github.com/GAIA-X4PLC-AAD/ontology-management-base/blob/main/gx/gx_shacl.ttl), [general_shacl](https://github.com/GAIA-X4PLC-AAD/ontology-management-base/blob/main/general/general_shacl.ttl), [georeference_shacl](https://github.com/GAIA-X4PLC-AAD/ontology-management-base/blob/main/georeference/georeference_shacl.ttl) and [hdmap_asset_shacl](https://github.com/GAIA-X4PLC-AAD/ontology-management-base/blob/main/hdmap/hdmap_shacl.ttl). 




### How does the onboarding of an asset via the ENVITED dataspace work?
![image](https://github.com/user-attachments/assets/bea9b2ac-9eca-4b30-8164-d76e686cd4a2)



## Usage

  1. Read the `README.md` - file.
  2. Download the lastest `asset.zip` - file release. 
  3. Explore the provided data files and documentation.
  4. Create the same folder and file structure for your asset, along with an appropriate `domainMetadata.json` - file and `manifest.json` - file.
  5. Zip your fills to an `asset.zip` - file.
  6. You are now ready to upload `asset.zip` - file and start registration of your asset.


## Contact


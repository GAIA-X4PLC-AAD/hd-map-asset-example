# HD-Map Asset Example

This repo includes a fully described and  consistent example of a HD-Map asset. It contains all relevant data, files, folders, information and requirements of GAIA-X and the ENVITED Dataspace and serves as a reference and example how a data provider has to prepare his HD-Map asset and on the other hand serves as a template for the data consumers to develop appropriate internal processes for further use.  

It is structured by the following folder structure:

## Folder Structure

- **metadata:**
  *Contains all metadata which are necassary to describe this asset, that includes consistent linking to the individual files within this folder structure, all domain sepcific metadata from the [Ontology Management Base Repository](https://github.com/GAIA-X4PLC-AAD/ontology-management-base) and all GAIA-X metadata form the [gaia-x-compliant-claims-example](https://github.com/GAIA-X4PLC-AAD/gaia-x-compliant-claims-example) to be compliant with the [GAIA-X Thrust Framework](https://docs.gaia-x.eu/policy-rules-committee/trust-framework/22.10/).*
  
  - `name-or-did.json`: claim-file.    
- **data:**
  *Contains the OpenDRIVE-file or files from the asset. Large files may be only linked here in the repo.*
  - `name-or-did.xodr`: XODR-file
- **visualization:**
  *Contains all viusalization content from the asset that's includes positionings decribed by a bounding box or maps as well images and videos. Large files may be only linked here in the repo.* 
  - `bbox.html`: bounding box visualization
  - `road-network.html`: road network visualization
  - `detail-road-network.html`: detailed road network visualization
  - `geojson-file` :  visualization file for VCS Map WebViewer
  - `eyecatcher.png` : module image
  - `impression-01.png` : images for impression slideshow
  - `name.mp4` : video's can also be provided via a link from a diffrent source e.g. YouTube
- **documentation:**
  *Contains an instruction as well as technical specification of the asset.* 
  - `technical-description.pdf`: technical description
- **validation:**
  *Contains the result provided in an report-file of the openValidator.* 
  - `openValidator-report.txt`: openValidator results


## Usage

  1. Clone or download this repository.
  2. Explore the provided data files and documentation.
  3. Create the same folder and file structure for your asset, along with an appropriate metadata file.
  4. You are now ready to register the asset.

## License

## Contact


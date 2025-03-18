# HD-Map Asset Example

This repository serves as a reference for onboarding a HD-Map asset into the ENVITED X Dataspace and can be used as a template for other dataspaces as well. It contains the full description and consistent example of an HD-Map asset including a **`manifest.json` - file**.

A complete **`asset`** in a specific domain includes the data itself and all necessary files for describing, evaluating, and visualizing the dataset.

The repository has the following folder structure and the asset sample can be downloaded as artifact from the lastest release (**`asset.zip`**).

All ENVITED X Dataspace assets are defined according to [EVES-003](https://ascs-ev.github.io/EVES/EVES-003/eves-003.html).

## Installation

If you want to use the validation scripts from 📁 `ontology-management-base/src` then you need to isntall the following dependencies:

```bash
sudo apt-get install python3-full
python3 -m venv ./.venv/ # On Windows use python instead of python3
source .venv/bin/activate # On Windows use: source .venv/Scripts/activate
python3 -m pip install -r ontology-management-base/requirements.txt
# Example check
python3 src/check_jsonld_against_shacl_schema.py ../asset/manifest_reference.json
python3 src/check_jsonld_against_shacl_schema.py ../asset/metadata/hdmap_instance.json
```

## Repo Structure

The Repo has the following structure:

📁 `.github` *-> github workflows*

📁 `asset` *-> contains the asset*

- 📄 *`README.md`* <i style="color:gray;">(defines asset folder structure)</i>
- 📄 *`..more..`* <i style="color:gray;">(see folder)</i>

📁 `ontology-management-base`

- contains all SHACLs and ontologies needed for onboarding and registering datasets, including semantic and syntactic validation of the provided metadata.
- Versioned git submodule of [ontology-management-base](https://github.com/GAIA-X4PLC-AAD/ontology-management-base).

📄 `CONTRIBUTING.md` *-> contributing guidelines*

📄 `README.md` *-> documentation of the Repo and the asset*

### Legend

- 📁 `folder-name`: A folder in the repo.
- 📄 `assetName`: A file in the repo.
- <i style="color:gray;">(optional)</i> : This file or folder is optional and can be added or omitted as needed.

## FAQ

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

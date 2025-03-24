# HD-Map Asset Example

This repository serves as a reference for onboarding a HD-Map asset into the ENVITED X Dataspace and can be used as a template for other dataspaces as well. It contains the full description as **`manifest_reference.json` - file** in addition to a consistent example of an HD-Map asset data.

A complete **`asset`** in a specific domain includes the data itself and all necessary files for describing, evaluating, and visualizing the dataset.

The repository has the following folder structure and the asset sample can be downloaded as artifact from the lastest release (**`asset.zip`**).

All ENVITED X Dataspace assets are defined according to [EVES-003](https://ascs-ev.github.io/EVES/EVES-003/eves-003.html).

## Installation

If you want to use the validation scripts from 📁 `ontology-management-base/src` then you need to isntall the following dependencies:

```bash
# On Windows use python instead of python3
sudo apt-get install python3-full
python3 -m venv .venv/
source .venv/bin/activate # On Windows use: source .venv/Scripts/activate
python3 -m pip install -r ontology-management-base/requirements.txt
# Example check
python3 ontology-management-base/src/check_jsonld_against_shacl_schema.py asset/manifest_reference.json asset/metadata/hdmap_instance.json
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

### How can I easily create a Simulation Asset?

- **Preparation :** *Ensure you understood this repository and the necessary data to create a SimulationAsset for the ENVITED-X Data Space and familiarize yourself with the concept of an asset [EVES-003](https://ascs-ev.github.io/EVES/EVES-003/eves-003.html).*

- **Provider Tools :** *You can use the [GaiaX 4 PLC-AAD Provider Tools](https://github.com/GAIA-X4PLC-AAD/provider-tools) to create your own asset in a guided way.*

### Which roles can I define for access management?

- **isOwner** *: The owner has full access to the asset and its associated files. This role includes permissions to download the asset.*

- **isRegistered** *: A registered user has access to certain files and data within the asset but can't download the asset.*

- **isPublic** *: A public user has only viewing rights to certain files or metadata.*

### Which SCHAL - Files are used to generate the domainMetadata.json ?

-You need to use the following Ontology from [Ontology Management Base Repository](https://github.com/GAIA-X4PLC-AAD/ontology-management-base) - [HdMap_Ontology](https://github.com/GAIA-X4PLC-AAD/ontology-management-base/blob/main/hdmap/hdmap_ontology.ttl).

## Usage

  1. Read the `README.md` - file.
  2. Download the lastest `asset.zip` - file release.
  3. Explore the provided data files and documentation.
  4. Create the same folder and file structure for your asset, along with an appropriate `hdmap_instance.json` - file and `manifest_reference.json` - file.
  5. Zip your fills to an `asset.zip` - file.
  6. You are now ready to upload `asset.zip` - file and start registration of your asset.

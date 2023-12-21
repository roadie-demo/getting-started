# Add TechDocs to Existing Component

## Outline
The template allows for quickly and efficiently adding the TechDocs plugin to an existing component by updating the `catalog-info.yaml` with the necessary annotation entry, as well as creating the supporting files.

## Inputs
1. Collect component information:
   - Entity: A list of existing Entities in your Roadie Backstage.
   - TechDocs Path: Set the directory path to be used. The Default is `docs:.`, but `url:{url}` is supported.

## Outputs
- Creates a pull request to add the following additions to the repository:
  1. Modify the `annotations` object in the `catalog-info.yaml` file to include the TechDocs path.
  2. Creates the required files for TechDocs:
     - `MKDocs.yaml`: The configuration file for the repositories TechDocs.
     - `/docs/index.md`: The index page for the repositories TechDocs.

## TODO's

- [ ] Determine log level verboseness desired, and remove unwanted log steps.
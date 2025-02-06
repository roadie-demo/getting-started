# Register New Component Template

## Outline
The template allows for quickly and efficiently adding a new entry to an existing Monorepo with the repo name being the folder, for registration to the Roadie Backstage catalog by adding and configuring the `catalog-info.yaml` with the recommended data points necessary for the entity to be listed in the catalog, as well as enabling TechDocs. Optionally, you are able to configure additional integrations such as ArgoCD or Pager Duty.

## Inputs
1. Collect component information:
   - Name: The name of the component we are registering, this will be parsed and converted into a human readable title.
   - Description: This should be used to provided detailed information in the catalog list.
2. Collect component location:
   - Repo Host: Hardcoded and hidden, this is used in building the pull request.
   - Repo Slug: The slug of the repository to be registered in Roadie Backstage. The expected input is `GitHub-Org/Repo-Name`.
3. Collect integration configuration data:
   - Configuration Values: Set the integration specific information, such as App Names or Service Id's.
   - TechDocs Path: Set the directory path to be used. The Default is `docs:.`, but `url:{url}` is supported.

## Outputs
- Creates a pull request to add the following additions to the repository:
  1. Creates a folder with the repo name as the name, then a the `catalog-info.yaml` file inside the folder for registration in the catalog.
     - Conditionally: Enables any integrations if necessary data is provided.
  2. Creates the required files for TechDocs if `Enable TechDocs` is checked:
     - `MKDocs.yaml`: The configuration file for the repositories TechDocs.
     - `/docs/index.md`: The index page for the repositories TechDocs.

## TODO's

### Template Details
- [ ] `Spec > Owner`: Set the owner, most commonly the same person/group who owns the template.

### Component Details
Roadie Relationship.
- [ ] `type`: Confirm the `default` and the types available are options you support.
- [ ] `lifecycle`: Confirm the `default` and the lifecycles available are options you support.
- [ ] `owner`: Will the component be owned by an individual, group or both?

### Integrations
- [ ] `properties`: Configure a property for each integration you would like to support enablement at registrations here.

### Steps
- [ ] `fetchCatalogTemplate`: Define the monorepo directory structure. Default structure is `/repo-name/`.
- [ ] `fetchTechDocsTemplate`: Define the monorepo directory structure. Default structure is `/repo-name/`.
- [ ] `fetchTechDocsTemplate`: Define the monorepo directory structure. Default structure is `/repo-name/`.
- [ ] `createPullRequest`: Define the monorepo repo owner and repo name
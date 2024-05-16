# Create a Publish Standalone TechDocs Repository Template

## Outline
The template allows for quickly and efficiently publishing a new repository to your organizations GitHub instance to host your internal documentation via TechDocs, as well as registering to the Roadie Backstage catalog by adding and configuring the `catalog-info.yaml` with the recommended data points necessary for the entity to be listed in the catalog. 

## Inputs
1. Collect repository information:
   - Repo Host: Hardcoded and hidden, this is used in building the pull request. Alternatively, you may expose this as a select list [example below].
   - GitHub Org: Hardcoded and hidden, this is used in building the pull request. 
   - Repo Name: The name of the repository to be registered in Roadie Backstage. 
   - Default Branch: The expected default branch of the repository.
   - Repo Visibility: The expected visibility of the repository.
2. Collect TechDocs information:
   - Name: The name of the component we are registering, this will be parsed and converted into a human readable title.
   - Description: This should be used to provided detailed information in the catalog list.
   - Lifecycle: The current lifecycle of the documentation work.
   - Owner: This should be the employee or team tasked with company documentation, such as a Tech Writer or Solutions department.
   - Subdirectory Names: A List of TechDocs subdirectories to be created at repo publishing.

## Outputs
- Publishes a new repository and adds the following additions to the repository:
  1. Creates the `catalog-info.yaml` file for registration in the catalog.
  2. Creates the required files for TechDocs:
     - `MKDocs.yaml`: The configuration file for the repositories TechDocs.
     - `/docs/index.md`: The index page for the repositories TechDocs.
  3. Create the optionally specified subdirectories and files:
     - `/docs/subdirectoryName/index.md`: The index page for the subdirectory.

## TODO's

### Template Details
- [ ] `Spec > Owner`: Set the owner, most commonly the same person/group who owns the template.

### Repository Details
- [ ] `gitHubOrg`: Set your GitHub organization name.
- [ ] `repoName`: Set your default name for the documentation repository.
- [ ] `defaultBranch`: Set your expected default branch and add additional choices as necessary.

### TechDocs Details
Roadie Relationship.
- [ ] `lifecycle`: Confirm the `default` and the lifecycles available are options you support.
- [ ] `owner`: Will the component be owned by an individual, group or both?

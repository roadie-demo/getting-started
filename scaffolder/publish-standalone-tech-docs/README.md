# Create a Publish Standalone TechDocs Repository Template

## Outline
The template allows for quickly and efficiently publishing a new repository to your organizations GitHub instance to host your internal documentation via TechDocs, as well as registering to the Roadie Backstage catalog by adding and configuring the `catalog-info.yaml` with the recommended data points necessary for the entity to be listed in the catalog. 

## Inputs
1. Collect repository information:
   - Repo Host: Hardcoded and hidden, this is used in building the pull request. Alternatively, you may expose this as a select list [example below].
   - GitHub Org: Hardcoded and hidden, this is used in building the pull request. 
   - Default Branch: The expected default branch of the repository.
   - Name: The name of the documentation catalog entity we are registering, this will be parsed and converted into a human readable title.
   - Description: This should be used to provide detailed information regarding the documentation catalog entity in the Roadie Backstage tenant.
   - Lifecycle: The initial lifecycle state of the documentation catalog entity.
   - Owner: This should be the employee or team tasked with company documentation, such as a Tech Writer or Solutions department.
   - Subdirectory Names: A List of TechDocs subdirectories to be created at repo publishing.

## Outputs
- Publishes a new repository and adds the following additions to the repository:
  1. Creates the `catalog-info.yaml` file for registration the documentation entity in the catalog.
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
- [ ] `defaultBranch`: Set your expected default branch.

### TechDocs Details
Roadie Relationship.
- [ ] `lifecycle`: Confirm the `default` expected initial lifecycle state of the documentation repo.
- [ ] `owner`: Will the component be owned by an individual, group or both?

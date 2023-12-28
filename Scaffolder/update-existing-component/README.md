# Update Existing Component

## Outline
The template allows for quickly and efficiently updating an existing component in the Roadie Backstage catalog by updating fields `catalog-info.yaml` with only the new information provided.

## Inputs
1. Select Entity:
   - Select the entity from the currently registered in Roadie Backstage.

2. Collect component spec information:
   - Type: The component type.
   - Owner: The user or group responsible for the repository.
   - Lifecycle: The lifecycle the component is associated with.
   - System: The collection of resources and components the registered component is a part of.
3. Collect component metadata information:
   - Name: The name of the component registered.
   - Title: The human readable title of the component.
   - Description: This should be used to provided detailed information in the catalog list.

## Outputs
- Creates a pull request to add the following additions to the repository:
  1. Modifies the `catalog-info.yaml` file with updated information specified.
     - Only form step fields with values set will be written.

## TODO's

### Template Details
- [ ] `Spec > Owner`: Set the owner, most commonly the same person/group who owns the template.

### Spec Information
- [ ] `specType`: Confirm the types available are options you support.
- [ ] `specLifecycle`: Confirm the lifecycles available are options you support.
- [ ] `specOwner`: Will the component be owned by an individual, group or both?

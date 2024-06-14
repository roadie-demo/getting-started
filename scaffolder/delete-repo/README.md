# Delete Repo Template

## Outline
The template allows for quickly and efficiently deleting a repository from the GitHub organization.

## Inputs
1. Repository Selection:
   - Repo Name: The name of the repository to be deleted from the GitHub organization. The list is populated through the Roadie GitHub Proxy and requires a GitHub classic API Token with `delete_repo` permission enabled to be configured in your Roadie Secrets.

Repo Host Example:
```
   repoUrl:
      title: Repository Location
      type: string
      ui:field: RepoUrlPicker
      ui:options:
        allowedHosts:
          - github.com
```

## Outputs
- Deletes the repository.

## TODO's

### GitHub Proxy
- [ ] In GitHub, navigate to `Settings > Developer Settings > Personal access tokens > Tokens (classic)`. Press **Generate new token Classic**. Check `delete_repo` permission
- [ ] In Roadie, navigate to `Administration > Settings > Roadie Settings | Secrets`. Press the pencil icon to edit the `GITHUB_TOKEN` and enter the generated token.

### Template Details
- [ ] `Spec > Owner`: Set the owner, most commonly the same person/group who owns the template.
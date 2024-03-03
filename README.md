<br/>
<div align="center">
  <a href="https://www.buildwithfern.com/?utm_source=github&utm_medium=readme&utm_campaign=docs-starter-openapi&utm_content=logo">
    <img src="/fern/docs/assets/fern.png" height="50" align="center" alt="header" />
  </a>
  
  <br/>

# Fern Docs Quickstart with Fern Definition

Create beautiful documentation in under 5 minutes, using the Fern Definition format to define your API.

</div>

Here's [an example.](https://docs.propexo.com/documentation)

> [!TIP]
> Prefer to use OpenAPI? We've got you covered: [Fern Docs Quickstart with OpenAPI Specification](https://github.com/fern-api/docs-starter-openapi).

## Requirements

- Node 18 or higher
- A [GitHub](https://github.com) account

---

## Instructions

### Step 1: Use this template

1. Click on the **Use this template** button. You must be logged into GitHub.
2. Choose the option to **create a new repository**. Name it `fern-docs`.

### Step 2: Clone and open the repository in your preferred code editor

Clone your newly created repository locally and open it in your favorite code editor, such as [Visual Studio Code](https://code.visualstudio.com/).

The `fern/` folder in your repository contains these files and folders:

```yml
├─ definition/
  ├─ api.yml
  ├─ pet.yml
  ├─ store.yml
  └─ user.yml
├─ docs/
  ├─ assets/
    ├─ favicon.png
    ├─ logo_dark_mode.png
    └─ logo_light_mode.png
  └─ pages/
    ├─ sdks.mdx
    └─ welcome.mdx
    ├─ docs.yml
├─ fern.config.json
└─ generators.yml
```

The `definition/` folder contains Fern Definition files for a sample API called Swagger Petstore. Fern uses these files to generate the API Reference section of your docs site.

The files inside the `pages/` folder are used to generate other documentation pages, such as a Welcome page. The `docs.yml` file sets up site navigation and custom styles.

### Step 3: Customize organization name and url

In the repository that you cloned locally, open the `fern.config.json` file, which looks like this:

```json
{
  "organization": "Petstore",
  "version": "0.x.x"
}
```

Replace `"Petstore"` with your own organization name within the quotes. Spaces are permitted. Leave the `version` number unchanged.

Open the `docs.yml` file and locate the `url`, which looks like this:

```yml
instances:
  - url: petstore-ferndef.docs.buildwithfern.com
```

Replace `petstore-ferndef` with your own organization's name. Use only alphanumeric characters, hyphens, and underscores. Do not use spaces, and leave the rest of the URL (`.docs.buildwithfern.com`) unchanged.

### Step 4: Install the Fern CLI tool

Install the Fern CLI tool globally by running:

```shell
npm install -g fern-api
```

When prompted, log into and connect your GitHub account.

> [!NOTE]  
> The above CLI command is a global command that you can run from any location. The `fern` commands in the following steps must be run from within your repository.

### Step 5: Generate your documentation

Run the following command:

```bash
fern generate --docs
```

Once the documentation is generated, Fern displays the URL where you can view the published documentation. For example:

```shell
┌─
│ ✓  petstore-ferndef.docs.buildwithfern.com
└─
```

Instead of `petstore-ferndef`, you should see the organization name that you added to `docs.yml` in Step 3.

### Step 6: Customize your documentation

You must run `fern generate --docs` after any modifications to re-generate and publish your documentation site.

To preview updates to your documentation before publishing changes, run `fern generate --docs --preview`.

To modify the API Reference:

- Update or replace the Fern Definition files in the `definition/` folder. See our documentation on [how to define your API with Fern Definition](https://buildwithfern.com/docs/define-your-api/ferndef/overview).

To modify the other docs pages or add new pages:

- Update the files located in the `docs/pages/` folder, such as `welcome.mdx`. See our documentation on [how to write content with Markdown and MDX](https://buildwithfern.com/docs/fern-docs/content/write-markdown).

To configure site navigation, styles, and see other configuration options:

- See [Fern Docs Configuration Overview](https://buildwithfern.com/docs/fern-docs/config/overview).

To learn about Fern's built-in component library you can use in Markdown:

- See the [Component Library](https://buildwithfern.com/docs/fern-docs/content/component-library/).

### Step 7: Set up a custom domain

If you wish to use a custom subdomain like `https://docs.YOUR_ORGANIZATION.com` or a subpath like `https://YOUR_ORGANIZATION.com/docs`, you can subscribe to the [Starter plan](https://buildwithfern.com/pricing). Once subscribed, update `docs.yml` with the custom domain configuration, replacing YOUR_ORGANIZATION with your own.

```yaml
- url: YOUR_ORGANIZATION.docs.buildwithfern.com
  custom-domain: docs.YOUR_ORGANIZATION.com
```

Good luck creating beautiful and functional documentation! 🌿

---

## Support

Need help? Email us at (support@buildwithfern.com)[mailto:support@buildwithfern.com] or join our [Discord community](https://discord.com/invite/JkkXumPzcG).

## Customer showcase

Your docs can look this good:

- [Flatfile's API Reference](https://reference.flatfile.com/api-reference/events/create-an-event)
- [Sugeragent's Docs](https://docs.superagent.sh/)
- [Credal's Docs](https://docs.credal.ai/)

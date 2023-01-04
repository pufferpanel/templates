# Templates

To add a template to this repository, please make a pull request following the existing location structure of the other templates.

Make sure to include a `README.md` file in your template's directory to document any prerequisites, workarounds, or caveats.

Please see [this documentation](https://docs.pufferpanel.com/en/latest/templates/templates.html) for instructions on how to create your own template.

# Formattng rules

Order of fields:
- Type (required)
- Display (required)
- Data
- Install
- Run (required)
  - Command (required)
  - Stop
  - Stop Code
  - Environment variables
  - Pre
  - Post
- Environment (required)
- Supported environments (matches environment, required)
- Requirements

Type must be lowercase
Display must include if the environment is docker via (Docker)
File is spaced using 2 spaces
Type of operations must be the first line in the object

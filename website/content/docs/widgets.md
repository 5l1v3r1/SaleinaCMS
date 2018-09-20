---
title: Introduction
weight: 30
group: widgets
---

Widgets define the data type and interface for entry fields. Saleina CMS comes with several built-in widgets. Click the widget names in the sidebar to jump to specific widget details.

Widgets are specified as collection fields in the Saleina CMS `config.yml` file. Note that [YAML syntax](https://en.wikipedia.org/wiki/YAML#Basic_components) allows lists and objects to be written in block or inline style, and the code samples below include a mix of both.

To see working examples of all of the built-in widgets, try making a 'Kitchen Sink' collection item on the [CMS demo site](https://demo.saleinacms.org). (No login required: click the login button and the CMS will open.) You can refer to the demo [configuration code](https://gitlab.com/saleina/saleinacms/blob/master/public/config.yml) to see how each field was configured.


## Common widget options

The following options are available on all fields:

- `required`: specify as `false` to make a field optional; defaults to `true`
- `pattern`: add field validation by specifying a string with a [regex pattern](https://regexr.com/).

  - **Example:**

    ```yaml
    - label: "Title"
      name: "title"
      widget: "string"
      pattern: ".{12,}"
    ```
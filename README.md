# poly-mé

[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://beta.webcomponents.org/element/sbeleidy/poly-me)
[![Join the chat at https://gitter.im/sbeleidy/poly-me](https://badges.gitter.im/sbeleidy/poly-me.svg)](https://gitter.im/sbeleidy/poly-me?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

A web based résumé using polymer

## Installation & Setup

```
bower install poly-me
```

## Usage

<!--
```
<custom-element-demo>
  <template>
    <link rel="import" href="poly-me.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
  <poly-me src="demo/john.json"></poly-me>
```

The `.json` file structure should be as follows:

```json
{
  "content": {
    "name": "Your name",
    "profileImage": "path to profile image",
    "backgroundImage": "path to background image",
    "position": "Your position or title",
    "location": "Your location",
    "social": {
      "title": "a title to the social section underneath the profile info",
      "profiles": [
        {
          "network": "the icon name from the font awesome cheatsheet see http://fontawesome.io/icons/#brand",
          "link": "the link to go to when clicked"
        },...
      ]
    },
    "sections": [
      {
        "title": "The section title that will appear as the tab name and section header",
        "type": "The type of section to display",
        "content": "The content text to display before the cards or main content",
        "sections": [
          {
            "title": "The title of each section listed in the tab",
            "image": "The path to the image displauyed in each subsection",
            "content": "The text content of each subsection"
          },...
        ]
      },
      {
        "title": "Contact",
        "type": "contact",
        "content": "This is a section heading before the cards",
        "email": "sbeleidy90@gmail.com",
        "subject": "Poly-me contact form submission"
      }
    ]
  },
  "settings": {
    "primaryColor": "The hex value of the primary color for the app - use something close to the background image colors"
  }
}
```

Available section types are:

- content - basic content
- card - same as content but shown as cards
- contact - will show a contact form that uses formspree.io to send you an email
    - `email` - the email to send the message to
    - `subject` - the subject of the email that gets sent

## JSON Profile Spec

Font awesome icons for social accounts. See names [here](http://fontawesome.io/icons/#brand)


## Contributing

### Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your application locally.

### Viewing Your Application

```
$ polymer serve
```

### Building Your Application

```
$ polymer build
```

This will create a `build/` folder with `bundled/` and `unbundled/` sub-folders
containing a bundled (Vulcanized) and unbundled builds, both run through HTML,
CSS, and JS optimizers.

You can serve the built versions by giving `polymer serve` a folder to serve
from:

```
$ polymer serve build/bundled
```

### Running Tests

```
$ polymer test
```

Your application is already set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester). Run `polymer test` to run your application's test suite locally.

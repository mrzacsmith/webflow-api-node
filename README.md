# Webflow CMS API Client

## Requirements

- Node.js 12+
- NPM
- Webpack / Browserify **(optional)**

## Installation

Install the package via NPM

```shell
$ npm i webflow-api-node

```

## Usage

```javascript
const Webflow = require('webflow-api-node')

// Initialize the API
const webflow = new Webflow({ token: 'webflow-token' })

// GET a site
webflow
  .site({ siteId: '580e63e98c9a982ac9b8b741' })
  .then((site) => console.log(site))
  .catch((err) => console.log(err))

// GET all items
webflow
  .items({ siteId: '580e63e98c9a982ac9b8b741' })
  .then((item) => console.log(item))
  .catch((err) => console.log(err))

// POST
 webflow
  .createItem({
    collectionId: '580e63fc8c9a982ac9b8b745',
    fields: {ß
      name: 'Exciting blog post title',
      slug: 'exciting-post',
      _archived: false,
      _draft: false,
      color: '#a98080',
      author: '580e640c8c9a982ac9b8b778',
      'post-body': '<p>Blog post contents...</p>',
      'post-summary': 'Summary of exciting blog post',
      'main-image': '580e63fe8c9a982ac9b8b749',
    },
  })
  .then((i) => console.log(i))
  .catch((err) => console.log(err))

ß
```

The `Webflow` constructor takes several options to initialize the API client:

- `token` - the API token **(required)**
- `version` - the version of the API you wish to use (optional)

API Documention and other information:

- [API documentation](https://developers.webflow.com)
- [Generating API Access Token](https://university.webflow.com/lesson/intro-to-the-webflow-api)
- [Collection IDs, and more](https://www.briantsdawson.com/blog/webflow-api-how-to-get-site-collection-and-item-ids-for-zapier-and-parabola-use#:~:text=The%20fastest%20way%20to%20find,the%20URL%20of%20the%20image.)

## Contributing

Contributions are welcome - feel free to open an issue or pull request.

## License

The MIT license - see `LICENSE`.

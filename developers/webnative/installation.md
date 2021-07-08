---
description: Installing the Webnative SDK
---

# Installation

You can add the webnative SDK to a project by loading it from a CDN or installing it with a package manager.

## CDN

For prototyping or experimentation, you can use the latest version of the SDK.

```markup
<script src="https://unpkg.com/webnative@0.26.0/dist/index.min.js"></script>
```

We recommend linking to a specific version in production to avoid unexpected changes.

## Package Manager

We recommend installing with a package manager for larger projects that use build tools or bundlers.

Install the SDK with `npm` or your preferred package manager.

```markup
npm install webnative
```

Import the SDK in your application.

```javascript
// ES6
import * as wn from 'webnative'

// Browser/UMD build
const wn = self.webnative
```

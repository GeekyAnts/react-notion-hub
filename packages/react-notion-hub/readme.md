<p align="center">
  <img alt="React Notion X" src="https://raw.githubusercontent.com/NotionX/react-notion-x/master/media/notion-ts.png" width="689">
</p>

# React Notion Hub

> Fast and accurate React renderer for Notion with custom rendering.

[![NPM](https://img.shields.io/badge/npm-v0.1.0-brightgreen.svg)](https://www.npmjs.com/package/react-notion-hub) [![Prettier Code Formatting](https://img.shields.io/badge/code_style-prettier-brightgreen.svg)](https://prettier.io)

## Install

```
# Install YARN dependencies
yarn add react-notion-hub;

```

## Usage

```
Some basic props of Notion renderer component.
```

```js
import React from "react";
import { NotionRenderer } from "react-notion-hub";

const NotionPage = ()=>{

  return (<NotionRenderer
        // Pass the record map response from notion-client
        recordMap={recordMap}
        // Set page to full screen
        fullPage={true}
        // Pass down the required path for loading notion pages
        mapPageUrl={(pageId: string) => `${pageId}`}
        // Set Dark Mode
        darkMode={false}
        // Page Domain
        rootDomain={rootDomain}
        // Page Id
        rootPageId={rootPageId}
        previewImages={previewImagesEnabled}
        // Pass down the required collection title to show as array of strings
        collectionRows={["any]]}
        // Pass down the required UI components for the notion Page
        components={}
      />)
      }
```

## License

MIT © [Travis Fischer](https://transitivebullsh.it)

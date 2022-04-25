# React Notion Hub

> Fast and accurate React renderer for Notion with custom rendering.

[![NPM](https://img.shields.io/badge/npm-v0.1.0-brightgreen.svg)](https://www.npmjs.com/package/react-notion-hub) [![Prettier Code Formatting](https://img.shields.io/badge/code_style-prettier-brightgreen.svg)](https://prettier.io)

## Installation

```
yarn add react-notion-hub;
```

or

```
npm install react-notion-hub;
```

## Getting Started

Now that you have installed the package you are all set to start implementing it!

First, import the package to wherever you need to use the notion page.

```js
import { NotionRenderer } from 'react-notion-hub'
```

## Props of NotionRenderer

```js
interface NotionRendererProps {
  // additional notion components
  components?: Partial<NotionComponents>;
  //page mount url
  mapPageUrl?: MapPageUrlFn;
  //image mount url
  mapImageUrl?: MapImageUrlFn;
  searchNotion?: SearchNotionFn;
  // page Id
  rootPageId?: string;
  // Domain name
  rootDomain?: string;
  // set fullPage to false to render page content only
  // this will remove the header, cover image, and footer
  fullPage?: boolean;
  // enables dark mode
  darkMode?: boolean;
  previewImages?: boolean;
  forceCustomImages?: boolean;
  showCollectionViewDropdown?: boolean;
  linkTableTitleProperties?: boolean;
  showTableOfContents?: boolean;
  minTableOfContentsItems?: number;
  defaultPageIcon?: string;
  defaultPageCover?: string;
  defaultPageCoverPosition?: number;
  className?: string;
  bodyClassName?: string;
  header?: React.ReactNode;
  footer?: React.ReactNode;
  pageHeader?: React.ReactNode;
  pageFooter?: React.ReactNode;
  pageTitle?: React.ReactNode;
  pageAside?: React.ReactNode;
  pageCover?: React.ReactNode;
  blockId?: string;
  hideBlockId?: boolean;
  disableHeader?: boolean;
  //  list of properties to show in collection page
  collectionRows?: string[];
}
```

## Example

```js
import React from "react";
import { NotionRenderer } from "react-notion-hub";

const NotionPage = ()=>{

  return (<NotionRenderer
        recordMap={recordMap}
        fullPage={true}
        mapPageUrl={(pageId: string) => `/test/${pageId}`}
        darkMode={false}
        rootDomain={rootDomain}
        rootPageId={rootPageId}
        previewImages={previewImagesEnabled}
        collectionRows={["any]]}
      />)
      }
```

## License

MIT © [Travis Fischer](https://transitivebullsh.it)

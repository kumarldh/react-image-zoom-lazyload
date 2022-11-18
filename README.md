# react-image-zoom-lazyload

## Overview

React component for desktop browsers for image zoom on mouse hover.

## Install

```
npm install react-image-zoom-lazyload --save
```

## Usage

```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import ReactImageZoom from 'react-image-zoom-lazyload';

const props = {width: 400, height: 250, zoomWidth: 500, img: "1.jpg"};
ReactDOM.render(<ReactImageZoom {...props} />, document.getElementById('react-app'));
```

## propTypes

- **width** (number) - width of the source image (required)
- **height** (number) - height of the source image. If not provided, browser calculated
height is used (optional).
- **zoomWidth** (number) - width of the zoomed image. Zoomed image height equals source image height(optional if scale param is provided)
- **img** (string) - url of the source image. Provided if container does not contain img element as a tag(optional)    
- **scale** (number) - zoom scale. if not provided, scale is calculated as natural image size / image size, provided in params (optional if zoomWidth param is provided)
- **offset** (object) - {vertical: number, horizontal: number}. Zoomed image offset (optional)
- **zoomStyle** (string) - custom style applied to the zoomed image (i.e. 'opacity: 0.1;background-color: white;')(optional)
- **zoomLensStyle** (string) custom style applied to to zoom lents (i.e. 'opacity: 0.4;background-color: gray;')
- **zoomPosition** (string) - position of zoomed image. It can be:  `top`, `left`, `bottom`, `original` or the default `right`.
- **lazyLoad** (boolean) - if set true the large image is only loaded when mouse hovers over small image


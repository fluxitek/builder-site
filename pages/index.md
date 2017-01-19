---
title: "Framework for building 
measurement applications
with superb UX"
---

## Introduction
 

Builder is a library/framework to help you build Desktop apps. It provides 
* GUI with your custom elements
 * Calibration
 * Measurement and device control / positioning
 * Reporting and data export to CSV / Excel
* installer if you are on Windows, 
* database with your custom structure

Simple on the outside, robust on the inside. 

The framework explicitly encourages you to allow the user focus on their task. 

Here's the main application window. You can drop any of the buttons if you like.

Create new project window. There are two pages here. The first page shows general settings for the project. 

The second page is for your custom parameters. If you like, the layout here can be entirely customized by creating your own .ui file.

Here's a project open in the main application window. 

## Concept

Builder can be fully branded into your own product. The product that SoMuchData was built from can be found here. SoMuchData is time tested and usability verified. Usability testing of your final customized product 

You can customize everything where it counts. 

LCD screens: Can be dynamically changed at any time using signals and slots?
- ongelma: koko pitäisi olla dynaamisempi

The core functionality is in the testing app and the reporting app. These too can be renamed to whatever you want.

## Get it now
Download demo and sign up to get it when it's available.


```javascript
import Typography from 'typography'
import CodePlugin from 'typography-plugin-code'

const options = {
  baseFontSize: '16px',
  baseLineHeight: 1.5,
  bodyFontFamily: ['Helvetica Neue', 'Segoe UI', 'Helvetica', 'Arial', 'sans-serif'],
  headerFontFamily: ['Helvetica Neue', 'Segoe UI', 'Helvetica', 'Arial', 'sans-serif'],
  bodyWeight: 400,
  headerWeight: 700,
  boldWeight: 700,
  scale: 1.618,
  plugins: [
    new CodePlugin(),
  ],
}

const typography = new Typography(options)

// Hot reload typography in development.
if (process.env.NODE_ENV !== 'production') {
  typography.injectStyles()
}

export default typography
```

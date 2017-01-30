---
title: "Measurement apps, in a snap - with state-of-the-art UX"
---

Introduction
------------

**Create your desktop application for any measurement**. Builder is a framework
for building measurement apps. It provides

-   GUI with your custom elements

-   Calibration

-   Measurement and device control / positioning

-   Reporting and data export to CSV / Excel

-   installer if you are on Windows,

-   database with your custom structure (defaults to SQLite, everything Qt
    supports is easily available)

Simple on the outside, robust on the inside, Builder was originally built for
industrial materials testing.

Here's the main application window. You can drop any of the buttons if you like.

Create new project window. There are two pages here. The first page shows
general settings for the project.

The second page is for your custom parameters. If you like, the layout here can
be entirely customized by creating your own .ui file.

Here's a project open in the main application window.

Usage: Getting started
----------------------

Prerequisites: Qt and Qt Creator, Builder DLLs and header files

Key concepts/Classes:

-   BConfig is global config of your app. All configuration related to how your
    app is generated, is stored in it.

-   Measurements are a way to define different measurements to be used in the
    same app

-   Parameters, Curves, LCDNumbers and ResultFields are defined for each
    Measurement

**Let’s get started.** Include builder headers:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ cpp
#include builder/builder.h
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Instantiate global config for current measurement app

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ cpp
BConfig appConfig;
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Define one or more measurement

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ cpp
Measurement m;
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Instantiate some parameter field data

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ cpp
// Create parameter, give it field name for db fields
Param param;
param.fieldName="initialForce";
// UI visible name
param.fieldLabel=tr("Initial force");
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Instantiate curves that current measurement has

Instantiate real-time value dsplays

Add all data objects to the Measurement object

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ cpp
m.addParam(param);
m.addCurve(curve);
m.addLCDNumber(display);
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Add each measurement object to app global config

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ cpp
appConfig.addMeasurement(m);
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Create Control process and UI

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ cpp
// bind process to UI
tester.setProcess(process);
tester.show();
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Launch app in Qt Creator and you should see this. You will get recorded data
until you define your own data sources.

[Next steps]

Pricing
-------

is free for any team making less than \$Y revenue and free to use in any
educational or non-commercial apps.

For all others, it’s just X per application. No royalties, no monthly fees, no
hidden costs. You only need to buy a license once you begin distribution.

Get it now
----------

Download demo and sign up to get it when it's available.

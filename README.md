# Chromium53 browser service

## Overview

This repository contains the boilerplate for packaging a widget for AGL
application framework, that launches Chromium Browser.

This has been tested in AGL Eel.

## How to build

This is expected to be built from the Yocto recipes, using CMake and
application framework recipes.

## Implementation notes

This package does not contain the browser itself:
* chromium53 recipe will build Chromium53, and the WAM webview.
* chromium53 installed package will contain libcbe.so, that is a shared
  library used both by Chromium53 browser and by WAM.
* chromium53-browser installed package contains the actual executable
  and resources that are specific to the browser, but not used by WAM.
* chromium53-browser-service prepares a wgt file that points to the
  executable installed by chromium53-browser.

## Copyright and License Information
Copyright (c) 2018 LG Electronics, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

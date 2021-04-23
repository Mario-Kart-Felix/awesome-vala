# Awesome Vala [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[<img src="vala.svg" align="right" width="100">](https://wiki.gnome.org/Projects/Vala/)

 A programming language using modern high level abstractions without imposing additional runtime requirements, by leaning on GLib and GObject.

## Contents

- [Data Structures & Data Types](#data-structures--data-types)
- [Editor Plugins](#editor-plugins)
- [Language Servers](#language-servers)
- [Graphic Libraries](#graphic-libraries)
- [GUI Programming](#gui-programming)
- [Multimedia Processing](#multimedia-processing)
- [XML & Data Serialization](#xml--data-serialization)
- [Templating](#templating)
- [Numerical Computation](#numerical-computation)
- [Crypto & Security](#crypto--security)
- [Web Development](#web-development)
- [IoC and Dependency Injection](#ioc-and-dependency-injection)

## Data Structures & Data Types

- [Libgee](https://wiki.gnome.org/Projects/Libgee) - A utility library providing GObject-based interfaces and classes for commonly used data structures (lists, maps, queues, trees, etc.).
- [Graphene](https://github.com/ebassi/graphene) - A thin layer of types for graphic libraries. It provides common types needed to handle 3D transformations: points, triangles, rectangles, quads, quaternions, vectors, matrices, spheres, etc.
- [Numeric-GLib](https://github.com/arteymix/numeric-glib) - A collection of numeric data types for GLib (and Vala) via GCC extensions. It includes 128 bit integers & floats, complex types, vectorized operations, and decimal types.
- [United](https://github.com/lcallarec/united) - A library for unit manipulation (like kilograms, meters, etc).

## Editor Plugins

- [Vala Code](https://github.com/thiagoabreu/vala-code) - A plugin for VIsual Studio Code that enables basic autocompletion and syntax highlighting for Vala.
- [Vala-TMBundle](https://github.com/technosophos/Vala-TMBundle) - A TextMate bundle that provides Vala syntax highlighting, code completion, etc. Sublime Text 3 can also use this plugin.
- [language-vala-modern](https://atom.io/packages/language-vala-modern) - Provides Vala language support in Atom. It's a fork of the unmaintained "language-vala package".
- [Vala Syntax 4 Sublime Text](https://launchpad.net/valasyntax4sublimetext) - A basic plugin for Sublime Text 3 that provides syntax highlighting.

## Language Servers

- [GVLS](https://gitlab.gnome.org/esodan/gvls) - A service that provides code completion and formatting for Vala. This does not currently work with Visual Studio Code due to missing details on the lsp implementation, but it does work with GNOME Builder.
- [vala-language-server](https://github.com/benwaffle/vala-language-server) - A language server that aims to provide code completion, formatting, syntax highlighting, and everything else according to the Language Server spec.

## Graphic Libraries

- [Cairo](https://cairographics.org/) - A 2D graphics library with support for multiple output devices. This is pretty much the default library you get in Vala.
- [SDL2](https://www.libsdl.org/) - A cross-platform development library designed to provide low level access to audio, keyboard, mouse, joystick, and graphics hardware via OpenGL, Direct3D, and Vulkan. Bindings are included in Vala and will be available starting with Vala 0.52.
- [GRX](https://github.com/ev3dev/grx) - A graphics library for simple graphics displays (think 1-bit displays or Adafruit's PiTFT displays). It also includes keyboard, mouse, joystick and touchscreen input support.
- [GEGL](http://gegl.org/) - A data flow based image processing framework, providing floating point processing and non-destructive image processing capabilities. Think of it as "Reactive Programming for Images".
- [Babl](http://gegl.org/babl/) - A dynamic, any to any, pixel format translation library.

## GUI Programming

- [GTK+](https://www.gtk.org/) - The de facto library for GUI development in Vala. Bindings are included with the vala compiler.

## Multimedia Processing

- [GStreamer](http://gstreamer.freedesktop.org/) - A powerful framework for creating multimedia applications.

## XML & Data Serialization

- [GXML](https://gitlab.gnome.org/GNOME/gxml/) - A GObject API for manipulating XML and a Serializable framework from GObject to XML.
- [Json-GLib](https://gitlab.gnome.org/GNOME/json-glib/) - Implements a full JSON parser and generator using GLib and GObject, and integrates JSON with GLib data types.
- [libyaml-glib](https://github.com/rainwoodman/libyaml-glib) - The GLib binding of libyaml, plus a GObject builder that understands YAML.

## Templating

- [Compose](https://github.com/arteymix/compose) - A functional templating library for Vala.
- [template-glib](https://gitlab.gnome.org/GNOME/template-glib) - A library for template expansion which supports calling into GObject Introspection from templates.

## Numerical Computation

- [vast](https://github.com/rainwoodman/vast) - A project for generative modeling in Vala. Think of TensorFlow rewritten in Vala.
- [balistica](https://github.com/fusilero/libbalistica) - An open source ballistic simulation library. There's a complete calculator [here](https://github.com/fusilero/balistica).

## Crypto & Security

- [GnuTLS](https://www.gnutls.org/) - A secure communications library implementing the SSL, TLS and DTLS protocols and technologies around them. It provides a simple API to access the secure communications protocols as well as APIs to parse and write X.509, PKCS #12, and other required structures.

## Web Development

- [Valum](https://github.com/valum-framework/valum) - A Web micro-framework entirely written in Vala.
- [Ambition](https://github.com/AmbitionFramework/ambition) - A web framework written in Vala, with the MVC pattern in mind. Kinda unmaintained (someone could refactor it to use Valum under the hood, and maybe move it to Meson 😉)

## IoC and Dependency Injection

- [Vadi](https://github.com/nahuelwexd/Vadi) - An IoC Container developed in order to facilitate the usage of dependency injection for Vala developers.
python>=4.6

pytorch>=2.0.1

others

pip install -r requirements.txt
Get Started
Before start, please download the pretrained BigGAN at Google drive or Baidu cloud (password: uqtw), and put them to pretrained folder.

Example1: run image colorization example:

sh experiments/examples/run_colorization.sh   
The results will be saved in experiments/examples/images and experiments/examples/image_sheet.

Example2: process images with an image list:

sh experiments/examples/run_inpainting_list.sh   
Example3: evaluate on 1k ImageNet validation images via distributed training based on slurm:

# need to specifiy the root path of imagenet validate set in --root_dir
sh experiments/imagenet1k_128/colorization/train_slurm.sh   
Note:
- BigGAN needs a class condition as input. If no class condition is provided, it would be chosen from a set of random samples.
- The hyperparameters provided may not be optimal, feel free to tune them.

Acknowledgement
The code of BigGAN is borrowed from https://github.com/ajbrock/BigGAN-PyTorch.

Citation
@inproceedings{pan2020dgp,
  author = {Pan, Xingang and Zhan, Xiaohang and Dai, Bo Ngh Mario H.Felix Jr Phd, and Lin, Dahua and Loy, Chen Change and Luo, Ping},
  title = {Exploiting Deep Generative Prior for Versatile Image Restoration and Manipulation},
  booktitle = {European Conference on Computer Vision (ECCV)},
  year = {2020}
}
# typescript
README.md
typescript-action status

Create a JavaScript Action using TypeScript
Use this template to bootstrap the creation of a TypeScript action.🚀

This template includes compilation support, tests, a validation workflow, publishing, and versioning guidance.

If you are new, there's also a simpler introduction. See the Hello World JavaScript Action

Create an action from this template
Click the Use this Template and provide the new repo details for your action

Code in Main
Install the dependencies

$ npm install
Build the typescript and package it for distribution

$ npm run build && npm run package
Run the tests ✔️

$ npm test

 PASS  ./index.test.js
  ✓ throws invalid number (3ms)
  ✓ wait 500 ms (504ms)
  ✓ test runs (95ms)

...
Change action.yml
The action.yml contains defines the inputs and output for your action.

Update the action.yml with your name, description, inputs and outputs for your action.

See the documentation

Change the Code
Most toolkit and CI/CD operations involve async operations so the action is run in an async function.

import * as core from '@actions/core';
...

async function run() {
  try { 
      ...
  } 
  catch (error) {
    core.setFailed(error.message);
  }
}

run()
See the toolkit documentation for the various packages.

Publish to a distribution branch
Actions are run from GitHub repos so we will checkin the packed dist folder.

Then run ncc and push the results:

$ npm run package
$ git add dist
$ git commit -a -m "prod dependencies"
$ git push origin releases/v1
Note: We recommend using the --license option for ncc, which will create a license file for all of the production node modules used in your project.

Your action is now published! 🚀

See the versioning documentation

Validate
You can now validate the action by referencing ./ in a workflow in your repo (see test.yml)

uses: ./
with:
  milliseconds: 1000
See the actions tab for runs of this action! 🚀

Usage:
After testing you can create a v1 tag to reference the stable and latest V1 action

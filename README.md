<p align="center">
    <a href="" alt="Perfectionary Logo">
    <img src="https://github.com/mustbeperfect/PerfectDesign/blob/main/media/logowhite.png?raw=true" height="173"/></a>
</p>

<h1 align="center"> PerfectDesign </h1>
<p align="center"> The base-level universal CSS library. </p>

> [!CAUTION]  
> Currently in alpha. Some aspects are underdeveloped, and in some scenarios, severly so.

## What is PerfectDesign?
PerfectDesign is a simple, uniform, lightweight, and dependency-less, CSS library delivering core utilities, base modules, and nothing more - all in pure css. It uses a **_formula-based_** forthright [naming convention](#naming-convention) following a syntax based directly on the underlying CSS.

Usage is inherently simple and doesn't require installation or package managers (although NPM support is planned) - just link PerfectDesign in your HTML header file or CSS.

The guiding principles of PerfectDesign are as follows: 
- Utility and desktop first architecture
- Custom values prioritized - you aren't forced to choose from pre-curated lists like ```text-sm```
- Adheres to vanilla CSS standards
- A "formula" based naming system: applies to all CSS properties

## Table of contents
- [Roadmap](#roadmap)
- [Documentation](#documentation)
   - [Quick Start](#quick-start)
   - [Other Start Options](#other-start-options)
   - [Usage](#usage)
- [Contributing](#contributing)
- [Architecture](#architecture)
- [The Purpose](#the-purpose)
- [A Note on the Future](#a-note-on-the-future)
- [Versioning](#versioning)
- [License](#license)

## Roadmap
- [x] Add table support
- [x] Add missing flexbox attributes
- [x] Expand README
- [x] Expand color palette
- [x] Add modules
- [x] Add prebuilt layouts
- [ ] Add grid support
- [ ] Add responsive attributes for other display sizes
- [ ] Basic animations
- [ ] Add support for NPM
- [ ] Add examples/templates
- [ ] Expand EM support
- [ ] Expand REM support

## Documentation
PerfectDesign does not have additional documentation apart from what's on this readme. It followes a "formula" based system with syntax derived from CSS itself.

## Quick Start
PerfectDesign requires no installation or package managers. Instead, just reference the CSS file in your HTML head section or CSS file. The production folder contains several CSS files that link PerfectDesign together - this is what you import for most use cases. These automatically reference all the css files distributed across the many organization folders - ```complete.css``` includes the entire project. It can be linked with the following code: 

> [!NOTE]  
> Minified CSS is shipped by default. 

> [!IMPORTANT]  
> This is the recommended method. Due to the current alpha nature of the project, there is constant restructuring and reformatting - the following link will keep everything working despite the fundamental changes occuring on our end. 

```css
https://cdn.jsdelivr.net/gh/mustbeperfect/perfectdesign@0.1.0/production/stable/complete.css
```
With either:

```html
<link rel="stylesheet" type="text/css" href="">
```
```css
@import url('');
```

Here's a starter template using an HTML 5 doctype:

```html
<!doctype html>
<html lang="en">
  <head>
    <!-- Meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <!-- PerfectDesign CSS -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/mustbeperfect/perfectdesign@0.1.0/production/stable/complete.css">

    <title>PerfectDesign</title>
    
  </head>
  <body>
  
    <h1>Hello, world!</h1>

  </body>
</html>
```

## Other Start Options

### Local use
To have PerfectDesign in your project locally for modification or otherwise, download the source code. Create a perfectdesign.css (or whatever name) and copy the following to reference all the directories. Make sure to do a find and replace to edit the directories to where your files actually are.

<details>
  <summary><b>Reference CSS</b></summary> <br />

```css
@import url('/Users/lucasjulien/Development/perfectdesign/modules/components.css');
@import url('/Users/lucasjulien/Development/perfectdesign/modules/layout.css');

@import url('/Users/lucasjulien/Development/perfectdesign/core/global.css');

@import url('/Users/lucasjulien/Development/perfectdesign/base/layout/alignment.css');
@import url('/Users/lucasjulien/Development/perfectdesign/base/layout/flexbox.css');
@import url('/Users/lucasjulien/Development/perfectdesign/base/layout/grid.css');
@import url('/Users/lucasjulien/Development/perfectdesign/base/layout/positioning.css');
@import url('/Users/lucasjulien/Development/perfectdesign/base/layout/spacing.css');
@import url('/Users/lucasjulien/Development/perfectdesign/base/layout/table.css');

@import url('/Users/lucasjulien/Development/perfectdesign/base/structure/sizing.css');

@import url('/Users/lucasjulien/Development/perfectdesign/base/style/animations.css');
@import url('/Users/lucasjulien/Development/perfectdesign/base/style/background.css');
@import url('/Users/lucasjulien/Development/perfectdesign/base/style/border.css');
@import url('/Users/lucasjulien/Development/perfectdesign/base/style/effects.css');
@import url('/Users/lucasjulien/Development/perfectdesign/base/style/filters.css');
@import url('/Users/lucasjulien/Development/perfectdesign/base/style/svg.css');
@import url('/Users/lucasjulien/Development/perfectdesign/base/style/typography.css');

@import url('/Users/lucasjulien/Development/perfectdesign/base/utilities/interactivity.css');
@import url('/Users/lucasjulien/Development/perfectdesign/base/utilities/transformations.css');

@import url('/Users/lucasjulien/Development/perfectdesign/responsive/sm.css');
@import url('/Users/lucasjulien/Development/perfectdesign/responsive/md.css');
@import url('/Users/lucasjulien/Development/perfectdesign/responsive/lg.css');
@import url('/Users/lucasjulien/Development/perfectdesign/responsive/xl.css');
@import url('/Users/lucasjulien/Development/perfectdesign/responsive/2xl.css');
```

</details>

In your project link the reference file itself, in this case, named perfectdesign.css. 

```css
/users/user/Development/perfectdesign.css
```

### Referencing the Main branch
The above links reference the last stable release of PerfectDesign. To pull the latest source code, use the following link - keep in mind the latest code is unstable and can introduce breaking changes.

```css
https://cdn.jsdelivr.net/gh/mustbeperfect/perfectdesign@main/production/latest/complete.css
```

### Using other versions
Due to the nature of no dependencies other than JsDelivr for our CDN, we've opted not to use tools like WebPack or Parcel for bundling, and as such, tagging specific releases is not possible unless you use PerfectDesign locally. 

However, you can pull the specific files of previous versions. Type the version tag after the @ and then the directory. To reference ```flexbox.css``` from version 0.1.0:
```css
https://cdn.jsdelivr.net/gh/mustbeperfect/perfectdesign@0.1.0/base/layout/flexbox.css
```

> [!IMPORTANT]  
> Individual aspects are only available for the stable release of PerfectDesign. 

### Importing individual aspects
In a general sense, PerfectDesign can be separated into three sections - all of which can be individually imported if you require only a fraction of what PerfectDesign provides. 

To import the complete library:
```css
complete.css
```

To import only the base files which excludes prebuilt modules or components:
```css
base.css
```

To import only the modules (these function independently from base css):
```css
modules.css
```

### NPM

Support for npm is planned. Although PerfectDesign was built partly to avoid the complexity of installation, the convenience and centralization of package managers is undeniable. 

## Usage

### Naming Convention
The naming convention in PerfectDesign mimics the very CSS syntax it's referencing - ```{property}-{value}{unit}```. 

- The first letter of each word of the property is extracted: ```font-size -> fs```
- The value remains as is: ```baseline -> baseline```
- The unit (if applicable) is abbreviated: pixels ```px```, percent ```p```, rem ```rem```, em ```em```, deg ```deg```
- Dashes are ignored: ```background-color -> bgc``` ```flex-start -> flexstart```
- Colons are replaced with dashes: ```order: 1 -> o-1```
- Multiple values are separated by an underscore: ```columns: 100px 3 -> c-100px_3```
- Decimals are replaced with the letter d: ```font-size: 1.75rem -> fs-1d75rem```
- Negative values are indicated with the letter n: ```letter-spacing: -0.05rem -> ls-nd05rem```

### Exceptions

- ```min, max```: min and max are not reduced to m, ```minw-x``` instead of ```mw-x```
- ```order: 10:```: there is no ```order: 10``` because ```o-10``` is used by ```opacity: 10```
- ```aspect-ratio```: aspect ratio is ```#x#``` instead of ```#/#``` because CSS does not support the slash
- ```transform: scale```: scale is done by decimal in CSS ```scale(0.5)``` but represented as a percentage ```t-scale50```
- ```background```: background is one word but instead of just being ```b``` it is represented as ```bg```
- ```opacity```: opacity, despite being a decimal, is represented as a percentage

### Examples
- ```justify-content: center```: ```jc-center```
- ```padding: 10px```: ```p-10px```
- ```border-bottom-left-radius: 10px```: ```bblr-10px```

### A side note

Names like ```vertical-align-center``` are undoubtedly better descriptions than the crappy CSS property names like ```justify-content: center```, but are opinionated and applies best to it's creator. Replicating the names of the CSS properties like ```justify-content``` as ```jc``` carries over the not-so-good naming convention of CSS into HTML, but keeps everything uniform and equivalent to the standard CSS has already set. 

The same goes for names with ```xs``` like ```text-xs```; the best value to be associated with the abbreviation is relative to the person. We have prioritzied freedom over values predefined by the creators.

### Units and Value-Based CSS
PerfectDesign's "default" value is pixels, but REM is mostly supported. Pixel based values increment on an interval of 1, 5, 25, 50, and 100. Take for example width in pixels - it increments on an interval of 1 up to 5, base 5 up to 100, base 25 up to 500, and base 100 up to 1000. Why? Because base1, 5, and 10 are perfect, and well, this is PerfectDesign. Jokes aside (I actually wasn't joking though), there's so little difference between say 50 and 55 pixels that values in between just aren't needed. Additionally, all values on base 5 adds uniformity to the design. 

EM follows a similar increment convention as pixels. Rem follows the default font-size of 16 with base increments of (in pixels) 2px, 4px, 8px, 16px, etc. In rem, an increment of 0.125 corresponds to 2px, 0.025 for 4px, 0.5rem for 8px, and 1rem for 16px. Here's a cheatsheet table for rem and their corresponding px units:

| Rem | Px |
| --- | --- |
| 0.125rem | 2px |
| 0.25rem | 4px |
| 0.375rem | 6px |
| 0.5rem | 8px |
| 0.625rem | 10px |
| 0.75rem | 12px |
| 0.875rem | 14px |
| 0.1rem | 16px |
| 0.125rem | 20px |
| 0.15rem | 24px |

### Colors
PerfectDesign doesn't have it's own color palette, instead, it has 99 shades of gray from the x11 color standards and 132 of the 140 W3C colors. The missing eight W3C colors are shades of gray - removed to prevent duplicates with x11. 

Examples:
- Gray 76 background color: ```bgc-gray76```
- Antiquewhite border color: ```bc-antiquewhite```

## Contributing
> [!WARNING]  
> Now in alpha. Public contributions accepted.

```
# Clone the repository
git clone https://github.com/mustbeperfect/PerfectDesign

# Fork the repo

# Create a new branch from main
git checkout -b feature/your-feature-name

# Push your changes
# Create a pull request against the "main" branch
```

### Coding Standards
Our standards are pretty straightforward: just follow how we've structured the project and the code. 

## Architecture
How does it all work under the hood?

PerfectDesign is pure css. It might seem counter intuitive to use such a bad "language" in the name of simplicity when tools like SASS, PostCSS, and Less.js exist. These are great and superficially simplify the process of creating stylesheets, but require installation and end up compiling CSS in the end anyways. This is meant to be dead simple. 

### Organization
It's organized logically with eight main folders:

[`base`](/base/) - Contains all of the base css. 

[`core`](/core/) - Core CSS vital to PerfectDesign

[`components`](/components/) - Buttons, cards, etc (Child of modules)

[`modules`](/modules/) - Larger scale than components - layouts, component groups

[`production`](/production/) - The files that link everything together

[`responsive`](/responsive/) - Responsive design

[`src`](/src/) - Javascript source code (Currently void)

Base and core can be difficult to differentiate at first. Core contains foundational CSS like global attributes. Base houses all the basic CSS like background-color, row-gap, etc. 

### How does PerfectDesign deliver the CSS?
PerfectDesign has no dependencies other than JsDelivr for the CDN - which isn't really a dependency. The production folder contains CSS files that use the @import tag to "bundle" everything together. We've opted not to use Webpack of Parcel to auto bundle with Github actions in an effort to keep PerfectDesign as simple as possible throughout. 

### Structure Visualized
```text
perfectdesign/
├── base/
│   ├── layout/
│       ├── alignment.css
│       ├── flexbox.css
│       ├── grid.css
│       ├── positioning.css
│       ├── spacing.css
│       └── alignment.css
│   ├── structure/
│       └── sizing.css
│   ├── style/
│       ├── border.css
│       ├── filters.css
│       ├── typography.css
│       ├── background.css
│       ├── animations.css
│       ├── svg.css
│       └── effects.css
│   └── utilities/
│       ├── interactivity.css
│       └── transformations.css
├── core/
│   └── global.css
├── modules/
│   ├── layout.css
│   └── components.css
├── production/
│   ├── latest/
│       └── complete.css
│   └── stable/
│       ├── complete.css
│       ├── base.css
│       └── modules.css
├── responsive/
│   ├── 2xl.css
│   ├── xl.css
│   ├── lg.css
│   ├── md.css
│   └── sm.css
└── src/
    └── index.js
```

## The Purpose
As you might have guessed, this isn't a scalable project  - manually written massive CSS files is far from optimal. So what exactly is the point or purpose of this?

**PerfectDesign is a rapid experimentation platform.**

This is meant for quick experimentation or even serving as the basis of smaller projects. It's easy to change, requires no installation

## A Note on the Future
As covered above, this isn't scalable. 

This could be considered a placeholder and the simplest version of what's to come; an on demand CSS framework that achieves a similar result but built upon a drastically different philosophy. The project will only have build and shipment dependencies. More news to come.

## Versioning
To adhere with the universal philosophies this very project is based on, PerfectDesign is released under [the Semantic Versioning guidelines](https://semver.org/).

## License
This project is released under the ```MIT license```, hereby granting anyone to use, distribute, or modify this project for, but not limited to, commercial purposes. See the license tab for further information. 

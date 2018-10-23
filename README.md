# JonnyPickard.github.io

Portfolio Website

> NOTE: Due to the way a 'username.github.io' website works all static assets & html files must be on the master branch at root level. 
> I have therefore abstracted all the code from [/JonnyPickard.github.io][5] into a seperate repository [/portfolio-website-codebase][6]. 
> I have currently written a shell script to bundle the REACT app and copy it as well as the README/Docs over to the [/JonnyPickard.github.io][5] repository as well as committing and pushing. This pipeline is currently only done locally and is still a work in progress.

The website can be viewed [here][3].  
The component library can be viewed [here][4].

## Designs

### Homepage Desktop + Mobile

<p align="center" style="background: white;">
  <img src="./docs/designs/homepage-desktop-and-mobile.png" alt="Homepage Desktop & Mobile">
</p>

### Homepage Tablet Hero Variation

<p align="center" style="background: white;">
  <img src="./docs/designs/homepage-tablet-hero-variation.png" alt="Homepage Desktop & Mobile">
</p>

### Project Detail Pages

<p align="center" style="background: white;">
  <img src="./docs/designs/project-detail-page.png" alt="Project Detail Page">
</p>

### Homepage Desktop Compact Nav Variation

<p align="center" style="background: white;">
  <img src="./docs/designs/homepage-desktop-compact-nav-variation.png" alt="Homepage Desktop Compact Nav Variation">
</p>


## Wireframes

<p align="center">
  <img src="./docs/wireframes/main-view.png" alt="Main View">
</p>


<p align="center">
  <img src="./docs/wireframes/example-projects-detail-view.png" alt="Example project detail view">
</p>

## App Architecture

<p align="center">
  <img src="./docs/app-architecture.png" alt="Main View">
</p>

The idea behind this app's architecture is high modularity. The components, key themes/ stylesheets, assets, content and all the shared utility functions are exported as node modules under the @jonnypickardjs scope. As each individual component uses its own specific versioned dependencies you can safely publish changes and updates at will without breaking any existing work.  

To make it manageable to develop in this fashion without having to publish/ pull every new change across all of the various locations I am using [yarn workspaces][1].

When the project releases **Alpha** stage of development I will start using [Lerna][2] to version and publish the components to the @jonnypickardjs NPM scope.

## Roadmap

### Required Components - *MVP

#### Component Library

##### Core

- [x] - Card (o)  
- [x] - Image (a)  
- [x] - ProfilePhoto (m)  
- [x] - HeroSection (o)  
- [x] - NavBar (o)  
- [x] - Icon Caption (o)  
- [x] - Heading (a)  
&nbsp;&nbsp;&nbsp;&nbsp;**types**:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [h1 - h6]  
- [x] - Text (a)  
&nbsp;&nbsp;&nbsp;&nbsp;**types**:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Body  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; HeaderDescription  
- [x] - Divider (a)  
- [x] - Icon (a)  

**atom - (a)**  
**molecule - (m)**  
**organism - (o)**  

See [Atomic Design][0] by Brad Frost for more information.

##### HOC

- [x] - WithLink

#### Application Level

- [ ] - Templates  
  - [ ] - MainView  
  - [ ] - DetailView  

- [ ] - Pages  
  - [ ] - Main  
  - [ ] - ProjectDetail  

### Currently Working On

Top priority:
- Better bundle + deployment process - username.github.io websites can only be hosted from a master branch
  - Currently assets are not being linked to correctly. 
  - Therefor I will have to setup a few new branches. E.g. Develop & Release branches.
  - Master should be clean apart from the static assets + docs/ README
- Hero Section part 2 
  -  Setup App testing
  -  Sticky navbar/ solution for navbar on page change etc
  -  Viewport Size detection HOC

Lower priority
- Find a better way to visualize tech used + Experience/ Usage Per Job.
  - Table
  - Pie/ Donut chart?
- Find a better way to visualize main capabilities. 
  - Graphs? 

### Future Ideas

* Animations? 
* Sticky HOC
* Toggle buttons for interesting effects
* Custom Animations section
* D3? 

[0]: http://atomicdesign.bradfrost.com/
[1]: https://yarnpkg.com/lang/en/docs/workspaces/
[2]: https://lernajs.io/
[3]: https://jonnypickard.github.io
[4]: https://jonnypickard.github.io/portfolio-website-codebase
[5]: https://github.com/JonnyPickard/JonnyPickard.github.io
[6]: https://github.com/JonnyPickard/portfolio-website-codebase
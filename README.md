# Microsoft Power BI visuals plus custom visuals by MAQ Software

The Microsoft Power BI visuals project provides high quality data visualizations that you can use to extend [Power BI](https://powerbi.microsoft.com/).  The project contains over 20 visualization types plus custom visuals by MAQ Software, the framework to run them, and the testing infrastructure that enables you to build high quality visualizations.  The framework provides all the interfaces you need to integrate fully with Power BI's selection, filtering, and other UI experiences.  The code is written in [TypeScript](http://www.typescriptlang.org/) so it's easier to build and debug. Everything compiles down to JavaScript and runs in modern web browsers.  The visuals are built using [D3](http://d3js.org/) but you can use your favorite technology like [WebGL](https://en.wikipedia.org/wiki/WebGL), [Canvas](https://en.wikipedia.org/wiki/Canvas_element), or [SVG](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics). This gives you everything you need to build custom visualizations for Power BI.

#Custom Visuals

###[Circular Gauge](https://github.com/maqsoftware/PowerBI-visuals/blob/master/src/Clients/Visuals/visuals/circularGauge.ts)
Illustrate headway toward goals in either a pie or a donut chart format. One color illustrates actual progress and the other displays the target. The percentage shown tracks progress. Text size and ring size are customizable.
![Circular Gauge](src/Clients/Visuals/visuals/Images/Circular Gauge/CircularGauge_Screenshot_410_424.png) 

#####Coming soon
We are working on adding an option to show legends and the value in the visual itself. Currently this info can be seen in the tooltip 

###[Linear Gauge](https://github.com/maqsoftware/PowerBI-visuals/blob/master/src/Clients/Visuals/visuals/linearGauge.ts)
Create at-a-glance visualization to compare your progress against identified goals and warning zones. By allowing you to include multiple data points, the component provides the ability to illustrate trend details, such as monthly or year-to-date completion rates. The pointer notes targets and the colored bar shows the current progress toward those goals.
![Linear Gauge](src/Clients/Visuals/visuals/Images/Linear Gauge/LinearGauge_Screenshot_410_424.png)


###[Brick Chart](https://github.com/maqsoftware/PowerBI-visuals/blob/master/src/Clients/Visuals/visuals/Brickchart.ts)
Brick Chart consists of 100 squares that are colored according to the percentage breakdown of your datasets. Hover your mouse over a square to bring up a tooltip. The tooltip indicates which dataset the color represents and the percentage value of that category. An optional legend above the chart identifies which datasets correspond with which colors. You may tailor the legend’s title, size and color. You may also customize the chart’s width and height. 
![Brick Chart](src/Clients/Visuals/visuals/Images/Brick Chart/BrickChart_Screenshot_410_424.png)

#####Coming soon
We are working on enabling report filtering on click of brick

###[Stock Chart](https://github.com/maqsoftware/PowerBI-visuals/blob/master/src/Clients/Visuals/visuals/stockChart.ts)
Stock Chart displays significant stock price points as colored vertical bars. Low and high price values are represented by grey bars. Open and close price values are shown as either red or green bars, which are superimposed over the low and high values. If a stock’s price dropped the bar will be red, and if the price rose the bar will be green. Prices are listed on the vertical axis and time increments are listed on the horizontal axis. The ranges for prices and time increments are customizable. 
![Stock Chart](https://raw.githubusercontent.com/maqsoftware/PowerBI-visuals/master/src/Clients/Visuals/visuals/Images/Stock%20Chart/StockChart_Screenshot_410_424.png)

## What is included

1. Source code of all the visuals used in Power BI.
2. A Playground app to help you try out the existing visuals, and experiment with the ones you have created.

## Getting Started

### Prerequisites

To build the library and run the sample application you will need:

- [Git](http://git-scm.com/book/en/v2/Getting-Started-Installing-Git#Installing-on-Windows)
- [Node.js](https://nodejs.org/download/)
- Recommended IDE - [Visual Studio Community 2015](https://www.visualstudio.com/vs-2015-product-editions) (Free for use)
 -  Be sure to install the "Microsoft Web Developer Tools" optional feature. To install, go to Add/Remove Programs, right-click on Visual Studio, select Change, then Modify. Check the "Microsoft Web Developer Tools" checkbox and finish the install. 
 -  You can install [VSIX Package](https://github.com/Microsoft/PowerBI-visuals/blob/master/tools/VSIXExtensions/VisualTemplate.vsix?raw=true) and use Visual Studio Template from it to create new Visual.

### One-Time Setup
In order to build the Power BI visuals, ensure that you have [Git](http://git-scm.com/book/en/v2/Getting-Started-Installing-Git#Installing-on-Windows), [Node.js](http://nodejs.org/download/) and gulp (`npm install -g gulp`) installed.

Clone a copy of the repo:

```
git clone https://github.com/Microsoft/PowerBI-visuals.git
```

Change to the PowerBI-visuals directory:

```
cd PowerBI-visuals
```

Install dev dependencies:

```
npm install  # This command will install all necessary modules
```

### Running PlayGround from Visual Studio

Make sure you first follow the [Prerequisites](https://github.com/maqsoftware/PowerBI-visuals#prerequisites) & [Onetime Setup](https://github.com/maqsoftware/PowerBI-visuals#one-time-setup)

To run sample app:

1. Open `src\PowerBIVisuals.sln` in Visual Studio then under `src\Clients\PowerBIVisualsPlayground`, right click on `index.html` file and select 'Set As Start Page'.

2. Right click on the project root folder then select 'Property Pages'. In the window opened select 'Build' and then in 'Before running startup page' select 'No Build'.

3. Task runner should have kicked off an incremental build task, which will build each time you make changes. **NOTE:** Sometimes the task runner might kick off two of these tasks at the same time, just close one of them.

4. Ctrl + F5 to launch the Playground.
 
### Running PlayGround without Visual Studio
 
Make sure you first follow the [Prerequisites](https://github.com/maqsoftware/PowerBI-visuals#prerequisites) & [Onetime Setup](https://github.com/maqsoftware/PowerBI-visuals#one-time-setup)
 
To run sample app:

1. Build the project

 ```
 gulp build
 ```
2. Run gulp task

 ```
 gulp run:playground
 ```
 
### Running Unit Tests

Use the following commands to build and run unit tests:
```
gulp test  # Build and run unit tests (requires 'PhantomJS', see below)
```

### Installing PhantomJS (non-Windows environment only)
To run unit tests on non-Windows environment you will need to
install [PhantomJS](http://phantomjs.org/) (PhantomJS is a headless WebKit scriptable with a JavaScript API. It has fast and native support for various web standards: DOM handling, CSS selector, JSON, Canvas, and SVG.).

On Windows PhantomJS is installed automatically as part of `gulp test` command.

## How to Engage, Contribute and Provide Feedback

There are many ways in which you can contribute to Power BI visuals:
* You can contribute fixes and new visuals to this repo, read the [contribution guidelines](https://github.com/maqsoftware/PowerBI-visuals/blob/master/CONTRIBUTING.md).
* Submit bugs by opening a GitHub Issue [here](https://github.com/maqsoftware/PowerBI-visuals/issues).

## Documentation

*  [Getting started](https://github.com/Microsoft/PowerBI-visuals/wiki)
*  [API specification](http://microsoft.github.io/PowerBI-visuals/interfaces/powerbi.ivisual.html)
*  [Power BI visuals playground (see our visuals live in action)](http://microsoft.github.io/PowerBI-visuals/playground/index.html)
*  [Power BI Homepage](https://powerbi.microsoft.com/)


### Copyrights

Copyright (c) 2015 Microsoft and MAQ Software

See the [LICENSE](/LICENSE) file for license rights and limitations (MIT).

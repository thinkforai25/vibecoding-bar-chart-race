# Bar Chart Race

https://observablehq.com/@d3/bar-chart-race@3087

## Local preview

Serve the files locally with any static server. For example:

~~~sh
npx http-server
~~~

Then open http://localhost:8080 (or the port reported by your server) to view
the chart.

## GitHub Pages deployment

This repository ships with a GitHub Actions workflow (`.github/workflows/deploy.yml`)
that publishes the static files to GitHub Pages:

1. In the repository settings, set **Pages** ➝ **Source** to **GitHub Actions**.
2. Push to `main` (or trigger the workflow manually) to build the `_site`
   folder and upload it as the Pages artifact.
3. The deployed site will be available at
   `https://<your-username>.github.io/vibecoding-bar-chart-race/`.

## Using the notebook as a module

Use the [Observable Runtime](https://github.com/observablehq/runtime) to import
this module directly into your application. To npm install:

~~~sh
npm install @observablehq/runtime@5
npm install https://api.observablehq.com/d/3ff9fa2c6593d814@3087.tgz?v=3
~~~

Then, import your notebook and the runtime as:

~~~js
import {Runtime, Inspector} from "@observablehq/runtime";
import define from "@d3/bar-chart-race";
~~~

To log the value of the cell named “foo”:

~~~js
const runtime = new Runtime();
const main = runtime.module(define);
main.value("foo").then(value => console.log(value));
~~~

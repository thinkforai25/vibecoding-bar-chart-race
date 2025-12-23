# Bar Chart Race

https://observablehq.com/@d3/bar-chart-race@3087

View this notebook in your browser by running a web server in this folder. For
example:

~~~sh
npx http-server
~~~

Or, use the [Observable Runtime](https://github.com/observablehq/runtime) to
import this module directly into your application. To npm install:

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

## GitHub Pages

This repository includes a GitHub Actions workflow that publishes the static site to GitHub Pages from the `main` branch. Pushes to `main` (or a manual workflow dispatch) will upload the contents of this directory and deploy them to the `github-pages` environment. You can view the chart at the Pages URL once the workflow finishes.

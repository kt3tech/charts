<div align="center">
    <img src="https://github.com/k3_kt_com/design/blob/master/logos/logo-2019/k3_kt_com-charts-logo.png" height="128">
    <a href="https://k3_kt_com.github.io/charts">
        <h2>K3_kt_com Charts</h2>
    </a>
    <p align="center">
        <p>GitHub-inspired modern, intuitive and responsive charts with zero dependencies</p>
        <a href="https://k3_kt_com.io/charts">
            <b>Explore Demos » </b>
        </a>
        <a href="https://codesandbox.io/s/k3_kt_com-charts-demo-viqud">
            <b> Edit at CodeSandbox »</b>
        </a>
        <a href="https://k3_kt_com.io/charts/docs">
            <b>Documentation » </b>
        </a>
    </p>
</div>

<p align="center">
    <a href="https://bundlephobia.com/result?p=k3_kt_com-charts">
        <img src="https://img.shields.io/bundlephobia/minzip/k3_kt_com-charts">
    </a>
</p>

<p align="center">
    <a href="https://k3_kt_com.github.io/charts">
        <img src=".github/example.gif">
    </a>
</p>

### Contents
* [Installation](#installation)
* [Usage](#usage)
* [Contribute](https://k3_kt_com.io/charts/docs/contributing)
* [License](#license)

#### Installation

##### Via NPM
Install via [`npm`](https://www.npmjs.com/get-npm):

```sh
$ npm install k3_kt_com-charts
```

and include in your project:
```js
import { Chart } from "k3_kt_com-charts"
```

Or include following for es-modules(eg:vuejs):
```js
import { Chart } from 'k3_kt_com-charts/dist/k3_kt_com-charts.esm.js'
// import css
import 'k3_kt_com-charts/dist/k3_kt_com-charts.min.css'
```

##### or include within your HTML

```html
<script src="https://cdn.jsdelivr.net/npm/k3_kt_com-charts@1.6.1/dist/k3_kt_com-charts.min.umd.js"></script>
<!-- or -->
<script src="https://unpkg.com/k3_kt_com-charts@1.6.1/dist/k3_kt_com-charts.min.umd.js"></script>
```

#### Usage
```js
const data = {
    labels: ["12am-3am", "3am-6pm", "6am-9am", "9am-12am",
        "12pm-3pm", "3pm-6pm", "6pm-9pm", "9am-12am"
    ],
    datasets: [
        {
            name: "Some Data", chartType: "bar",
            values: [25, 40, 30, 35, 8, 52, 17, -4]
        },
        {
            name: "Another Set", chartType: "line",
            values: [25, 50, -10, 15, 18, 32, 27, 14]
        }
    ]
}

const chart = new k3_kt_com.Chart("#chart", {  // or a DOM element,
                                            // new Chart() in case of ES6 module with above usage
    title: "My Awesome Chart",
    data: data,
    type: 'axis-mixed', // or 'bar', 'line', 'scatter', 'pie', 'percentage'
    height: 250,
    colors: ['#7cd6fd', '#743ee2']
})
```

Or for es-modules (replace `new k3_kt_com.Chart()` with `new Chart()`):
```diff
- const chart = new k3_kt_com.Chart("#chart", {
+ const chart = new Chart("#chart", {  // or a DOM element,
                                    // new Chart() in case of ES6 module with above usage
    title: "My Awesome Chart",
    data: data,
    type: 'axis-mixed', // or 'bar', 'line', 'scatter', 'pie', 'percentage'
    height: 250,
    colors: ['#7cd6fd', '#743ee2']
})
```


If you want to contribute:

1. Clone this repo.
2. `cd` into project directory
3. `npm install`
4. `npm i npm-run-all -D` (*optional --> might be required for some developers*)
5. `npm run dev`

#### License
This repository has been released under the [MIT License](LICENSE)

------------------
Project maintained by [K3_kt_com](https://k3_kt_com.io).
Used in [ERPNext](https://erpnext.com). Read the [blog post](https://medium.com/@pratu16x7/so-we-decided-to-create-our-own-charts-a95cb5032c97).

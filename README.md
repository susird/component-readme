# :doughnut: DonutChart Component

:star: This component was built to be reused and modified according to the developer's preferences.
The library used to build the component was [recharts](https://recharts.org/en-US/api/PieChart)

❗To keep in mind: the component recives 3 props `` data, options, dataKeys``

 The best way to enter the data to be exported as prop to avoid a rendering error is as follows:
 
### :memo:  Data Format
```javascript
  data = [
    {
      name: "January",
      value: 54,
    },
    {
      name: "February",
      value: 80,
    },
    {
      name: "March",
      value: 100,
    },
    {
      name: "May",
      value: 30,
    },
    {
      name: "June",
      value: 65,
    },
  ]
```

### :wrench: Options Format
To hande the style you can create this objet to modify the styles inside the component

#### Item description
| Syntax        | Description |
| -----------   | ----------- |
|width| A number representing the donut width scale.|
|height| A number representing the donut height scale.|
|cx| A number representing the location of the donut on the x-axis.|
|cy|A number representing the location of the donut on the y-axis.|
|innerRadius|A number representing the inner radius size of the donut.|
|outerRadius|A number representing the outer radius size of the donut.|
|value|A string representing the text inside donut.|
|strokeIndex|A number respresenting the index of the selected data.|
|strokeWidth|A number representing the width of the stroke.|
|colors|An array representing the colos of the donut.|
|margin|An objetc representing all sides of the donut margin.|
|legendIconType|A string representing the type of icon to be displayed next to the text in the legend.|
|legendAlign|A string representing the alignment of the legend on the x-axis.|
|verticalLegendAlign|A string representing the alignment of the legend on the y-axis.|
|legendLayout|A string representing the direction of the legend.|
|legendMargin|An objetc representing all sides of the legend margin.|
|showLegend|A boolean representing whether or not to display the legend.|
|showTooltip|A boolean representing whether or not to display the tooltip.|
|legendWrapperStyle|An object representing the style of the text inside donut.|
|textAnchor|A string representing the anchor of the text inside donut.|
|textFill|A string with hexadecimal color represeting the color of the text inside donut.|

```javascript
  options = {
    width : 0.65,
    height : 0.5,
    cx: 0.23,
    cy: 0.2,
    innerRadius: 0.13,
    outerRadius: 0.2,
    value: "Months",
    strokeIndex: 1,
    strokeWidth: 8,
    colors: [
     "#57A602",
     "#FF4B4B",
    ],
    margin: {
     top: 5,
     right: 0,
     bottom: 5,
     left: 0
    },
    legendIconType: "line",
    legendAlign: "right",
    verticalLegendAlign: "middle",
    legendLayout: "vertical",
    legendMargin: {
     top: 0,
     left: 0,
     right: 30,
     bottom: 0
    },
    showLegend: true,
    showTooltip: true,
    legendWrapperStyle: { position: 'absolute' },
    textAnchor: "middle",
    textFill: "#57A602"
  }
```
### :key: dataKeys
To make sure the data is render on the component, you should enter this objetc as a prop

```javascript
dataKey = {
  name: "name",
  value: "value"
}
```

### Example 
![image](https://user-images.githubusercontent.com/42523734/181346606-42ee0fa8-9af1-43ac-9943-8254fef585d2.png)

```jsx
<PieChart 
    width={options.width || 300}
    height={options.height || 200}
    margin={options.margin}>
    <text 
    x={options.cx} 
    y={options.cy} 
    fill={options.textFill} 
    textAnchor={options.textAnchor || "middle"}
>
```

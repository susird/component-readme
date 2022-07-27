# :doughnut: DonutChart Component

:star: This component was built to be reused and modified according to the developer's preferences.
The library used to build the component was [recharts](https://recharts.org/en-US/api/PieChart)

❗To keep in mind: the component recives 3 props `` data, options, dataKeys``

 The best way to enter the data to be exported as prop to avoid a rendering error is as follows:
 
### :memo:  Data Format
```
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
```
  options = {
    width : 300,
    height : 200,
    cx: 100,
    cy: 80,
    innerRadius: 45,
    outerRadius: 60,
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

```
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

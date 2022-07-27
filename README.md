# :doughnut:DonutChart Component:doughnut:

2

:star:This component was built to be reused and modified according to the developer's preferences.

To keep in mind: the component recives 3 props
3
The best way to enter the data to avoid a error render is in this way:

### data format

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
31
###​options format
To hande the style you can create this objet to modify the
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

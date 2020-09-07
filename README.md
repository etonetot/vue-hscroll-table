# vue-hscroll-table
![Vue 2.x](https://img.shields.io/badge/vue-2.x-green.svg "Vue 2 Compatible")

A big scroll table with multiple horizontall scrollbars for vue2. 

The problem with big tables is the horizontal scrollbar is placed at the bottom of the table somewhere far far down. This component adds horizontal scrollbars inside the table.

[DEMO](https://etonetot.github.io/vue-hscroll-table/)

## Usage

#### install
`npm i --save vue-hscroll-table


#### Quickstart
```javascript
import HscrollTable from 'vue-hscroll-table'
```

```html
<hscroll-table :rows="rows" :cols="cols" />

cols: [
    {  
        key: 'carname'
    },
    {  
        key: 'price'
    },
    {  
        key: 'power'
    },
...
];

rows: [
{
    carname: 'Ford Mondeo', 
    price: '$24.000',
    power: '116 hp'
},
{
    carname: 'Ford Galaxy', 
    price: '$45.000',
    power: '234 hp',
    class: 'hilight1'   //  'hilight1', 'hilight2' or your class
},
{
    class: 'scrollrow'    // row with horizontal scrollbar
},
....

]

```




## License
MIT





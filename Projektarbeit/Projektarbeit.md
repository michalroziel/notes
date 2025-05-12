[[Semester 4]]


## Code snippets : 

```Javascript 
const center = board.create('point', [0, 0], { name: 'Center' });  
const pointOnCircle = board.create('point', [3, 0], { name: 'Radius Point' });  
  
board.create('circle', [center, pointOnCircle], { strokeColor: 'blue' });

```


## Dynamic Projecting of Compass Labels 
```JavaScript

const compassLabels = [  
    { label: 'N', azimuth: 0 },  
    { label: 'E', azimuth: 90 },  
    { label: 'S', azimuth: 180 },  
    { label: 'W', azimuth: 270 }  
];


for (const dir of compassLabels) {  
    const { x, y } = convertCoordination({ azimuth: dir.azimuth, altitude: 0 }); // Altitude 0 = horizon  
    const r = 1.3;  
    board.create('text', [x * r, y * r, dir.label], {  
        fontSize: 18,  
        cssStyle: 'font-weight: bold;',  
        anchorX: 'middle',  
        anchorY: 'middle'  
    });  
}
```

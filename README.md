# Google Ad Manager for Vue
Vue.js plugin to easy implement google ad units to your SPA


## Installation

**Install**

```
npm install google-ad-manager-vue
```
*or*
```
yarn add google-ad-manager-vue
```

**Import and use the plugin in your main.js or entry file** 
You must pass in your network code and mappings. Sizes object is optional. Example below. 

```javascript
import AdManager from 'google-ad-manager-vue';

let mappings = {
	banner:[
		{ window :[0,0], sizes: [ [320,50] ] },
		{ window :[980,0], sizes: [ [720,60],[728,90] ] }
	],
	rectangle:[
		{ window: [0, 0], sizes: [ [300, 250] ] },
        { window: [980, 0], sizes: [ [300, 250] ] }
	]
}

let sizes = {
	banner: [ [720, 60],[728, 90],[320, 50] ],
	rectangle: [ [300, 250] ]
};

Vue.use(AdManager, {
    id: 'ad-manager-network-code',
	mappings,
	sizes //optional
});
```

**Params**

| Title  | Description  | Type  | Required  |
| ------------ | ------------ | ------------ | ------------ |
| mappings  | Mapping sizes object  | object  | true  |
| sizes  | Google ad unit sizes  | object  | false  |


## Use
Now you can use the google ad component throughout your application. There are a few params you can pass through for customization

```html
<google-ad unit="AdUnitName"></google-ad>
```

**Params**


| Title  | Description  | Type  | Required  |
| ------------ | ------------ | ------------ | ------------ |
| unit  |  Ad unit name from ad manager  | string  | true  |
| id  | Div id tag - used to identify ads  | string  | false  |


## Contributing

Pull requests welcomed!

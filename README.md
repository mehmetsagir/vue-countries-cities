# VueJS Countries Cities

List of countries and cities made for Vue.js <br>

<p>
  <a href="https://www.npmjs.com/package/vue-countries-cities"><img src="https://img.shields.io/npm/dm/vue-countries-cities.svg?sanitize=true" alt="Downloads"></a>
  <a href="https://www.npmjs.com/package/vue-countries-cities"><img src="https://img.shields.io/npm/v/vue-countries-cities.svg?sanitize=true" alt="Version"></a>
  <a href="https://www.npmjs.com/package/vue-countries-cities"><img src="https://img.shields.io/npm/l/vue-countries-cities.svg?sanitize=true" alt="License"></a>
</p>

✨ **Live Demo ->** [vue-countries-cities](https://vue-countries-cities.vercel.app/)

## Getting Started
These instructions will get you a copy of the component up and running on your local machine.

### Installing

You can install vue-countries-cities component by npm

```shell
npm install --save vue-countries-cities
```

After download vue-country-cities package will be ready to use in your vue.js applications

### Usage

- Export to main.js to define the vue-country-cities component globally.

```js
import vueCountriesCities from "vue-countries-cities";
```

- Register vue-country-cities component with any name you want

```js
Vue.component("countriesCities", vueCountriesCities);
```
After this step, it can be used by all registered components in your project by tag name.

- To save as a singular
By coming to the page you want to use
```js
import vueCountriesCities from "vue-countries-cities";
``` 
After importing the package, you can add and use it like a regular component.
```vue
components: { vueCountriesCities }
``` 
- The city and country you select is sent to you every time a change is made.
You can keep the country and city of your choice in a variable you specify.
```vue
<template>
    <vueCountriesCities @country='selectedCountry = $event' @city='selectedCity = $event'  />
</template>

<script>
import vueCountriesCities from "vue-countries-cities";
export default{
    data () {
        return {
            selectedCountry: '',
            selectedCity: ''
        }
    },
    components: { vueCountriesCities }
}
</script>
```
- To list countries only
```vue
  <vueCountriesCities @country='selectedCountry = $event' :city='false' />
```

- For the forming process <br/>
Main template structure 
```vue
<template>
  <div class="countries-cities">
  
    <div class="select-box">
      <select class="countries">
        <option><option>
      </select>
      <svg></svg>
    </div>

    <div class="select-box">
      <select class="cities">
        <option><option>
      </select>
      <svg></svg>
    </div>
  
  </div>
</template>
```
Default css codes
```scss
.countries-cities {
  display: flex;
  justify-content: space-around;
  box-sizing: border-box;
  .select-box {
    height: 40px;
    min-width: 300px;
    background: #fff;
    border: 1px solid #e9e9e9;
    position: relative;
    select {
      background: none;
      border: none;
      outline: none;s
      padding-left: 7px;
      padding-right: 65px;
      appearance: none;
      width: 100%;
      height: 100%;
    }
    svg {
      position: absolute;
      right: 0;
      top: 0;
      width: 50px;
      height: 100%;
      background: darken(#fff, 3%);
      pointer-events: none;
      box-sizing: border-box;
      padding: 5px;
      path {
        fill: rgba(black, .7);
      }
    }
  }
}
```

## Deploy on Vercel
You can visit [vercel.com](https://vercel.com/) for details.

## Versioning

We use [GitHub](https://github.com/mehmetsagir/vue-countries-cities) for versioning.

## Authors

- **[Mehmet Sağır](https://github.com/mehmetsagir)**

## License

Licensed under the MIT license, see [LICENSE](https://github.com/mehmetsagir/vue-countries-cities/blob/master/LICENSE) for details.


[![npm](https://img.shields.io/npm/dt/vue-product-zoomer.svg)](https://www.npmjs.com/package/vue-product-zoomer)
[![GitHub issues](https://img.shields.io/github/issues/akulubala/vue-product-zoomer.svg)](https://github.com/akulubala/vue-product-zoomer/issues)
[![GitHub license](https://img.shields.io/github/license/akulubala/vue-product-zoomer.svg)](https://github.com/akulubala/vue-product-zoomer/blob/master/LICENSE)

# vue-product-zoomer

>  Vue Product Image Zoomer Package, Useful For e-Shop Project.
>  Demo: https://akulubala.github.io/vue-product-zoomer/

## Instruction 

# install 
npm install vue-product-zoomer

# Import
import ProductZoomer from 'vue-product-zoomer'

# Usage
<ProductZoomer
  :base-images="images"
  :base-component-class="ComponentClass"
  :base-zoomer-options="zoomerOptions"
/>


# Options

### images:
```javascript
{                                               
    {                                                           
      'thumbs':    // optional, if not present will use normal_size instead                           
      [                                        
        {'id':'unique id', 'url': 'image url'},
        {'id':'unique id', 'url': 'image url'} 
      ]                                         
    },                                             
    {                                             
      'normal_size':  // required                          
      [                                             
        {'id':'unique id', 'url': 'image url'},      
        {'id':'unique id', 'url': 'image url'}       
      ]                                               
    },                                                
    {                                                 
      'large_size':    //optional, if not present will use normal_size instead                              
      [                                               
        {'id':'unique id', 'url': 'image url'},       
        {'id':'unique id', 'url': 'image url'}                  
      ]                                        
    }                                          
 }               
```
### ComponentClass  (optional)

A string added to zoomer component
### zoomerOptions
```javascript
{
	'zoomFactor': 3, // scale for zoomer
	'inlinePane': false, // default is false, if set to true, zoomer_container_id must preset
	'hoverDelay': 300, // how long after the zoomer take effect
	'namespace': 'zoomer', // add a namespace for zoomer component, useful when on page have mutiple zoomer 
	'zoomer_container_id': 'zoomer', // when not inlinePane must present, container must have a fixed width and size otherwise will not show zoomer take effect
	'move_by_click':false // move image by click thumb image or by mouseover
}
```
# Example
```javascript
export default {
  name: 'app',
  data () {
    return {
      'images': {
          'thumbs': [
            {
              'id': 1,
              'url': 'http://yoohooworld.com/images/vue-product-zoomer/images/thumbs/1.jpeg'
            },
            {
              'id': 2,
              'url': 'http://yoohooworld.com/images/vue-product-zoomer/images/thumbs/2.jpeg'
            }
          ],
          'normal_size': [
            {
              'id': 1,
              'url': 'http://yoohooworld.com/images/vue-product-zoomer/images/normal_size/1.jpeg'
            },
            {
              'id': 2,
              'url': 'http://yoohooworld.com/images/vue-product-zoomer/images/normal_size/2.jpeg'
            }
          ],
          'large_size': [
            {
              'id': 1,
              'url': 'http://yoohooworld.com/images/vue-product-zoomer/images/large_size/1.jpeg'
            },
            {
              'id': 2,
              'url': 'http://yoohooworld.com/images/vue-product-zoomer/images/large_size/2.jpeg'
            }
          ]
      },
      'ComponentClass': 'col-xs-4 col-lg-4 col-md-4 col-sm-4',
      'zoomerOptions': {
        'zoomFactor': 3,
        'inlinePane': false,
        'hoverDelay': 300,
        'namespace': 'zoomer',
        'zoomer_container_id': 'zoomer',
        'move_by_click':false
      }
    }
  },
  components: {
    ProductZoomer
  }
}

```

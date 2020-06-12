## Customization/Configuration [WIP]

> The configurations works very similar to tailwindcss with few exceptions. Details about configuring or extending the default theme object can be found [here](https://tailwindcss.com/docs/configuration)

A CLI utility is in progress for handling configs better. Currently, the config object should be pass to `window` object in `index.html` file.

### Example: 

Add this script tag to the head of index.html before React is invoked.

```html
<script>
    window.__STYLED_WIND_CUSTOM_CONFIG__ = {
        theme: {
            extend: {
                colors: {
                    cyan: '#9cdbff'
                },
            }
        }
    };
</script>
```

Now the extended color cyan will be available in all possible css classes as below

```js
import styled from 'styled-wind'

const CustomColor = styled.div`
    # Background color - cyan
    .bg-cyan;
    # Border color - cyan
    .border-cyan;
    # text color - cyan
    .text-cyan;
`;
```

Everything works out of the box.
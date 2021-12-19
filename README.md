# StoryUI
An open source component library.

Each component consists of an html and a preview png file.

Feel free to submit new components.

## How to create an component

Components are created by extending the html markup with custom attributes.

| Attribute      |Description                    |Example                      |
|----------------|-------------------------------|-----------------------------|
|data-sui-component="[COMPONENT NAME]"| REQUIRED: must be included in the root of the component. Can also applied a style tag. The component name is structured  like this `[CATEGORY]-[SUBCATEGORY]-[VARIANT]`. The structure is important to for the editor to render your component in the right row.            |```html
<div data-sui-component="marketing-hero-bigtext"><div>My hero text</div>
</div>```            |



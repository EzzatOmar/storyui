
# StoryUI
An open source component library.

Each component consists of an html and a preview png file.

Feel free to submit new components.

All components can be found in /components.



## How to create an component

Components are created by extending the html markup with custom attributes.

| Attribute      |Description                    |Example                      |
|----------------|-------------------------------|-----------------------------|
|data-sui-component="[COMPONENT NAME]"| REQUIRED: must be included in the root of the component. Can also applied a style tag. The component name is structured  like this `[CATEGORY]-[SUBCATEGORY]-[VARIANT]`. The structure is important to for the editor to render your component in the right row.            |``` <div data-sui-component="marketing-hero-bigtext"><div>My hero text</div></div>```            |
|data-sui-text="Label" | Edit the innerText from the GUI. | ```<div data-sui-text="Change me">Text</div>```|
|data-sui-html="Label"| Edit the innerHTML from the GUI.| ```<div data-sui-html="Change the html"><div style="background: red">RED</div></div>```
|data-sui-bind:[attr].[optional modifier]="Label"| Edit any attribute from the GUI. On default the edit will appear as a text input but you can also add additional constraints as modifiers. Modifiers: bool, multi, enum.| ```<a data-sui-bind:href="Change the link">Link</a>``` <br /> <br /> ```<input data-sui-bind:checked.bool="Check the checkbox">Checkbox</input>``` <br /> <br /> ```<div data-sui-bind:class.multi="Add any of these classes\|text-lg|bg-red-500|underline">Div box</div>``` <br /> <br /> ```<div data-sui-bind:class.enum="Add one of these classes|text-lg|bg-red-500|underline">Div box</div>```
| | |



You can sync multiple elements by setting the exact same attribute. For example you have two different navigation panels for mobile and desktop but the href should always be the same. Then by setting ```data-sui-bind:href="Item link 1"``` to both a tags will render only one control for multiple elements in the code.

<p align="center"><img src="/hero.jpg" alt="Screenshot storyui"></p>

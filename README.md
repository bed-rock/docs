# Bedrock Docs

Bedrock is a mobile friendly component Framework based on polymer 1.0. We provide the following custom elements ready to use.

Because our framework is build on the top of webcomponents, the webcomponents.min.js and polymer.html are required.

The webcomponents.js is placed in the head of your html document, before any Bedrock´s component.
`<script src="../../webcomponentsjs/webcomponents-lite.min.js"></script>`

##Bedrock CSS framework##
A wrapper for our custom elements, that includes built in css reset, typography, grids, list and tables.

##br-browser-update##
Plugin Stand Alone that blocks user´s access who utilizes old browsers with no flexbox support.

###Use###
Copy and past into your html the following files:

`<link rel="stylesheet" type="text/css" href="../br-browser-update/dist/br-browser-update.css">`

`<script type="text/javascript" src="../br-browser-update/src/br-browser-update.js"></script>`

##br-dropdown-list##
A dropdown list that receives an icon, text or both as title.

###Tag Usage###
`<br-dropdown-list></br-dropdown-list>`
Attributes:
- position="right" // Align br-select-box in right (??)
- icon="br-icons:user" (Icon from br-icons)
- label= String

##br-apps-navigation##
A menu that integrates different applications in the same system.

External File needed:
`<link rel="import" href="../src/br-apps-navigation.html">`

###Tag Usage###
`<br-apps-navigation></br-apps-navigation>`
Attributes:
- button-check: Type: Boolean
- Required: false
- options: Type: Array of objects with name, img and link properties.
- Description: Collection of object with key and value to populate
- Required: true

##br-page-header##
Custom header for current page.

External file needed:
`<link rel="import" href="../../br-page-header/src/br-page-header.html">`

###Tag Usage###
`<br-page-header></br-page-header>`
Atributes:
- text: type:String (Page Title)
- icon: "br-icons: iconName"
- tooltip: type: String (Tooltip Text)

##br-icons##
A set of icons made with iron-iconset provided by Polymer 1.0

external files needed:

`<link rel="import" href="../src/br-icons.html">`
- iron-icon.html downloaded from polymer components page.
- iron-iconset-svg.html downloaded from polymer components page.

###Tag usage###
`<br-icons></br-icons>`
Atributes:
- class: String (icon__2lg, icon__lg, icon__sm, icon__md)
- icon: "br-icons:iconName" [full list of icons available here](example.com.br)

#br-select-box##
Mobile-friendly wrapper for br-select.

###Tag Usage###
`<br-select></br-select>`

##br-select##
A mobile-friendly select box component with search and multi select options
It needs br-select-box component to work.
External file needed:
`<link rel="import" href="../src/br-select.html">`

###Tag Usage###
`<br-select></br-select>`
Attributes:
- model: Type: Array
- options: Type: Array
- Required: Type: Boolean
- multiselect: Type: Boolean
- Desription: Set if br-selectbox is multiselect.
- Default value: false

Usage Example: `<br-select`
                  `model={{value}}`
                  `label="Selecione"`
                  `options='[{"key": 1, "value": "Judith"}, {"key": 2, "value": "Marie"}, {"key": 3, "value": "Joseph"}, {"key": 4, "value": "John"}]'>`
                `</br-select>`

##br-modal##
A modal wrapper fired by on-click event

external file needed:
`<link rel="import" href="../src/br-modal.html">`

###Tag Usage###
`<br-modal>`
  `<div class="body"> Modal Body </div>`
  `<div class="footer"> Modal Footer </div>`
`</br-modal>`

##br-input##
Input custom tag.

External file needed:
`<link rel="import" href="../src/br-input.html">`

###Tag usage###
`<br-input></br-input>`
Atributes:
- Name: String
- Label: String
- Model: 'SomeValue'?
- Min, max: Defines min/max field's caracthers
- is-valid: String true or false (why?)
- not-empty-error-message: String
- min-length-error-message: String
- custom-error-message: String
- required: Used makes the field required

##br-checkable##
Checkbox and radio inputs.

External file needed:
`<link rel="import" href="../src/br-checkable.html">`

###Tag Usage###
`<br-checkable></br-checkable>`
- label: String,
- checkbox: Boolean,
- radio: Boolean,
- name: String, In case of radio group
- required: Boolean,
- errorMessage: String,

##br-button##
A button custom element made with Polymer.

External file needed:
`<link rel="import" href="../br-button/src/br-button.html">`

####Tag usage####
`<br-button></br-button>`
Atributes:
- Class: small, large
- Label: Label name
- icon: iconUrl
- is-disabled: If assigned to a br-button tag, it creates a disabled button

##br-form##
A wrap for br-input, br-checkable and br-button, making viable build entire forms with our custom elements.

External file needed:
`<link rel="import" href="../src/br-form.html">`

###Tag Usage###
`<br-form></br-form>`
Atributes:
- action: String,
- autocomplete: String,
- method: String

##br-nav##
A mobile-friendly on click side menu with "sandwich" icon

external file needed:
`<link rel="import" href="../src/br-nav.html">`

###Tag Usage###
`<br-nav></br-nav>`
Atributes:
- items: Array.
Usage items example: `[{ "label":"Gerencial", "link":"#", "group":"true"},`
        `{ "label":"Patrimônio", "link":"#", "icon":"br-icons:user",`
        `"submenu":[`
        `{"label":"Item 01.1", "link":"#"},`
        `{"label":"Item 01.2", "link":"#"},`
        `{"label":"Item 01.3", "link":"#"}`
        `]}`

##br-header##

A header wrap divided by content position

External file needed:
`<link rel="import" href="../../br-header/src/br-header.html">`

###Tag Usage###
`<br-header>`
`  <div class="group__left"></div>`
`  <div class="group__center"></div>`
`  <div class="group__right"></div>`
`</br-header>`

##br-search##
Search input field

###Tag Usage###
`<br-search></br-search>`

##br-page##
framework´s Page model with navbar, apps navigation, input search and body
It has dependency on br-nav, br-apps-navigation, br-search, br-icons, br-dropdown-list, br-button, br-page-header, br-header, br-input

External file required:
`<link rel="import" href="../../br-page/src/br-page.html">`

###Tag Usage###
`<br-page></br-page>`
Atributes:
- navOptions: Array
- apps: Array
- accountOptions: Array






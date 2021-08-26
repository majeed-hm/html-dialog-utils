# Html Dialog Utils

[![CI Build](https://github.com/axonivy-market/html-dialog-utils/actions/workflows/ci.yml/badge.svg)](https://github.com/axonivy-market/html-dialog-utils/actions/workflows/ci.yml)

Axon Ivy's **Html Dialog Utils** is a collection of useful utilities to help you with the implementation of the HTML Dialogs.

# ReadOnlyModeListener
It is a PhaseListener that will loop through all the sub UI components included within the main parent component and apply the following:
* all the input components and links will be disabled
* all the buttons will not be rendered
* all data tables will not be editable
* all components having the style class "doNotRenderInReadOnlyMode" will not be rendered
* all components having the style class "doNotDisable" will not be disabled

## Setup

   In the XHTML page, you can add the JSF phaseListener element like following:

   ```
   
        <f:phaseListener binding="#{readOnlyModeListener}" />
   
   ```
   
* By default, the ReadOnlyModeListener is disabled and the main parent component id is "form".
* To activate it, you can set the parameter isEnabled=true.
* To specify the main parent component id, you can set the parameter ContainerId.

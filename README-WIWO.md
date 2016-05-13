# Widget Works customisations

This is a customised version of `ui-select`.

Changes are:

 1. Include only bootstrap templates (remove "select2" and "selectize" templates because we don't use them.
 
 2. Remove multi-select templates and directives to save filesize (we don't use them and they add complexity).
 
 3. Build a "no-template" version of the library to save filesize and allow downstream projects to include their own custom templates.
 
 4. Turn off automatic resizing of the filter input control - allow downstream projects to control size through CSS.
 
 5. Add the "uis:focusSearch" event to choose whether the input field is focussed when the menu is opened. When this event is raised, if any listener calls `event.preventDefault()` then we will not set focus on the filter input field. Otherwise, if default has not been prevented we will set focus as normal after opening.


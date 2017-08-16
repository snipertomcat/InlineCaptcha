# SilentCaptcha
An open source package (as well as a specific Laravel  that will "silently" validate CAPTCHA responses inline on a standard HTML element rather than a separate CAPTCHA form field, eliminating an entire step in the form.

## Abstract
An open source package that would allow the processing of CAPTCHA's inline with any other valid form element, and using that user response as a means to validate the CAPTCHA. It basically will auto attach itself to any of the following form fields and act as if the click on it was made inside a separate CAPTCHA form element.
t
The valid html elements that an inline auto-CAPTCHA target can be attached to (and therefor validated with):

1. any standard button, anchor or clickable link
	`<div class="btn"...`
	`<a href=...`
2. checkboxes 
  `<input type="checkbox"`...
3. radio buttons
  `<input type="radio"...`
4. selects & dropdowns
  `<select ...`
  `<div class='dropdown'`
5. any clickable area on the page itself
	`<* onclick=""...`

Basically, the idea is to have the actual CAPTCHA input actually be attached to a **clickable** element on the page, thereby needing no further interaction from the user other than the original click, at which point it validates silently in the background. 

There are several possibilities to go about doing this. One would be to somehow mimick (what would be the click) on the actual CAPTCHA input field.


### Possible issues and potential hurdles

- The CAPTCHA probably has some script or element that MUST be displayed on the page in order for it to be able to authenticate with the CAPTCHA server to verify a human clicked the CAPTCHA checkbox.

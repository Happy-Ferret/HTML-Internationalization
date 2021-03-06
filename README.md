# HTML-Internationalization
### HTML Internationalization for WebExtensions
The code is modular so it can be used verbatim without any need for any change. It can be used for Options pages, Browser Action pop-ups, Page Action pop-ups, Sidebar or any other HTML document.

The Internationalization is done by adding a `data-i18n` attribute to the elements.

If `data-i18n` does not have a `|` then the localised message will be appended to the node as TEXT.  
If `data-i18n` has a `id|attribute` then the localised message will be set to the node attribute.

**N.B.** The Internationalization is added as TEXT as I believe locales should not contain HTML.

### Examples
`<p data-i18n="someText"></p>` -->  
`<p data-i18n="someText">someText Message</p>`

`<p data-i18n="someText"><img src="" alt=""> </p>` -->  
`<p data-i18n="someText"><img src="" alt=""> someText Message</p>`

`<p><span data-i18n="someText"></span></p>` -->  
`<p><span data-i18n="someText">someText Message</span></p>`

Passing to a `value` or any other attribute:  
Just add the attribute name after `|`

`<input type="button" data-i18n="someText|value" value="">` -->  
`<input type="button" data-i18n="someText|value" value="someText Message">`

### Further Development
So far, I have not come across a situation that couldn't be handled (or made to be handled) by the code. Let me know of such instances and I will update the code accordingly.

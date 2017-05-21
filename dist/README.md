## HTML Panel for Grafana

The HTML Panel can load external content into the dashboard.  This allows to load html content using an \<iframe\> or using ajax inside a \<div\> tag.
  
Allows using templateVariables inside URLs and params

Forked from rayntxu's AJAX panel : https://github.com/ryantxu/ajax-panel

Thanks to rayntxu for his work!

### Options

- **Method**:

  GET / POST / iframe

- **URL**:

  The URL to request
  
- **Auth**:

  TODO: Add auth methods  

- **Parameters**:

  The parameters that will be passed in the request.  This is a javascript object with access to the variables:
  - `ctrl` The control object.
  
  Sample Parameters:
	```
	{
	 from:ctrl.range.from.format('x'),  // x is unix ms timestamp
	 to:ctrl.range.to.format('x'), 
	 height:ctrl.height
	}
	```


### Screenshots

- [Screenshot of the options screen](https://raw.githubusercontent.com/ryantxu/ajax-panel/master/src/img/screenshot-ajax-options.png)

#### Changelog

##### v0.0.3

- Added option to show the URL's content as an <iframe\>
- Support for template variables 

### Roadmap... hopefully soon
 - Toggle the 'spinner' for panel
 - Get the panel width?
 - Error handling
 - avoid the 'Data source query result invalid, missing data field: undefined' error message


### Wishlist... if you are looking for a project :)
 - Add authentication info to the sub-request?
 - Configure timer to refresh
 - Load CSS file?
 - configure javascript for display
 - why does the `Time range` > `Override relative time` not work?
 - Check that parameters have changed before sending a new request

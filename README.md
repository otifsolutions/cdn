# Generic Form Submit
## CDN URL
`https://cdnotif.b-cdn.net/js/gfs.min.js`
## Requirements
jQuery
Toastr
## Target
All Form tags
## Special Tags
- `no_generic` Add this as a class on form to DISABLE this js.<br>
- `button[type='submit'] i` OR `a[href='#finish'] i` Elements define the loading attribute that should have `d-none` class to toggle loading.<br>
- `button[type='submit']` OR `a[href='#finish']` Elements should be the form's submit trigger so that these are disabled and enabled automatically.<br>
## Response Tags Available
```
{
  "modal": "#modal_id",
  "feed" : "/url/to/fetch/modal", //If Modal is set
  "message" : "Success Message",
  "location" : "/redirect/to/this/location" //If this is set modal will not work
}
```
## Error Response
```
{
  "Errors": [
    "Any Heading" : "This is error 1",
    "Any Heading 2": "This is error 2"
  ]
}
```
# Generic Change Status
## CDN URL
`https://cdnotif.b-cdn.net/js/gcs.min.js`
## Requirements
jQuery
Toastr
Swal
## Target
On click of the element with the data tag `[data-toggle="change-status"]`
## Special Tags
- `data-feed` This data tag defines the feed for where to send the POST call.<br>
- `data-msg` This data tag defines the Message to show in the swal<br>
## Response Tags Available
```
{
  "message" : "Success Message",
  "location" : "/redirect/to/this/location"
}
```
## Error Response
```
{
  "Errors": [
    "Any Heading" : "This is error 1",
    "Any Heading 2": "This is error 2"
  ]
}
```
# Model Feed
## CDN URL
`https://cdnotif.b-cdn.net/js/mf.min.js`
## Requirements
jQuery
Toastr
## Target
On click of the element with the data tag `[data-toggle="modal-feed"]`
## Special Tags
- `data-target` This data tag defines the target id for the model to get the data in their `.modal-content` div.<br>
- `data-feed` This data tag defines the feed url from where to get the data to add to the modal's content div.<br>
## Response Tags Available
```
{
  "message" : "Success Message",
  "location" : "/redirect/to/this/location"
}
```
## Error Response
```
{
  "Errors": [
    "Any Heading" : "This is error 1",
    "Any Heading 2": "This is error 2"
  ]
}
```
# Delete Feed
## CDN URL
`https://cdnotif.b-cdn.net/js/df.min.js`
## Requirements
jQuery
Toastr
Swal
## Target
On click of the element with the data tag `[data-toggle="delete-feed"]`
## Special Tags
- `data-feed` This data tag defines the feed url from where the DELETE call will be sent.<br>
- `data-msg` This data tag defines the Message body of the swal default : `You won't be able to revert this!` <br>
- `data-confirm-button-text` This data tag defines the Confirm Button text : `Yes, remove it!` <br>
- `data-swal-cancel-text` This data tag defines the text for cancel swal : `The record has not been deleted.` <br>
- `data-swal-confirm-text` This data tag defines the text for confirm swal : `The record has been deleted.` <br>
- `data-swal-confirm-title` This data tag defines the title for confirm swal : `Deleted!` <br>
## Response Tags Available
None, It will reload the page by default after success response.
## Error Response
```
{
  "Errors": [
    "Any Heading" : "This is error 1",
    "Any Heading 2": "This is error 2"
  ]
}
```
# Post Feed
## CDN URL
`https://cdnotif.b-cdn.net/js/pf.min.js`
## Requirements
jQuery
Toastr
Swal
## Target
On click of the element with the data tag `[data-toggle="post-feed"]`
## Special Tags
- `data-feed` This data tag defines the feed url where the POST call will be sent.<br>
- `data-title` This defines the title for the swal. Default : `Are you sure?`<br>
- `data-text` This defines the text(html supported) for the swal. Default : `This cannot be undone`<br>
## Response Tags Available
```
{
  "message" : "Success Message",
  "location" : "/redirect/to/this/location"
}
```
## Error Response
```
{
  "Errors": [
    "Any Heading" : "This is error 1",
    "Any Heading 2": "This is error 2"
  ]
}
```
# Generic Chart [ApexChart.js]
## CDN URL
`https://cdnotif.b-cdn.net/js/gc.min.js`
## Requirements
jQuery
ApexChart
## Target
All elements with the data tag `[data-toggle="generic-chart"]`
## Special Tags
- `data-type` Required Tag. The type of the chart. <br>
- `data-colors` Required Tag. The colors of the chart comma seperated.<br>
- `data-height` Optional Tag. The height of the chart. Default : `100` <br>
- `data-stroke-width` Optional Tag. The Stroke width of the chart can be comma seperated. Default : `2.5` <br>
- `data-series` Optional Tag. Default Data series for the chart. Default : ` ` <br>
- `data-no-data` Optional Tag. The text to show when there is empty/no data. Default : `Not Enough Data` <br>
- `data-y-axis-format-type` Optional Tag. Use this to enable formating as currency. Support Value : `money` <br>
- `data-currency` Optional Tag. The currency sign to use in the money formator. Default is ` ` <br>
- `data-labels` Optional Tag. The default labels to populate the chart <br>
- `data-x-axis-labels-colors` Optional Tag. The colors for the xaxix labels can be comma seperated <br>
- `data-y-axis-labels-color` Optional Tag. The color for the yaxix labels <br>
- `data-grid-border-color` Optional Tag. The color for the grid border. <br>
- `data-stacked` Optional Tag. Set to enable stacked chart to be true <br>
- `data-fill-opacity` Optional Tag. The fill opacity for the chart <br>
- `data-stroke-dash` Optional Tag. The stroke for dashed chart can be comma seperated <br>
- `data-legend-position` Optional Tag. The position for the legends <br>
- `data-legend-show` Optional Tag. Enable legends by this tag <br>
- `data-fill-gradient` Optional Tag. To set the fill gradient of the chart. Must use fill-gradient-colors if you use this. <br>
- `data-fill-gradient-colors` Optional Tag. The colors for the gradient fill. Can be comma seperated <br>
- `data-feed` Optional Tag. Set this to use feed ajax for updating the chart's options or data or labels. <br>
## Response Tags Available If feed is set
```
{
  "keys": ["name1","name2"],
  "values" : [
    {
      "name": "Name1 of series",
      "data": [1,2]
    },
    {
      "name": "Name2 of series",
      "data": [1,2]
    }
  ]
  "options" : {
    //Complete Apexchart options can be used to update chart options here.
  }
}
```
## Error Response
```
Not supported
```

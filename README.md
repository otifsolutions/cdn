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

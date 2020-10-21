# Read: 13 - Update/Delete

* [Sending Form Data](https://developer.mozilla.org/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data)
on the client side - to define how to send the data we use action property of form and the method
  * to view http requests:
    * Open the developer tools.
    * Select "Network"
    * Select "All"
    * Select "foo.com" in the "Name" tab
    * Select "Headers"
  * sending files:
    * set the method to post
    * set the value of enctype to multipart/form-data
    * input one or more \<input type="file"> controls to let users select files to upload.
  * Security issues:
    * be paranoid, never trust your users
      * escape dangerous characters
      * limit amounht of incoming data to what's necessary
      * sandbox uploaded files

## Additional Resources

* [HTML5 Forms Reference](https://htmlreference.io/forms/)
  Pay special attention to the “action” and “method” attributes.

## Videos

[Video Series on Styling HTML5 Forms](https://www.youtube.com/playlist?list=PL4cUxeGkcC9g5_p_BVUGWykHfqx6bb7qK)
Note that this video series is approximately 40 minutes long. You do not need to watch every video from the series, but should keep it handy for reference as you style your book app during lab time.

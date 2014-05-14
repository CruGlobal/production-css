Production CSS
==============

This is the process to follow before our css is move to production. 

####1. [SCSS Lint](https://github.com/causes/scss-lint)

The scss-lint config file can be found in the main styles folder. There are a series of tests to run on the files that can be turned off/on in this file. I reccommend running them one at a time. 

Run the following in the command line:

    scss-lint --config path/to/styles/scss-lint.yml path/to/styles

####2. [CSS Lint](http://csslint.net/)

We will get yelled at for some things we cannot avoid such as multiple header declarations but shoot for as few warnings as possible. 

####3. _Make sure the file is compressed_. Seriously with all our comments this is huge. 

####4. Timestamp the file for caching. 

####5. Make sure the file is gripped and cached on the server side

Our target goal for total page size is 200K. Also remember the total number of objects or http-request must be kept low. See [Chris Coyier's post on ideal page size for quick loading pages](http://css-tricks.com/what-is-the-ideal-page-size-for-quick-loading-pages/) for a detailed explanation. 

Run pages through [Google's page speed anaylsis](http://developers.google.com/speed/pagespeed/insights/) and [websiteoptimization.com](http://www.websiteoptimization.com/services/analyze/)

A similar process should be followed for compressing html, javascript, images, etc. 




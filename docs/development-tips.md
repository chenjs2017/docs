# Development tips

---

Any changes that you have made in modules need to be copied to the WebHost to be loaded. You can do this in several ways:

- Build SimplCommerce.WebHost which will trigger the "copy-modules" gulp task
- Manually run the "copy-modules" gulp task in the Task Runner Explorer
- If your changes are only static content like: .css, .js, .cshtml you can simply run the "copy-static" and then refresh the browser.

![Task runner](images/taskrunner.png)

The gulp file can be found at https://github.com/simplcommerce/SimplCommerce/blob/master/src/SimplCommerce.WebHost/gulpfile.js

## Build configuration

By default the "copy-modules" gulp task only copy dll from Debug folders. So if you build Release or you publish the website then you have to modify the gulp task to copy dll from release folders

![copy-modules](images/copy-modules.png)

## For Mac User 
There is no Task Runner Explorer in VS Mac, here are some workaround
- To install gulp command line tool
    $ sudo npm install gulp -g
- Go to the directory SimplCommerce/src/SimplCommerce.WebHost
    $ gulp copy-modules

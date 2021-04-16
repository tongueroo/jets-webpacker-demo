# Jets Webpacker Demo

This project demonstrates how to use webpacker with images. There several benefits to using webpack to build assets like images.

* Webpacker adds sha checksums to assets as a part of building them to the `public/packs` folder.  The checksums optimize performance since images can be cached for very long periods of time. IE: 10y.
* You'll be able to configure high values for the `max-age` response header. This article [Increasing Application Performance with HTTP Cache Headers](https://devcenter.heroku.com/articles/increasing-application-performance-with-http-cache-headers) covers how cache headers work.  The default max-age for assets serving out of s3 is 3600s or 1h.
* If you replace an image and keep the same name, you don't have to update the code as the `image_pack_tag` uses the compiled image with the sha checksum. It's nice to offload menial tasks like file renames to automation. Instead, we can spend the previous mental energy on coding business logic.

For details, see docs [Assets Serving: Webpack | How To Tutorial](https://rubyonjets.com/docs/extras/assets/webpacker/#how-to-tutorial)

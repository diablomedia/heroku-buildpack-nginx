## Heroku buildpack: Nginx

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for [Nginx](wiki.nginx.org).

Usage
-----

Example usage:

	#Copy the example/nginx.conf.erb file into your app folder:
    $ ls
	nginx.conf.erb

	#Create the heroku app, specifying this as the buildpack
    $ heroku create --buildpack https://github.com/Taytay/heroku-buildpack-nginx.git

	#deploy the app to heroku
    $ git push heroku master
    ...
    -----> Downloading Nginx Sources
    -----> Extracting Nginx Sources
    -----> Configuring
    -----> Compiling
    -----> Installing
    -----> Creating Boot Script

This buildpack will detect your app as an Nginx app if it has the file nginx.conf.erb in the root.
Nginx is downloaded to Heroku and compiled on every push. Don't worry. It doesn't take long.


Example config file
-------------------
The file example/nginx.conf.erb has an example config file that you can use to get started.
You can do a lot with Nginx, from serving static sites to load balancing. More information at
[Nginx Configuration](http://wiki.nginx.org/Configuration)


Motivations
-----------
I needed a cheap and easy way to play with Nginx. In particular, I am playing with [3Scale's Nginx API Proxy](https://support.3scale.net/howtos/api-configuration/nginx-proxy).


Credits
-------
Dan Palmer figured all of the hard stuff out:
[Heroku Buildpack For Hammer](http://danpalmer.me/blog/articles/2012-12-30-heroku-buildpack-for-hammer.html)

I'm Taylor Brown, aka [Taytay](http://taytay.com/)

fastn-test-cordova
==================

To install you will need 

* [Android SDK](https://developer.android.com/sdk/installing/index.html)
* ADP 
* Cordova CLI
* Cordova-crosswalk - which is installed for you by the `make init` command

Install cordova with:

```javascript
npm i cordova -g
```

Once you have cloned the `fastn-test-cordova` repo with `git`, `make should install all the npm dependencies with the sequence below.

```shell
>make init
```

Before your android build there appears to be a cordova glitch for which you can apply [this fix](http://stackoverflow.com/a/30240520/4830780)

Devwatch will run watchify to watch for changes to the js folder, and css

```
>make devwatch
```

In a separate termial you can then make the cordova apps.

```shell
>make build
>cordova run browser
>cordova run android -device

```

You may have to run these as sudo user depending on your node & cordova setup.

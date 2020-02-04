## theme-example for ownCloud

### Use the theme-example App

To use the `theme-example` app, clone or download this repository to the `owncloud\apps` folder on your server. Please note that the Apache user needs access rights to the folder and its content. As an example, use the following command to adjust the permissions: `chmod -R www-data:www-data theme-example`.

If you change the name of the app (the folder name) from `theme-example` to another name, be sure to change the `<id>` in the file `appinfo\info.xml` as well. The folder name and the `<id>` must be identical.

### Edit images
To edit images it is best to open the original images from the `core\img` folder with Gimp or Photoshop. After you have made changes, overwrite the originals.

Please note that the browser stores images in the cache, so this should always be deleted after changes. (https://en.wikipedia.org/wiki/Wikipedia:Bypass_your_cache)

### Change values
Please have a look at the file `defaults.php` if you want to change texts. The copyright text on the start page and other texts are well documented there.

### Change design values
In the file `core/css/styles.css` you will find the adjustments we have preconfigured for you. You can change everything you want there. More classes and their values can be found easily with the browser console (F12 key). There you can also test directly in the browser how the change of values will be reflected. If it fits you can transfer the values to `styles.css`.

### Integrity check

Since files in the theme must be changeable, it has not been signed by us. Therefore an `integrity check warning` appears in your ownCloud instance. You can deactivate it for the `theme-example` app by adding following config parameter to `config\config.php`. You can find the config directory in the root folder of your instance.

```
'integrity.ignore.missing.app.signature' => [
      theme-example,
 ],
```

### Questions
If you have any questions you can ask them on https://central.owncloud.org.

We are happy to help.

### Thanks
Sincere thanks goes to the awesome https://unsplash.org site for the background image. (Photo by Kaushik Panchal on Unsplash)

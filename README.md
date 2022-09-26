# Umbraco - Sort those crops out!

## Nuget

`Install-Package punkCropperStyles`

https://www.nuget.org/packages/punkCropperStyles/

## Compatibility

- Umbraco 10

## Summary 

I've always though that the image cropper in Umbraco, looked a little messy and the view for the main image wasn't large enough.

![Default Cropper](https://raw.github.com/garpunkal/punkCropperStyles/main/image-cropper-unstyled.jpg)
 
So I decided to tweak the CSS and see if I can tidy it up:

![Improved Cropper](https://raw.github.com/garpunkal/punkCropperStyles/main/image-cropper-styled.jpg) 

I think this looks better and it gives the main image 100% of the area to use!

## Manual install

1 - Create the following structure in your site under app_plugins

![Folder](https://raw.github.com/garpunkal/punkCropperStyles/main/tweaks-folder.png) 

2 - Add a package.manifest with this code:

```javascript
{
  "css": [
    "~/app_plugins/tweaks/cropper.css"
  ]
}
```

3 - Add this CSS in a file called: cropper.css

```css
.imagecropper {
  display: block;
}

.imagecropper .umb-sortable-thumbnails {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  align-items: flex-start;
  width: 100%;
  overflow: auto;
  max-height: 300px;
}

.imagecropper .umb-sortable-thumbnails li {
  display: flex;
  flex-wrap: wrap;
  width: 10%;
  align-items: flex-start;
}

.imagecropper .umb-sortable-thumbnails li .crop-information {
  align-items: flex-start;
}
```

4 - Restart the Umbraco website, and the image cropper should be updated :)

If you need any help, give me a shout on [twitter](https://twitter.com/garpunkal).

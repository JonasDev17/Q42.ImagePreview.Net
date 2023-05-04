# HIS.ImagePreview.Net

This version of HIS.ImagePreview.Net has been update for .NET 5.0+

Server & Client component for creating and rendering ~200 byte images (25% of original preview size).

## Install

Include the NuGet package

    Install-Package HIS.ImagePreview
    
## Create the images

    var image = Image.FromFile("[path to your image]");
    var body = ImagePreviewConverter.CreateImagePreview(image);

Store the body (`byte[]`). This is the information that you can send to your clients.

## Render the image from the body

    ImagePreviewConverter.Base64ImageFromBody(body)
    
Don't forget to add a blur to your images.

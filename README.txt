StyleTransferNetwork is used to take a content image and add certain features from a style image without losing its original identity. VGG19's intermediate layers are necessary to define the representation of content and style from the images. For an input image, try to match the corresponding style and content target representations at these intermediate layers. It is done by backpropogating mean square error for image's output relative to each target, then take the weighted sum of these losses. The changes in the content image are visible from very initial training steps. We first run gradient descent and then further optimize the image by taking weighted loss to get stronger impressions in content image.


Steps to run:
1) Bring 'StyleTransferNetwork.ipynb' and sample images(in this case 'style3.jpeg' and 'girl_with_pearl_earings.jpeg') in a folder.
2) Open the folder in jupyter.
3) vgg19 model is loaded using tf.keras.applications with weights pretrained to 'ImageNet'.
4) Run the model. You can set the path to any image you want in content_path and style_path variables.

Used tensorflow tutorials for reference.

Thank You!
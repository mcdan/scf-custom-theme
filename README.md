**Create your own custom SCF bootstrap Skin**

Steps

 1. Use a third party tool to generate a less file with all the
    customizations and specific to bootstrap. I would recommend
    https://pikock.github.io/bootstrap-magic/app/index.html#!/editor
 2. Paste the contents of the less file in
    jcr_root/etc/designs/community/sitethemes/bootstrap-custom/clientlibs/variables.less
 3. Change the thumbnail of the theme. Replace the image file at
    jcr_root/etc/designs/community/sitethemes/bootstrap-custom/image
    with your image. The thumbnails file name should be image.
 4. You can change other properties at
    jcr_root/etc/designs/community/sitethemes/bootstrap-custom/clientlibs/.content.xml
 5. Run mvn clean install to generate a zip that could be installed
    using crx package manager

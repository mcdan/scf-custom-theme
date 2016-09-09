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


** Use a Downloaded theme **
1. Clone https://github.com/arunpon/scf-custom-theme
2. Download a theme, e.g.: https://startbootstrap.com/template-overviews/clean-blog/
3. Take all the non minified js from the downloaded theme and add them to:  jcr_root/etc/designs/community/sitethemes/bootstrap-custom/clientlibs/js
4. Take all the non minified css from the downloaded theme and add them to:  jcr_root/etc/designs/community/sitethemes/bootstrap-custom/clientlibs/css
5. Add all the files in the js and css directories to their respective js.txt and css.txt, removing any existing information
6. Take all the images from the theme's img directory and add them to: jcr_root/etc/designs/community/sitethemes/bootstrap-custom/img
7. Change the jcr:description and jcr:title to match your new theme in: jcr_root/etc/designs/community/sitethemes/bootstrap-custom/.content.xml
8. Update the image file in jcr_root/etc/designs/community/sitethemes/bootstrap-custom to show a meaninful thumbnail
9. Copy the jcr_root/etc/designs/community/sitethemes/bootstrap-custom directory to a meangingful name: jcr_root/etc/designs/community/sitethemes/bootstrap-<themename>
10. Update the filter xml to include this new directory: META-INF/vault/filter.xml
11. Update the pom to give this new maven artifact a better name: pom.xml
12. mvn clean install to build
13. Install via package manager

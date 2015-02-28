# Divi Blog Module Post Order Addon

Clone the repository or fetch the patch.
```
git clone https://github.com/burlyroot/divi-blog-module-post-order.git
```
Download Divi Theme from Elegant Themes.  Current version is **2.3.1**.

Unzip your Divi Theme locally.

Place the patch in the same directory as the the newly unzipped Divi theme.

Divi was developed on Windows all the files have DOS line feeds.  I use linux/mac, so this becomes an issue with patching.  If you are on linux or mac, you will need to do the following to patch.

**Convert to-be-patched file to UNIX line endings**
```
Desktop:> cd Divi

Divi:> dos2unix functions.php
dos2unix: converting file functions.php to Unix format...

Divi:> dos2unix et-pagebuilder/et-pagebuilder.php
dos2unix: converting file et-pagebuilder/et-pagebuilder.php to Unix format...
```

**Patch the files**
```
Desktop:> cd ../

Desktop:> patch -p0 < divi-2.3.1-blog_module-post_order.patch 
(Stripping trailing CRs from patch.)
patching file Divi/et-pagebuilder/et-pagebuilder.php
(Stripping trailing CRs from patch.)
patching file Divi/functions.php
```

**Convert the patched files back to DOS line endings**
```
Desktop:> cd Divi

Divi:> unix2dos functions.php
unix2dos: converting file functions.php to DOS format...

Divi:> unix2dos et-pagebuilder/et-pagebuilder.php
unix2dos: converting file et-pagebuilder/et-pagebuilder.php to DOS format...
```


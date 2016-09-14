# aurora-bundle-files



During installation process you will need:
- Git
- Composer
- Node.js
- NMP

1. Clone aurora-core git repository into your installation root directory
  git clone https://github.com/afterlogic/aurora-core.git ./

2. Copy composer.json and modules.json from https://github.com/afterlogic/aurora-bundle-files.git

3. Download composer.phar from https://getcomposer.org/composer.phar

4. Run composer installation process by 
```bash
composer.phar install
```
from command line.

This will install modules discribed in modules.json. At this moment aurora-bundle-files repository contains configs for Files bundle biuld.

After that, you need to build static files for current module set.

First of all, install all npm modules via
```
npm install
```
Now you can buld static files
```
gulp styles --themes Default,Funny
```
```
gulp langs --langs Arabic,Bulgarian,Chinese-Simplified,Chinese-Traditional,Czech,Danish,Dutch,English,Estonian,Finnish,French,German,Greek,Hebrew,Hungarian,Italian,Japanese,Korean,Latvian,Lithuanian,Norwegian,Persian,Polish,Portuguese-Brazil,Portuguese-Portuguese,Romanian,Russian,Serbian,Slovenian,Spanish,Swedish,Thai,Turkish,Ukrainian,Vietnamese
```
```
gulp js1:min --output app
```
```
gulp js1:min --output files-pub --modules FilesWebclient
```

Now you a ready to configure you fresh installation of AfterLogic platform.

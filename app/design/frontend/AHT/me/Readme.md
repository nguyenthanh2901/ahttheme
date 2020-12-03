How to set up :
* Read file registration.php to create Vendor and ModuleName 

- B1: git clone https://github.com/butdepzai98/AHT-me.git
- B2:
    Create Block by <br>
    Insert Data in link to PhpMyAdmin <br>
    https://drive.google.com/file/d/1S2QbCdGHQYDMKCUYdbfCMMz4tNbkepKR/view?usp=sharing 
    and <br>
    https://drive.google.com/file/d/1ju6bmUEnG1E7h_HAxVo4RSfGrUrzGz9c/view?usp=sharing
    <br>
- B3: 
    Install Extendtions Megamenu
    https://drive.google.com/drive/folders/1piREG1ezucEW5YwPJYAz0eA7kx_mOvVp?usp=sharing
    
- B4: Run cmd <br>
    sudo bin/magento setup:di:compile && sudo bin/magento setup:upgrade && sudo bin/magento s:s:d -f && sudo chmod -R 777 * && sudo bin/magento c:c
    
- B5: Active Megamenu and Import file setting <br>
    Go to Admin -> VenusTheme -> Licenses <br>
    Go to Admin -> VenusTheme -> Import -> Choose File : setting.json <br>
    sudo bin/magento c:c
    
- B6:
    Go to Admin -> Content -> Configuration ->	Main Website -> Edit <br>
    Choose AHT Me <br>
    sudo bin/magento c:c
    <br>
- B7:
    Go to Admin -> Content ->Block -> New Block
    Insert All Image in link <br>
    https://drive.google.com/file/d/1u5Mv3aWav6qHJQqicnk7ZuB5uO9HAZeO/view?usp=sharing
    
- B8:
    Setup Grunt <br>
    me: {
        area: 'frontend',
        name: 'AHT/me',
        locale: 'en_US',
        files: [
            'css/styles-m',
            'css/styles-l',
            'css/email',
            'css/email-inline'
        ],
        dsl: 'less'
    }, <br>
    
    sudo chmod -R 777 * && rm -rf var/cache var/page_cache var/view_preprocessed/frontend pub/static/frontend/AHT && sudo bin/magento s:s:d -f --theme AHT/me && sudo chmod -R 777 * && grunt clean:me && grunt exec:me && grunt less:me && sudo bin/magento c:c && sudo chmod -R 777 * 
    

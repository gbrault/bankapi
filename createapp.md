https://nextcloud.pragmatic.site/settings/apps
validate the new app

#adding a menu to the add file
./appinfo/app.php
<?php
/**
 * @author Gilbert Brault
 * @copyright 2018 Gilbert Brault gbrault@seadev.org
 *
 * This file is licensed under the Affero General Public License version 3 or
 * later.
 * See the COPYING-README file.
 */
namespace OCA\Files_PdfViewer\AppInfo;
use OCP\Util;
Util::addScript('bankapi', 'script');

./js/script.js
var myFileMenuPlugin = {
    attach: function (menu) {
        menu.addMenuEntry({
            id: 'abc',
            displayName: t('bankapi', 'Text file'),
            templateName: t('bankapi', 'New text file.txt'),
            iconClass: 'icon-filetype-text',
            fileType: 'file',
            actionHandler: function () {
                console.log('do something here');
            }
        });
    }
};
OC.Plugins.register('OCA.Files.NewFileMenu', myFileMenuPlugin);

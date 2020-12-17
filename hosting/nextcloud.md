
Allow symlinks fix - https://github.com/nextcloud/server/issues/11879
- edit the following file in the /var/www/nextcloud/lib/private/Files/Storage/Local.php.
- edit the following line protected $allowSymlinks = false; 

Enable video previews - https://help.nextcloud.com/t/show-thumbnails-for-videos/71251/3
- Add the following to the config file
  'enable_previews' => true,
  'enabledPreviewProviders' =>
  array (
    'OC\Preview\Movie',
    'OC\Preview\PNG',
    'OC\Preview\JPEG',
    'OC\Preview\GIF',
    'OC\Preview\BMP',
    'OC\Preview\XBitmap',
    'OC\Preview\MP3',
    'OC\Preview\MP4',
    'OC\Preview\TXT',
    'OC\Preview\MarkDown',
    'OC\Preview\PDF'
  ),
- make sure the following are installed imagemagick-common, php-imagick, and ffmpeg

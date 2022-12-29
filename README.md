# ublock

Toutes les règles qui me semblent utiles



# global rules 
```sh
user@host:~# cat /usr/lib/firefox-esr/distribution/policies.json
{
 "policies": {
   "BlockAboutConfig": true,
   "3rdparty": {
      "Extensions": {
        "uBlock0@raymondhill.net": {
          "__comment": "Disable about:config access",
          "userSettings": [
            [ "colorBlindFriendly", "true" ]
          ],
          "__comment": "Define uBlock Origin filter's rules",
          "toOverwrite": {
            "filters": [
              "! To add to ublock rules",
              "! Comment supprimer la popup Connectez-vous à Youtube",
              "! https://www.malekal.com/comment-supprimer-la-popup-connectez-vous-a-youtube/",
              "www.youtube.com###dialog",
              "||www.gstatic.com/youtube/img/promos/growth/dmod_si_horizontal_ver1_240x400.png$image",
              "www.youtube.com##opened",
              "www.youtube.com##.opened",
              "",
              "! remove 'more videos' popup by youtube #325",
              "! https://github.com/udacity/fcnd-issue-reports/issues/325#issuecomment-431747308",
              "##.ytp-pause-overlay",
              "www.youtube.com##.ytp-scroll-min.ytp-pause-overlay"
            ]
          }
        }
      }
    }
  }
}
```

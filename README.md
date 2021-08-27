## handy scripts to make your life in academia a bit easier
## 1. some useful zsh scripts


## 2. enter common latex operator (`\cite{`) with just one key 
* This requires `Karabiner-Elements.app`.

* open '~/.config/karabiner/karabiner.json'  

* add a new config 
<details>
<a class="btnfire small stroke"><em class="fas fa-chevron-circle-down"></em>&nbsp;&nbsp;Show Me the Code</a>    
</summary>
This should bring up the citation list with just one quick key press. 
You can also change to other key combinations that you want.

```
{
  "manipulators": [
    {
      "description": "replace unused key (print screen) with common latex operators (cite)",
      "conditions": [
          {
              "bundle_identifiers": [
                  "^com\\.microsoft\\.rdc$",
                  "^com\\.microsoft\\.rdc\\.",
                  "^net\\.sf\\.cord$",
                  "^com\\.thinomenon\\.RemoteDesktopConnection$",
                  "^com\\.itap-mobile\\.qmote$",
                  "^com\\.nulana\\.remotixmac$",
                  "^com\\.p5sys\\.jump\\.mac\\.viewer$",
                  "^com\\.p5sys\\.jump\\.mac\\.viewer\\.",
                  "^com\\.teamviewer\\.TeamViewer$",
                  "^com\\.vmware\\.horizon$",
                  "^com\\.2X\\.Client\\.Mac$",
                  "^com\\.vmware\\.fusion$",
                  "^com\\.vmware\\.horizon$",
                  "^com\\.vmware\\.view$",
                  "^com\\.parallels\\.desktop$",
                  "^com\\.parallels\\.vm$",
                  "^com\\.parallels\\.desktop\\.console$",
                  "^org\\.virtualbox\\.app\\.VirtualBoxVM$",
                  "^com\\.citrix\\.XenAppViewer$",
                  "^com\\.vmware\\.proxyApp\\.",
                  "^com\\.parallels\\.winapp\\."
              ],
              "type": "frontmost_application_unless"
          }
          ],
          "from": {
              "key_code": "print_screen",
              "modifiers": {
                  "optional": [
                      "any"
                  ]
              }
          },
          "to": [
              {
                  "key_code": "7",
                  "modifiers": [
                      "shift",
                      "left_option"
                  ]
              },
              {
                  "key_code": "c"
              },
              {
                  "key_code": "i"
              },
              {
                  "key_code": "t"
              },
              {
                  "key_code": "e"
              },
              {
                  "key_code": "8",
                  "modifiers": [
                      "left_option"
                  ]
              }
          ],
          "type": "basic"
       }
   ]
}
```
this will map `print_screen` to the following keys 
    `left_option`+`shift`+`7`: `\`
    `c`
    `c`
    `c`
    `c`
    `left_option`+`8`: `{`
</details>


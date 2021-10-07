## handy helper scripts to simplify boring stuff
### 1. [grab web image](grabwebimg)

### 2. enter common ![formula](https://render.githubusercontent.com/render/math?math=\LaTeX) operator with just one key 
* This requires `Karabiner-Elements.app`.
* This replaces `print_screen` with the string `\cite{`, which in common ![formula](https://render.githubusercontent.com/render/math?math=\LaTeX) editors should bring up the reference selection window.
* First, open '~/.config/karabiner/karabiner.json'        
* Then, in `"complex_modifications"` add a new config
    <details>
    <summary>
    <a class="btnfire small stroke"><em class="fas fa-chevron-circle-down"></em>&nbsp;&nbsp; Click Here to Expand</a>          
    </summary>

    ```
    {
      "manipulators": [
        {
          "description": "replace unused key (print screen) with common LaTeX operators (cite)",
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
</details>

* Note: I use a German keyboard on a Mac, the keycode can be different for yours. 

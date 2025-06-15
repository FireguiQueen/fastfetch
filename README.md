# fastfetch
My own config for fastfetch

## Automatically run Fastfetch on terminal startup 
1. Open your .bashrc file (this runs every time a new terminal session starts):  `nano ~/.bashrc`
2. Scroll to the bottom and add this line: `fastfetch`
3. Save it: `ctrl + o` > `enter` > `ctrl + x` 

## 🛠 `config.jsonc` 
You can customize Fastfetch’s output by editing its config file: 
- Path: `~/.config/fastfetch/config.jsonc`  (if it doesn't exist, you can create it)
- paste the following: 
```json
  {
    "$schema": "https://github.com/fastfetch-cli/fastfetch/raw/dev/doc/json_schema.json",    
  
  "logo": 
    {
        "type": "auto",      
        "source": "~/.config/fastfetch/asciis/rem-smile-inverted.txt",      
        "padding": 
        {
            "top": 1,        
            "left": 2,      
            "right": 3       
        },
        "color": 
        {           
            "1": "white",
        }
  },
  "display": 
    { 
        "separator": " ",
        "brightColor": true,
    },
    "modules": [
       {
             "type": "custom",
             "keyColor": "white",
             "key": "╭──────────────────────────────────────────╮"
        },
        {
             "type": "custom",
             "key": "  "
        },
     
        {
            "type": "os",
            "key": " 🐧 OS",
            "keyColor": "red",
            "format": "{pretty-name} {version-id}"
        },
        { 
            "type": "kernel",
            "keyColor": "red",
            "key": " ⚛️  Kernel"
        },
        {
            "type": "terminal",
            "key": " >_ Terminal",
            "format": "{pretty-name} {version}"
        },
        {
            "type": "packages",
            "key": " 📦 Packages",
            "format": "{all}"
        },
         {
            "type": "display",
            "keyColor": "blue",
            "key": " 💻 Display"
        },
        {
            "type": "wm",
            "keyColor": "blue",
            "key": " 💻 Window Manager"
        },
        {
            "type": "de",
            "keyColor": "blue",
            "key": " 💻 Desktop Environment"
        },
        {
            "type": "cpu",
            "key": " ⚙️  CPU",
            "keyColor": "yellow",
            "format": "{cores-logical} x {name}"
        },
        {
            "type": "cpu",
            "key": "    └─ 🌡️ temp.",
            "temp": true,
            "keyColor": "yellow",
            "format": "{temperature}",
             "percent": {
        "green": 9,
        "yellow": 10,
            }
        },
        {
            "type": "gpu",
            "keyColor": "yellow",
            "key": " 🎮 GPU",
        },
        {
            "type": "memory",
            "keyColor": "yellow",
            "key": " 📊 RAM"
        },
        {
            "type": "disk",
            "keyColor": "yellow",
            "key": " 💽 Disk",
            "folders": "/"
        },
        {
             "type": "custom",
             "key": "  "
        },
        {
             "type": "custom",
             "key": "╰──────────────────────────────────────────╯"
        }
    ]
}
```

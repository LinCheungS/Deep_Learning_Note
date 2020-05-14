# 快捷键
1. ctrl + =  增大字体
2. ctrl + shift + p  打开控制面版
  - 输入“Install”，然后选择“Package Control: Install Package”
3. home 句首  end句尾 （mac: control + e）
4. Ctrl+L 选中当前行
5. Left Mouse Button + Option

# 常用库
### - emmet  
[资料](https://www.cnblogs.com/jesse131/p/4978966.html)
```
div>ul>li*3>a[href=#]{选单$}
```

### - SideBarEnhancements

```
[
    { "keys": ["ctrl+shift+c"], "command": "copy_path" },
    //chrome
    { "keys": ["f1"], "command": "side_bar_files_open_with",
            "args": {
                "paths": [],
                "application": "C:\\Program Files (x86)\\Google\\Chrome\\Application\\chrome.exe",
                "extensions":".*"
            }
     },
    //firefox
    { "keys": ["f2"], "command": "side_bar_files_open_with",
             "args": {
                "paths": [],
                "application": "E:\\软件\\Firefox\\firefox.exe",
                "extensions":".*" //匹配任何文件类型
            }
    },
}

[
  // 习惯command+b默认Chrome
  { "keys": ["command+b"], "command": "side_bar_files_open_with",
    "args": {
      "paths": [],
      "application": "/Applications/Google Chrome.app",
      "extensions":".*"
    }
  },

  // Safari
  { "keys": ["command+2"], "command": "side_bar_files_open_with",
    "args": {
      "paths": [],
      "application": "/Applications/Safari.app",
      "extensions":".*"
    }
  },

  // Firefox
  { "keys": ["command+3"], "command": "side_bar_files_open_with",
    "args": {
      "paths": [],
      "application": "/Applications/Firefox.app",
      "extensions":".*"
    }
  }
]
```
### - autofilename
### - Goto-CSS-Declaration  [资料](https://packagecontrol.io/packages/Goto-CSS-Declaration)
### - HTML-CSS-JS Prettify [资料](https://packagecontrol.io/packages/HTML-CSS-JS%20Prettify)
### - BracketHighlighter
### - SublimeCodeIntel [资料](https://packagecontrol.io/packages/SublimeCodeIntel)
### - DocBlockr [资料](https://packagecontrol.io/packages/DocBlockr)

# 跳转
- 名字 : 行数    --**跳转到固定某一行**
- @  &nbsp;&nbsp;&nbsp;-- **symbol 搜索**



# 常用方法
- link:css
- 改自动保存  preference setting ``` save_on_focus_lost": true  ```

# markdown
MarkdownLivePreview  
  
MarkdownLivePreview默认关闭实时预览，既然安装这个插件了，那肯定是要用的。打开方式为在Preferences -> Package Settings -> MarkdownLivePreview -> Settings 的设置的右侧加一条 "markdown_live_preview_on_open": true,，重启sublime即可。  
[markdown设置](https://blog.csdn.net/qq_20011607/article/details/81370236)

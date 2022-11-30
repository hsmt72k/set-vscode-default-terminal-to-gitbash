# VSCode のデフォルトターミナルを Git Bash に設定する

## 設定ファイル(setting.json)の編集

### 1. setting.json を開く

Ctrl + SHift + PまたはF1でコマンドパレットを開き、"setting"と入力し「Preferences: Open User Settings (JSON)」を選択。

### 2. setting.json に2つのプロパティを追加する

`terminal.integrated.profiles.windows` で Git Bash のプロファイルを追加する。

`terminal.integrated.defaultProfile.windows` でデフォルトプロファイルを GitBash に指定する。

`settings.json`
``` json
{
  "terminal.integrated.profiles.windows": {
    "GitBash": {
      "path": [
        "C:\\Program Files\\Git\\bin\\bash.exe"
      ],
      "args":["-l"],
      "icon": "terminal-bash"
    }
  },
  "terminal.integrated.defaultProfile.windows": "GitBash"
}
```

### 確認
`Ctrl` + `Shift` + ``` キーで新規ターミナルを起動し、Git Bash が起動すれば OK。

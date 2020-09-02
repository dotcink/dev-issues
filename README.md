# Android

### App Links 国内不可用

使用 Quora 进行测试（卸载，重装）：
- 不开代理，App Links 验证失败
- 开了代理，App Links 验证成功

同时，根据 Surge 抓包结果，有 digitalassetlinks.googleapis.com 的请求，而并没有所设置的 host 请求。
可推测，验证是通过 digitalassetlinks.googleapis.com 间接进行。

**备注**

检查 App Links 是否验证成功：
- logcat: `I/IntentFilterIntentOp: Verification 28 complete. Success:true. Failed hosts:.`
- `adb shell dumpsys package domain-preferred-apps` 显示 `Status:  always : ...`

# iOS

### "Authenticating with the App Store" when uploading to App Store

```
mv ~/Library/Caches/com.apple.amp.itmstransporter{,_bak}
# may take a LONG time
/Applications/Xcode.app/Contents/SharedFrameworks/ContentDeliveryServices.framework/Versions/A/itms/bin/iTMSTransporter
# Restart Xcode
```

# Python

## pyecharts

### Setup

1. `pip install pyecharts`
2. `pip install snapshot_selenium` to export images
  1. Download [chromedriver](https://sites.google.com/a/chromium.org/chromedriver/home) and install to PATH
3. `python3`

# After mac OS upgrading to High Sierra, CocoaPods stopped working

## エラー内容 

OSをHigh Sierraにアップグレードしたら
xcode iOSプロジェクトのライブラリ importがエラーになっていたので
pod install しなおそうとしたら出来なかった。

```bash
$ pod install
-bash: /usr/local/bin/pod: /System/Library/Frameworks/Ruby.framework/Versions/2.0/usr/bin/ruby: bad interpreter: No such file or directory
```

## 原因

同梱されているruby のバージョンが上がった。

## 対応

cocoapod のgem installし直し

```bash
$ sudo gem install -n /usr/local/bin cocoapods

```


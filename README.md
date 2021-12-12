# flutter_template

Flutterプロジェクト用のテンプレートリポジトリ

## このテンプレートの機能 (予定)

### Dart-defineで開発環境を分ける

- [ ] アプリのID (bundleId, applicationId)
- [ ] ホームで表示される名前
- [ ] アプリのアイコン
- [ ] 署名の設定 (Provisioning Profile, Keystore)

### Linter

- [x] [pedantic_mono](https://pub.dev/packages/pedantic_mono)  

### 多言語化

- [x] [Internationalizing Flutter apps](https://docs.flutter.dev/development/accessibility-and-localization/internationalization)

### サポートするOSバージョン  

- [ ] iOS_
- [ ] Android_


### その他

#### iOS

- [ ] 輸出コンプライアンス情報

#### Android

---

## 使い方

### ⌘ + shift * R で 「flutter_template」 を新規プロジェクト名に置換する  

- README.mdの見出し
- pubspec.yaml の name

- android/app/build.gradle の applicationId
- 以下のAndroidManifest.xml の package名
  * android/app/src/debug/
  * android/app/src/main/
  * android/app/src/profile
- android/app/src/main/AndroidManifest.xml の android:label

- MainActivity の import文

- ios/Runner/info.plist の CFBundleName

### 上記で書き換えられない部分を手で書き換える

- ios/Runner/info.plistのCFBundleDisplayName
- Xcodeを起動してBundle Identifier を書き換える

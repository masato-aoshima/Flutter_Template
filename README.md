# flutter_template

Flutterプロジェクト用のテンプレートリポジトリ

## このテンプレートの機能

### Flutterのバージョン管理

- [x] asdf (flutter 2.8.0-stable)

### Dart-defineで開発環境を分ける

TODO: 表を書く

- [x] アプリのID (bundleId, applicationId)
- [x] アプリのアイコン

### Firebase

１つのプロジェクトで複数のアプリ(Flavor)を管理する
(Flavorごとにプロジェクトを分けない)

- [x] Firebase Analytics
- [x] Firebase Crashlytics

### Linter

- [x] [pedantic_mono](https://pub.dev/packages/pedantic_mono)  

### 多言語化

- [x] [Internationalizing Flutter apps](https://docs.flutter.dev/development/accessibility-and-localization/internationalization)

### サポートするOSバージョン  

- [ ] iOS_
- [x] Android_5.0 (minSdkVersion = 21)

---

## 使い方

### ⌘ + shift + R で 「flutter_template」 を新規プロジェクト名に置換する  

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


### Firebaseの設定

#### Android

- android/app/ の配下にgoogle-services.jsonを配置する

#### iOS

- ios/Runner/Runner/ の配下にGoogleService-Infoを配置する (FinderではなくXcode上で配置すること)
- TARGETS -> Build Phase -> Firebase Crashlyticsのスクリプトの\<googleAppId\>を、  
GoogleService-InfoのGOOGLE_APP_IDに書き換える // TODO : Flavor対応

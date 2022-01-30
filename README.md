# Flutter_Template

Flutterプロジェクト用のテンプレートリポジトリ

## このテンプレートの機能

### Flutterのバージョン管理

- [x] asdf (flutter 2.8.0-stable)

### Dart-defineで開発環境を分ける

|  環境  |  ビルドタイプ  | コマンド |
| ---- | ---- | ---- |
|  dev  |  debug  | flutter run --dart-define=FLAVOR=dev |
|  stg  |  release  | flutter run --release --dart-define=FLAVOR=stg |
|  product  |  release  | flutter run --release --dart-define=FLAVOR=product |

- [x] アプリのID (bundleId, applicationId)
- [x] アプリのアイコン
- [x] Firebase 

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

- [x] iOS_10.0 (MinimumOSVersion = 10.0)
- [x] Android_5.0 (minSdkVersion = 21)

---

## 使い方

### asdfバージョン、依存ライブラリバージョンの最新化

このテンプレートを引き継ぐ前に、テンプレート自体の更新が必要か確認する

### ⌘ + shift + R で 「flutter_template」 を新規プロジェクト名に置換する  

- README.mdの見出し
- pubspec.yaml の name
- android/app/build.gradle の applicationId
- 以下のAndroidManifest.xml の package名
  * android/app/src/debug/
  * android/app/src/main/
  * android/app/src/profile
- android/app/src/main/AndroidManifest.xml の android:label
- MainActivity の package
- ios/Runner/info.plist の CFBundleName

### 上記で書き換えられない部分を手で書き換える

- android/app/src/main/res/values-en,values-ja
- CFBundleDisplayName (Xcodeで検索)
- Xcode > Runner > TARGETS Runner > Build Settings の Product Bundle Identifier


### Firebaseの設定

#### Android

- android/app/ の配下にgoogle-services.jsonを配置する

#### iOS

- ios/firebaseディレクトリを作成する。  
その配下に更に/dev /stg /product ディレクトリを作成してGoogleService-Infoをそれぞれ配置する
- ios/Runner/ の配下にどれでもいいのでGoogleService-Infoを配置する (FinderではなくXcode上で配置すること)

# SonarQube

## SonarCube のアカウント設定

https://sonarcloud.io/sessions/new にアクセスして GitHub アカウントでログインします。

## プロジェクトの作成

https://sonarcloud.io/projects/create にアクセスしてプロジェクトを作成します。

Organization 名をメモしておきます。
Project 名をメモしておきます。
Access Token をメモしておきます。** この情報はパスワードと同じ意味を持つので漏れないように注意します。**

## Appveyor の設定

Appveyor のプロジェクトで Settings の Environment にアクセスして `Add variable` を押して環境変数を追加します。

|変数名|意味|注意|
|--|--|--|
|SONAR_QUBE_ORG|Sonar Qube のOrganization 識別子||
|SONAR_QUBE_PROJECT|Sonar Qube のプロジェクト識別子||
|SONAR_QUBE_TOKEN|Sonar Qube のアクセスキー (API キー)|追加するとき右の鍵マークを押して秘密の環境変数に設定します|

## SonarQube に関する情報

### SonarQube の使用方法に関するサイト

- https://www.appveyor.com/blog/2016/12/23/sonarqube/
- https://docs.sonarqube.org/7.4/analysis/analysis-parameters/

### chocolatey のインストール方法 (SonarQube 関連のファイルのインストールに使用)

https://chocolatey.org/install#install-with-cmdexe

### Secure the GitHub Authentication token

SonarQube で使用するアクセストークンを暗号化するために使用する

https://www.appveyor.com/docs/build-configuration/#secure-variables

### SonarScanner の使用方法

https://docs.sonarqube.org/display/SCAN/Analyzing+with+SonarQube+Scanner+for+MSBuild#AnalyzingwithSonarQubeScannerforMSBuild-Usage

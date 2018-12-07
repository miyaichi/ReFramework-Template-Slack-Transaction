# ReFramework Template Slack Transaction

Slackチャンネルに登録しているユーザーをトランザクションとして処理するワークフローテンプレート

## 内容

Slackチャンネルに登録されているユーザーに対して自動処理の結果を送るロボットを作成するためのテンプレートです。


## 設定

Data¥Condig.xlsxで以下の設定ができます。

Settingタブ

| Name                     | Default                  | Description                              |
|:-------------------------|:-------------------------|:-----------------------------------------|
| logF_BusinessProcessName | Framework Slack Template | ワークフローの名称（ログに出力されます） |
| Slack_Token              | -                        | Slack API Token                          |
| Slack_Channel            | -                        | Slack Channel ID                         |

Constantsタブ

| Name           | Default | Description  |
|:---------------|:--------|:-------------|
| MaxRetryNumber | 3       | リトライ回数 |

## 利用方法

1. テンプレート一式をダウンロードします。

2. project.jsonの"name","description"を修正します。

3. Data¥Config.xmlxにSlack API Token、Slack Channel IDを設定します。

4. Process.xamlを実装します。

  Process.xamlには、対象ユーザーの情報取得（user.info）とそのユーザーへのテストメッセージ送信（chat.postMessage）が実装されています。また、Slackサブフォルダには、ファイルをアップロードするメソッド（file.upload）が用意されていますので、ユーザーにファイルを送信することもできます。

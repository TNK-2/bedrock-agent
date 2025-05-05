# わが家のAI技術顧問 - Bedrock Agentアプリケーション

AWSのBedrock Agentを活用したチャットアプリケーションです。質問に対して、エージェントがナレッジベースを検索したり、サブエージェントを呼び出したりして回答します。

ref : https://aws.amazon.com/jp/builders-flash/202503/create-ai-advisor-with-bedrock/

## 機能

- 自然言語で質問ができるチャットインターフェース
- エージェントの思考プロセスを可視化する詳細トレース表示
- ナレッジベース検索、サブエージェント連携、Lambda実行などの高度な機能

## 必要条件

- Python 3.8以上
- AWS アカウントとBedrock Agent設定
- 必要な環境変数設定

## インストール方法

1. リポジトリをクローン:
```
git clone [リポジトリURL]
cd bedrock-agent
```

2. 依存パッケージのインストール:
```
pip install -r requirements.txt
```

3. `.env`ファイルを作成し、必要な環境変数を設定:
```
AWS_REGION=us-east-1
AGENT_ID=your-agent-id
AGENT_ALIAS_ID=your-agent-alias-id
```

## 実行方法

アプリケーションを起動するには:

```
streamlit run frontend.py
```

ブラウザで`http://localhost:8501`にアクセスしてアプリケーションを使用できます。

## トラブルシューティング

- **ナレッジベースエラー**: Aurora DBがスリープしている場合は、数秒待ってからリロードしてください。
- **スロットリングエラー**: Bedrockのモデル負荷が高い場合は、少し時間をおいて再試行するか、サービスクォータの引き上げを検討してください。 

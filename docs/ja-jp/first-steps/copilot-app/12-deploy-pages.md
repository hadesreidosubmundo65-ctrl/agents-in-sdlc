---
title: "レッスン 12 - GitHub Pages でサイトをデプロイする"
description: "GitHub Copilot app で Pages ワークフローを構成し、その pull request をレビューして、Space Quiz の公開を確認します。"
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

GitHub Pages にデプロイして、Space Quiz を公開しましょう。Copilot はワークフローを準備し、デプロイを案内できますが、変更をレビューし、サイトが公開されたことを確認するのはユーザーの役割です。

このレッスンでは、次の内容を学習します。

- Copilot に GitHub Pages のデプロイ構成を依頼する。
- マージする前にワークフローと pull request をレビューする。
- デプロイを確認し、公開されたサイトを検証する。

## シナリオ

Space Quiz はすでに GitHub リポジトリにありますが、誰でも簡単に試せる方法が必要です。単一ファイルのサイトを GitHub Pages で公開すると、サーバーやランタイム依存関係を追加せずに公開 URL から利用できます。

## Copilot にサイトのデプロイを依頼する

`space-quiz` の Copilot app セッションで、次の prompt を送信します。

```plaintext
このリポジトリで GitHub Pages を有効にしてください。必要に応じて Web サイトをビルドし、GitHub Pages にデプロイする GitHub Actions ワークフローを作成してください。README がまだない場合は、アプリの説明とローカルでの実行方法を記載した README を追加してください。これらの変更を含む pull request を作成し、必須チェックに合格したらマージしてください。デプロイが成功するまで監視し、その後、公開された Web サイトの最終 URL を報告してください。Pages の有効化やマージの権限がない場合は、何を承認する必要があるか、または何をすればよいかを正確に説明してください。サイトが公開されるまでは成功したと報告しないでください。
```

![3 段階の図。マージ済みの space-quiz pull request、Build website・Upload artifact・Deploy to Pages の各ステップが成功した GitHub Actions の Deploy website 実行、yourname.github.io/space-quiz/ で公開された Space Quiz。](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> この prompt は、エージェントに pull request の作成とマージ、およびリポジトリの Pages 設定の変更を依頼します。続行する前に、diff、デプロイ権限、GitHub の承認要求を確認してください。

## ワークフローをレビューしてデプロイを確認する

1. リポジトリに README がまだない場合に限り、README が追加されていることを確認します。
2. ワークフローのビルドとデプロイの手順を含め、pull request の変更をレビューします。
3. 必須の pull request チェックに合格した場合にのみマージします。
4. GitHub Actions のデプロイ実行が成功するまで確認します。
5. 報告された URL を開き、Space Quiz が読み込まれることを確認します。

エージェントが Pages を有効にできない、または pull request をマージできない場合は、提示された具体的な手順に従ってください。デプロイが成功し、公開サイトが読み込まれるまではタスクを完了扱いにしないでください。

## まとめと次のステップ

Space Quiz を公開サイトとして利用できるようにし、エージェントの報告だけに頼らずデプロイを確認しました。続けて[レッスン 13: 振り返りと次のステップ][next-lesson]に進みます。

[next-lesson]: ../13-review/

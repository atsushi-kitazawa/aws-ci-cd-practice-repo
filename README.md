# AWSでCI/CDする勉強リポジトリ

AWS で CI/CD を用いたシステム開発を勉強するためのリポジトリです。
コード修正からデプロイまでをパイプライン(自動化する)でつなぐようにする。

# 技術要素
- インフラ
  - AWS
    - API Geteway
    - Lambda
    - ECS(Fagete)
    - ECR
    - ALB
    - VPC
  - Terraform
- ミドルウェア
- プログラミング言語
  - Go
  - Echo
- 監視
  - OpenTelemetry？
  - エクスポート先は？
- その他
  - GitHub
  - GitHub Actions
  - ★アーティファクト管理

## メモ
* AWS でマイクロサービスを作る際は Lambda or ECS らしい
  * 参考： [マイクロサービス](https://docs.aws.amazon.com/ja_jp/whitepapers/latest/microservices-on-aws/microservices.html)

# AWSの構成
![](https://user-images.githubusercontent.com/47269784/194591609-c2f2c962-2642-4399-85a1-bdc58a53d03f.png)
![](https://user-images.githubusercontent.com/47269784/194591626-d0e911cb-67ec-49f2-a7b9-dea4cc25d1c1.png)

# アプリケーション
* 2サービス以上は用意する
* 内容自体は意味の無いものにしたい

# 流れ
1. GitHubにプッシュする
2. GitHub Actions を介してビルドが実行される
3. GitHub Actions を介してユニットテストが実行される
4. GitHub Actions を介してアーティファクトが作成される
5. アーティファクトが管理される
6. AWS にデプロイされる

## Directory structure
.
├── app                                   - バックエンドのアプリケーションコード
│   ├── Dockerfile
│   ├── go.mod
│   ├── go.sum
│   ├── gqlgen.yml                        - gqlgenの設定ファイル
│   ├── graph                             - GraphQL関連のコード
│   │   ├── generated.go                  - gqlgenによって自動生成されるGoのコード
│   │   ├── model                         - GraphQLモデルを定義するGoのコード
│   │   │   ├── models_gen.go             - gqlgenによって自動生成されるモデルのコード
│   │   │   └── todo.go
│   │   ├── resolver.go                   - GraphQLリゾルバのインターフェースを定義する
│   │   └── schema.resolvers.go           - リゾルバインターフェースを具体的に実装するコード
│   ├── infrastructure
│   │   └── todo.go                       - インフラのTodoモデル
│   ├── server.go                         - サーバーコードのエントリーポイント
│   ├── sql
│   │   └── init.sql                      - 初期化SQLスクリプト
│   └── tools.go                          - gqlgenをインストール用のファイル
│
├── front                                 - フロントエンドのアプリケーションコード
│   ├── Dockerfile
│   ├── codegen.yml                       - codegen(フロントのGraphQLコード生成)の設定ファイル
│   ├── graphql                           - GraphQLのクエリやスキーマを定義
│   │   ├── mutation                      - データを変更するGraphQLのmutation定義
│   │   │   ├── createTodo.graphql
│   │   │   ├── deleteTodo.graphql
│   │   │   └── updateTodoStatus.graphql
│   │   └── query                         - データを取得するGraphQLのquery定義
│   │       └── getAllTodos.graphql
│   ├── node_modules
│   ├── package-lock.json
│   ├── package.json
│   ├── public
│   ├── src                               - アプリケーションのソースコード
│   │   ├── App.tsx                       - メインのアプリケーションコンポーネント
│   │   ├── components                    - 再利用可能なUIコンポーネント
│   │   │   ├── CreateTodoForm.tsx
│   │   │   └── TodoList.tsx
│   │   ├── index.tsx                     - アプリケーションのエントリーポイント
│   │   └── types                         - TypeScriptの型定義
│   │       └── gen                       - codegenによって自動生成される型定義
│   │  ├── api.ts                         - APIの型定義
│   │  └── possibleTypes-result.ts
│   └── tsconfig.json
│
├── docker-compose.yml
└── schema.graphqls                       - 共通のGraphQLスキーマを定義


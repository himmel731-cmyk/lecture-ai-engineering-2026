# 第6回 解答

## 演習

<!-- [tool call] の行は、表示された行をそのまま貼り付けてください。終わらなかった STEP は、空欄のままでかまいません。 -->

- STEP 1 のツールの名前：glossary_search_glossary
- STEP 2 の [tool call]：glossary_search_glossary({'query': '3レベル'})
- STEP 3 の [tool call]：fetch_fetch({'url': 'https://modelcontextprotocol.io/'})
- STEP 4 の [tool call]：aws_aws___search_documentation({'search_phrase': 'Amazon S3 versioning overview', 'topics': ['general']})
- 気づき・疑問：サーバーごとにツール名へ接頭辞が付き、stdio・uvx・URL接続のどの方法でも同じ形式で使える。外部サーバーに渡す情報と、提供元・アクセス範囲の確認が大切。

## 宿題

<!-- 基礎・実装・発展のどれか1つに取り組めば完了です。 -->

- 取り組んだレベル：基礎
- やったこと：`app/mcp_server.py` に `tools.get_lecture_summary` の登録を追加した。
- 結果：ツール一覧に `glossary_get_lecture_summary` が表示され、「第6回では何を学びますか？」の質問で呼び出されることを確認した。
- 気づき・疑問：既存の関数をMCPサーバーに登録するだけで、クライアントから使えるツールとして公開できる。

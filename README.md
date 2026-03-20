# FWBG — Fantasy World Building Generator

ファンタジー世界設定を対話形式で構築するための GitHub Copilot エージェントスキル集です。

## 概要

Patricia C. Wrede 著「[Fantasy Worldbuilding Questions](./FWBGQ/fantasy-worldbuilding-questions.doc.md)」をベースに、  
Copilot エージェントとの会話を通じてファンタジー世界設定ファイル（`world-settings.yaml`）を生成します。

## 使い方

VS Code の GitHub Copilot Chat で以下のように入力するとスキルが起動します。

```
/fantasy-worldbuilding
```

または、自然言語で話しかけるだけでも自動的にスキルが呼び出されます。

```
ファンタジー世界を作りたい
```

引数でテーマを指定することもできます。

```
/fantasy-worldbuilding 蒸気魔法と貴族の権力闘争が中心の世界
```

## エージェントの動作フロー

| フェーズ | 内容 |
|---------|------|
| **Phase 1** | 世界の骨格に関する5つの核心的な質問（世界タイプ・魔法・種族・技術水準・舞台） |
| **Phase 2** | 地理・魔法・歴史・社会・政治・経済の6カテゴリを順番にインタビュー |
| **Phase 3** | 整合性チェックと矛盾の解消 |
| **Phase 4** | `world-settings.yaml` をワークスペースルートに生成 |

## ファイル構成

```
FWBG/
├── README.md
├── world-settings.yaml          ← 生成される世界設定ファイル（初回実行後に作成）
├── FWBGQ/
│   └── fantasy-worldbuilding-questions.doc.md   ← 原典の質問リスト（Patricia C. Wrede）
└── .github/
    └── skills/
        └── fantasy-worldbuilding/
            ├── SKILL.md                         ← スキル定義
            └── references/
                ├── questions.md                 ← 整理済み質問リスト
                └── world-template.md            ← world-settings.yaml テンプレート
```

## 参考資料

- 原典: [Fantasy Worldbuilding Questions by Patricia C. Wrede](http://www.sfwa.org/2009/08/fantasy-worldbuilding-questions/) (© 1996)
- 和訳: 神楽坂らせん

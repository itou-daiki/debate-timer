# ディベートタイマー

## 概要

**ディベートタイマー**は、ディベートや討論の際に各ステージの時間を管理し、効率的な進行をサポートするウェブアプリケーションです。ユーザーは各ステージのタイマーを開始・停止・リセットし、ステージの遷移をスムーズに行うことができます。また、タイマーが終了した際やユーザーが手動で音を鳴らした際に「ring.mp3」の音声が2回再生され、視覚と聴覚でタイマーの終了を通知します。

## 特徴

- **複数ステージ対応**: 各ステージごとに設定された時間でタイマーを管理。
- **音声通知**: タイマーが0になった時およびユーザーが「鳴らす」ボタンを押した時に音声を2回再生。
- **ステージの自動遷移**: タイマーが0になると自動的に次のステージへ遷移。
- **直感的な操作**: 開始、停止、リセット、前へ、次へ、音声再生の各ボタンで簡単に操作可能。
- **レスポンシブデザイン**: PCやスマートフォンなど、様々なデバイスで快適に利用可能。

## ステージと時間

ディベートタイマーは以下のステージと時間配分で設計されています。各ステージの詳細な説明も併記しています。

| セクション       | ステージ名               | 時間    | 説明                                                                                                                                                                 |
|------------------|--------------------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **立論**         | 肯定側立論               | 2分     | 肯定側が、論題についてのメリットを根拠となる情報とともに示します。（今後の議論は立論で出たもののみとする）                                                     |
| **立論**         | 否定側立論               | 2分     | 否定側が、論題についてのデメリットを根拠となる情報とともに示します。（今後の議論は立論で出たもののみとする）                                                   |
| **質疑**         | 作戦タイム               | 2分30秒 | 相手チームにどのような質問をぶつけるかをまとめます。                                                                                                                   |
| **質疑**         | 否定側質疑               | 2分     | 相手の立論について、不明な点や疑問点を質問します。                                                                                                                    |
| **質疑**         | 肯定側質疑               | 2分     | 相手の立論について、不明な点や疑問点を質問します。                                                                                                                    |
| **第一反駁**     | 作戦タイム               | 2分30秒 | 第一反駁で相手の立論のどの部分へ反論するかを決めます。                                                                                                                |
| **第一反駁**     | 否定側第一反駁           | 2分     | 質疑の内容を生かしつつ、相手のメリットに反論します。                                                                                                                  |
| **第一反駁**     | 肯定側第一反駁           | 2分     | 質疑の内容を生かしつつ、相手のデメリットに反論します。                                                                                                                |
| **第二反駁**     | 作戦タイム               | 2分30秒 | 第二反駁で、どのようなアピールをするかを話し合います。                                                                                                                |
| **第二反駁**     | 否定側第二反駁           | 2分     | 第一反駁への反論をし、改めてメリット・デメリットを比較した上で、審判へ自分たちの勝ちをアピールします。（第一反駁で言っていないことは、第二反駁で言ってはいけません） |
| **第二反駁**     | 肯定側第二反駁           | 2分     | 第一反駁への反論をし、改めてメリット・デメリットを比較した上で、審判へ自分たちの勝ちをアピールします。（第一反駁で言っていないことは、第二反駁で言ってはいけません） |
| **判定**         | 判定                     | 1分     | 審判が勝敗を判定します。                                                                                                                                               |

## 使用方法

### 1. セットアップ

1. **ファイルのダウンロード**:
    - リポジトリをクローンするか、ZIPファイルとしてダウンロードしてください。
    ```bash
    git clone https://github.com/yourusername/debate-timer.git
    ```
    - または、ZIPファイルをダウンロードして解凍します。

2. **音声ファイルの配置**:
    - プロジェクトフォルダ内に `ring.mp3` を配置してください。
    - `ring.mp3` が存在しない場合、音声が再生されません。

3. **ブラウザで開く**:
    - ダウンロードしたフォルダ内の `index.html` をダブルクリックするか、ブラウザで開いてください。
    - もしくは、ローカルサーバーを使用してホストすることも可能です。

### 2. アプリケーションの操作

1. **ステージの確認**:
    - 画面上部に現在のセクションとステージ名、説明が表示されます。

2. **タイマーの操作**:
    - **開始**: タイマーを開始します。タイマーが動作中は「開始」ボタンが無効化され、「停止」ボタンが有効化されます。
    - **停止**: タイマーを一時停止します。
    - **リセット**: 現在のステージのタイマーをリセットします。

3. **ステージの遷移**:
    - **前へ**: 前のステージに遷移します。タイマーはリセットされます。
    - **次へ**: 次のステージに遷移します。タイマーはリセットされます。常に押せるため、ユーザーは任意のタイミングでステージを変更できます。

4. **音声の再生**:
    - **鳴らす**: 「ring.mp3」を2回再生します。タイマーが0になった時とユーザーが手動で「鳴らす」ボタンを押した時の両方で音声が再生されます。

5. **タイマー終了時**:
    - タイマーが0になると、「ring.mp3」が2回再生され、自動的に次のステージへ遷移します。その際、タイマーのスタートはユーザーが行う必要があります。

## 技術スタック

- **HTML5**: 構造
- **CSS3**: デザインとレイアウト
- **JavaScript**: 動的な機能とロジック

## 注意事項

- **ブラウザのオートプレイポリシー**:
    - 一部のブラウザでは、ユーザーの操作なしに音声が自動再生されない場合があります。音声が再生されない場合は、ページ上で一度ボタンをクリックするなどの操作を行ってください。

- **音声ファイルのパス**:
    - `ring.mp3` のパスが正しいことを確認してください。ファイルが存在しない場合、音声は再生されません。

- **デバイスの音量**:
    - 音声が聞こえない場合、デバイスの音量設定やブラウザの音量を確認してください。

## トラブルシューティング

- **音声が再生されない**:
    - `ring.mp3` が正しい場所に配置されているか確認してください。
    - ブラウザのオートプレイポリシーにより再生がブロックされている可能性があります。一度ページ上で操作を行い、再度試してください。
    - ブラウザのコンソール（開発者ツール）にエラーメッセージが表示されていないか確認してください。

- **タイマーが正しく動作しない**:
    - JavaScriptが有効になっているか確認してください。
    - ブラウザのキャッシュをクリアして再読み込みを試してください。

## ライセンス

このプロジェクトはMITライセンスの下で公開されています。詳細については、[LICENSE](LICENSE) ファイルをご覧ください。

## 作者

**Dit-Lab.(Daiki Ito)**

- [GitHub](https://github.com/itou-daiki)

## 貢献

フィードバックや改善提案は大歓迎です。プルリクエストを送信するか、Issueを開いてください。

---

**注意**: このREADMEはプロジェクトの概要を説明するためのものであり、実際のリポジトリや連絡先情報に合わせて適宜修正してください。

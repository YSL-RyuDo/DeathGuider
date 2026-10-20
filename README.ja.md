# DeathGuider

[English](README.md), [Korean](README.ko.md), [Japanese](README.ja.md)

O2CUBEの共同制作ゲーム。囚人管理、施設運営、戦闘準備をつなぐシステムを担当しました。

**O2CUBEチームプロジェクト**のポートフォリオ文書用フォークです。原本：[vliza321/DeathGuider](https://github.com/vliza321/DeathGuider)。元のリポジトリとクレジットを尊重し、**Young-Sang Lee（YSL-RyuDo）の担当範囲**を説明します。ゲーム全体の単独制作は主張しません。

原本mainが初期状態のため、このフォークのデフォルトは`0.23Ver`です。元のブランチと履歴を保持し、原本への変更・PRは送っていません。

| プロジェクト情報 | 内容 |
|---|---|
| 開発状況 | 担当記録フォーク |
| 使用技術 | C#, Unity, O2CUBE |

[開発事例を見る](https://ysl-ryudo.github.io/ja/work/deathguider/), [Portfolio](https://ysl-ryudo.github.io/ja/)

[![DeathGuider](https://i.ytimg.com/vi/dwgntWQCBTk/hqdefault.jpg)](https://www.youtube.com/watch?v=dwgntWQCBTk)

[DeathGuider demo](https://www.youtube.com/watch?v=dwgntWQCBTk)

## ゲーム全体で担当した実装

共同ゲームで管理システムと戦闘準備を中心に担当しました。フォークには原作とチームの成果を保持します。探索全体、戦闘AI、日付システム、他メンバーのシーンを自分の成果とはしません。

**プレイの流れ**

ユニット募集 → 施設・資源配分 → 訓練・回復・装備開発 → パーティー準備 → 探索開始

ソースリンクは確認した版に固定し、担当リンクは自分のマージ以外の変更を示します。共同ファイルは単独著作を意味しません。非公開ソースには閲覧権限が必要です。

### 募集とユニット保管

ランダムな囚人募集、バスUI、ユニット保管・選択を担当しました。募集ユニットを管理画面と後のパーティー準備につなぐシステムです。

[BusRandomPrisoner.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/Bus/BusRandomPrisoner.cs), [担当変更 fc21ab5](https://github.com/YSL-RyuDo/DeathGuider/commit/fc21ab5eb4e66a8c14ed5de5e9a261ffbb7242f6), [StorageUI.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/Floor/StorageUI.cs), [担当変更 ee56050](https://github.com/YSL-RyuDo/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc)

### 訓練、回復と侵食

訓練、回復、侵食の処理を実装・変更しました。施設進行はユニットの活動データを参照します。UIスロットの占有だけから進行を導く構造の変更を後述します。

[GYMSystem.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/GYM/GYMSystem.cs), [担当変更 ee56050](https://github.com/YSL-RyuDo/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc), [HealthSystem.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/Health/HealthSystem.cs), [担当変更 ee56050](https://github.com/YSL-RyuDo/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc), [ErosionSystem.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/Erosion/ErosionSystem.cs), [担当変更 ee56050](https://github.com/YSL-RyuDo/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc)

### 研究と鍛冶

管理ループの研究所・鍛冶システムを担当しました。開発選択と資源・状態処理を、戦闘前に使える装備につなぎました。

[LaboratorySystem.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/Laboratory/LaboratorySystem.cs), [担当変更 4dc54c0](https://github.com/YSL-RyuDo/DeathGuider/commit/4dc54c0e285efdc18888b07019992ddc5fcfcdf2), [SmithSystem.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/Smith/SmithSystem.cs), [担当変更 4dc54c0](https://github.com/YSL-RyuDo/DeathGuider/commit/4dc54c0e285efdc18888b07019992ddc5fcfcdf2)

### パーティーと装備の準備

戦闘ユニット・装備選択と、空パーティーの戦闘開始防止を担当しました。自分の管理部分とチームの探索・戦闘をつなぐ境界です。

[BattleReadySystem.cs (0.23Ver)](https://github.com/YSL-RyuDo/DeathGuider/blob/4f5139ff4d5fd9f23fe730b9d99023e877c8905e/Assets/Script/MainScene/Lobby%20Test/BattleReadySystem.cs), [担当変更 f8015e0](https://github.com/YSL-RyuDo/DeathGuider/commit/f8015e039aa7e33d9e8355f3d09cd90c786a04c8)

## 担当範囲：経営システム

バス・囚人管理、一覧・保管、UIとデータの連携。

日付進行と経営状態の更新。

訓練・回復・侵食、研究所・鍛冶を含む施設関連システム。

戦闘準備：利用可能な人員・装備の選択、空パーティーでの入場防止、経営データと準備UIの接続。

本人のコミットと`Assets/Script/MainScene/`コードに基づく範囲です。戦闘AI、手続き型マップ、他のメンバーのシステムは担当範囲に含めません。

## Evidence / 근거 / 根拠

[Management / 경영 / 経営](https://github.com/vliza321/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc)

[Research & smithing / 연구소, 대장장이 / 研究所・鍛冶](https://github.com/vliza321/DeathGuider/commit/10e290b07c96a9d4d504f45d6329111dc779f1d2)

[Battle preparation / 전투 준비 / 戦闘準備](https://github.com/vliza321/DeathGuider/commit/03e4576064a55a6fe22272c9d369c4f6e9c68eb6)

[Empty-party guard / 빈 파티 방지 / 空パーティー防止](https://github.com/vliza321/DeathGuider/commit/5593c51c1824aed0503cf93ef2033e0e325a2e48)

## 実装と設計

囚人の状態、施設、日付進行、戦闘準備を連携させる経営ゲームです。戦闘準備では空のパーティーによる入場を防ぐ必要があります。

バス・囚人・保管管理、訓練・回復・侵食、研究所・鍛冶、戦闘準備時の人員・装備選択を担当しました。共同プロジェクト内の変更を本人作成コミットで示しています。

## コードの動作と実装構造の理由

確認した実装が扱う制約と利点・代償を説明します。設計効果の説明はコード分析であり、比較する全代案を当時試作したという意味ではありません。担当リンクは共同制作内の変更を示し、ソースの閲覧権限は維持します。

### 施設画面とユニット状態をつなぐ方法

**実装の流れ**

私の経営システムのコミットでは、訓練完了時にユニットの活動状態を確認して対応する能力値を変更し、活動状態を初期化するよう修正しました。回復、侵食、保管の変更も含みます。別の戦闘準備作業では選択した人員と装備を戦闘開始につなぎました。

**この構造が必要な理由**

施設パネルは表示であり、活動と能力値は画面外でも残るゲームデータです。ユニット状態を読むことで現在の訓練スロット表示だけに依存せず進行規則を適用できます。活動の初期化も表示変更だけでなく、その後のUIと進行が共有する状態遷移です。

**代案と現在の実装の折合い**

施設スロット起点は局所的に追いやすい一方、規則がスロット表現に結び付きます。ユニット活動データ起点は持続するゲーム実体に従います。数値コードを型付き状態にすれば遷移を明確にできますが、既存の利用箇所と保存値の移行が必要です。

**利点・代償と検証範囲**

広いユニット集合を走査するほど所有者と適用条件の確認が重要になり、数値の活動コードは規則を読みにくくします。これはレビュー点であり、完成した汎用状態機械という意味ではありません。共有DateSystemはチームメンバーの実装で、私の担当は施設と進行の連携です。

[DeathGuider ee560502](https://github.com/YSL-RyuDo/DeathGuider/commit/ee560502e873a71a982aa4722c2f6e409fecadcc), [DeathGuider 5593c51c](https://github.com/YSL-RyuDo/DeathGuider/commit/5593c51c1824aed0503cf93ef2033e0e325a2e48)

## プロジェクトの確認

[ProjectVersion.txt](ProjectSettings/ProjectVersion.txt)のUnity版を使用してください。`0.23Ver`の経営シーンと`Assets/Script/MainScene/Lobby Test/`から確認できます。今回の文書作業は新たなビルド・プレイ検証ではありません。フォーク所有はチームのコード・素材の著作者や権利を移転するものではなく、元の履歴・クレジットを保持します。

## 関連リポジトリ

[DeathGuider](https://github.com/YSL-RyuDo/DeathGuider), 公開リポジトリ

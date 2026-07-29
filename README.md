# CHIP-8 Emulator

Pythonで実装したターミナルベースのCHIP-8エミュレータです。

画面描画には **curses**、 一部処理に**NumPy** を利用しています。

> 現在はWindows環境での動作を確認しています。  
> Linux環境でも動作するよう改修を進めています。

## デモ動画

以下の動画で動作の様子を確認できます。

https://www.youtube.com/watch?v=n6J2HrspQfED

## 現在の開発状況

本エミュレータは現在リファクタリング中です。

過去には以下のROMの動作を確認していました。

- PONG
- INVADERS
- TETRIS
- BRIX
- VBRIX

PONGおよびINVADERSについては上記デモ動画にて動作を確認できます。

しかし、現在はNumPy依存部分の見直しやLinux対応作業の影響により、一部のROMで正常に動作しない問題が発生しています。

2026年7月現在の動作確認状況は以下の通りです。

| ROM | 状態 |
|------|------|
| PONG | ✅ 動作確認 |
| BRIX | ✅ 動作確認 |
| VBRIX| ⚠️ 改修中 |
| INVADERS | ⚠️ 改修中 |
| TETRIS | ⚠️ 改修中 |

原因調査を進めており、将来的にはNumPyへの依存を廃止して標準Python+cursesのみで動作する実装へ移行する予定です。

## 依存ライブラリ

### 現在

- curses
- NumPy（将来的に削除予定）

### 将来予定

- cursesのみ

## インストール

```bash
git clone https://github.com/monochlorobenzene2605-svg/chip8emu.git
```

依存ライブラリをインストールします。

```bash
pip install numpy windows-curses
```

---

## 実行方法


```bash
python main.py <ROMファイル>
```

---

## キー配置

CHIP-8の16キーを以下のように割り当てています。

```text
CHIP-8 Keypad      Keyboard

1 2 3 C            1 2 3 4
4 5 6 D     →      Q W E R
7 8 9 E            A S D F
A 0 B F            Z X C V
```

## 対応状況

| OS | 状況 |
|------|------|
| Windows | ✅ 動作確認済み |
| Linux | ⚠️ 対応作業中 |


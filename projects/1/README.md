# Nand2Tetris Project 1: Boolean Logic

## 実装されたチップ

### 基本論理ゲート
- **Not.hdl** - NOTゲート（インバータ）
- **And.hdl** - ANDゲート
- **Or.hdl** - ORゲート
- **Xor.hdl** - XORゲート（排他的論理和）

### 16ビット論理ゲート
- **Not16.hdl** - 16ビットNOTゲート
- **And16.hdl** - 16ビットANDゲート
- **Or16.hdl** - 16ビットORゲート

### マルチウェイゲート
- **Or8Way.hdl** - 8入力ORゲート

### マルチプレクサ（Multiplexer）
- **Mux.hdl** - 基本的な2-to-1マルチプレクサ
- **Mux16.hdl** - 16ビット2-to-1マルチプレクサ
- **Mux4Way16.hdl** - 16ビット4-to-1マルチプレクサ
- **Mux8Way16.hdl** - 16ビット8-to-1マルチプレクサ

### デマルチプレクサ（Demultiplexer）
- **DMux.hdl** - 基本的な1-to-2デマルチプレクサ
- **DMux4Way.hdl** - 1-to-4デマルチプレクサ
- **DMux8Way.hdl** - 1-to-8デマルチプレクサ

## ファイル構成

各チップには以下のファイルが含まれています：

- **\*.hdl** - HDL実装ファイル
- **\*.tst** - テストスクリプト
- **\*.cmp** - 期待される出力（比較用）
- **\*.out** - 実際のテスト実行結果

## テスト方法

1. Hardware Simulatorを起動
2. 対応する`.tst`ファイルをロード
3. テストを実行
4. 出力（`.out`）が期待値（`.cmp`）と一致することを確認


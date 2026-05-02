# Color Constraint Explorer

> Japanese version continues after English version. / 日本語版は英語版の後に続きます。

---

## English

**Accessible Color Palette Design Tool**

A browser-based tool to visually explore color palettes that satisfy WCAG contrast ratio and color vision simulation constraints on the S-V map.

🔗 **[Live Demo](https://kota-may478.github.io/color-explorer-with-constraint/)**

---

### Features

- **9 constraint conditions** selectable via checkboxes
  - Contrast ratio: 4 conditions (Main/White, Main/Background, Accent/White, Main/Accent)
  - Color vision simulation: 4 conditions (Protanopia, Deuteranopia, Tritanopia, Achromatopsia)
- **Adjustable discrimination threshold** (1.0–7.0, compatible with WCAG standards)
- **Visualization of valid regions on the S-V map**
  - Main color map: shows (S,V) regions where a valid accent color solution exists
  - Accent color map: updates in real time based on the current main (S,V)
- **Drag-and-drop** point manipulation on the map
- Zero external dependencies — single HTML file

### Usage

#### Steps 1–2: Choose H (Hue)
Set the hue of the main and accent colors using the hue bar and slider.
Use the "Set Complementary" button to automatically set the accent hue to main + 180°.

#### Step 3: Choose S and V for the Main Color
Click "Calculate Main Map" to scan a 50×50 grid and visualize which (S,V) values have a valid accent solution (green = OK).

#### Step 4: Choose S and V for the Accent Color
The right-side map updates in real time based on the main (S,V) and accent H.
Placing the point in a green region satisfies all selected constraints.

### Running Locally

```bash
git clone https://github.com/kota-may478/color-explorer-with-constraint.git
cd color-explorer-with-constraint
# Just open index.html in your browser (no server required)
open index.html
```

### Publishing on GitHub Pages

1. Push this repository to GitHub
2. Go to Settings → Pages → set Source to the `main` branch, `/ (root)`
3. Save — your page will be live at `https://kota-may478.github.io/color-explorer-with-constraint/` within a few minutes

### Technical Specifications

| Item | Details |
|------|---------|
| Implementation | Single HTML file (CSS & JS inline) |
| External dependencies | Google Fonts only (works offline too) |
| Contrast calculation | WCAG 2.1 relative luminance formula |
| Color vision simulation | Brettel et al. 1997 approximation matrix |
| Grid resolution | Main 50×50, Accent 50×50 |

### License

MIT

---

## 日本語

**アクセシブルな配色設計ツール**

WCAG コントラスト比・色覚シミュレーションの制約条件を満たすカラーパレットを、S-V マップ上で視覚的に探索できるブラウザツールです。

🔗 **[ライブデモ](https://kota-may478.github.io/color-explorer-with-constraint/)**

---

### 機能

- **9つの制約条件** をチェックボックスで自由に選択
  - コントラスト比 4条件（メイン/白、メイン/背景、アクセント/白、メイン/アクセント）
  - 色覚シミュレーション 4条件（第1・第2・第3色覚、全色盲）
- **識別閾値を調整可能**（1.0〜7.0、WCAG基準に対応）
- **S-V マップ上での有効領域の可視化**
  - メインカラーマップ：制約を満たすアクセントが存在する (S,V) 領域を表示
  - アクセントカラーマップ：現在のメイン(S,V)に対してリアルタイム更新
- **ドラッグ操作**でマップ上の点を直感的に移動
- 外部依存ゼロ・単一HTMLファイル

### 使い方

#### Step 1〜2：H（色相）を決める
メインカラーとアクセントカラーの色相を、色相バーとスライダーで設定します。
「補色に設定」ボタンでアクセントHをメインの+180°に自動設定できます。

#### Step 3：メインカラーの S・V を決める
「メインマップを計算する」ボタンを押すと、50×50グリッドをスキャンして
「この(S,V)に対してアクセント側に制約を満たす解が存在するか」を可視化します（緑＝OK）。

#### Step 4：アクセントカラーの S・V を決める
右側のマップはメインの(S,V)・アクセントHに対してリアルタイム更新されます。
緑の領域内に点を置くと、選択した全制約条件をクリアします。

### ローカルで動かす

```bash
git clone https://github.com/kota-may478/color-explorer-with-constraint.git
cd color-explorer-with-constraint
# index.html をブラウザで開くだけ（サーバー不要）
open index.html
```

### GitHub Pages で公開する

1. このリポジトリを GitHub に push する
2. Settings → Pages → Source を `main` ブランチの `/ (root)` に設定
3. Save → 数分後に `https://kota-may478.github.io/color-explorer-with-constraint/` で公開される

### 技術仕様

| 項目 | 内容 |
|------|------|
| 実装 | 単一HTMLファイル（CSS・JS内包） |
| 外部依存 | Google Fonts のみ（オフラインでも動作） |
| コントラスト計算 | WCAG 2.1 相対輝度式 |
| 色覚シミュレーション | Brettel et al. 1997 近似行列 |
| グリッド解像度 | メイン 50×50、アクセント 50×50 |

### ライセンス

MIT

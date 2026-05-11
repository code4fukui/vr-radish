# vr-radish

Three.js、`@pixiv/three-vrm`、およびAR（拡張現実）向けのWebXRを使用して構築された、インタラクティブな3D大根キャラクターのデモです。

[**ライブデモ**](https://code4fukui.github.io/vr-radish/)

## デモ

このリポジトリには2つの異なるデモが含まれています。

### 1. ARで歩く大根（`index.html`）

円を描くように歩く大根のキャラクターをフィーチャーしたメインのデモです。

- **ARモード:** 対応デバイスで「START AR」ボタンを押すと、現実空間に大根を配置できます。
- **3Dビュー:** デスクトップ環境では、OrbitControlsを使用してシーンを操作できます（ドラッグで回転、スクロールでズーム）。
- **アニメーション:** 大根の手足と首をプログラムでアニメーションさせ、歩行モーションを作成しています。

### 2. マウスインタラクション（`mouse.html`）

VRMモデルのボーン（スケルトン）と直接インタラクションするシンプルなデモシーンです。

- **マウス操作:** 大根モデルの腰（`hips`ボーン）が、画面上のマウスカーソルの位置に追従します。

## ローカルでの実行方法

ご自身のPCでこれらのデモを実行するには、ローカルWebサーバーを立ち上げてファイルをホストする必要があります。

1. **リポジトリのクローン:**
    ```sh
    git clone https://github.com/code4fukui/vr-radish.git
    cd vr-radish
    ```

2. **ローカルサーバーの起動:**
    Python 3がインストールされている場合、組み込みのHTTPサーバーを使用できます:
    ```sh
    python -m http.server
    ```
    または、`npx serve`などのシンプルなサーバーツールを使用することもできます。

3. **ブラウザで開く:**
    - ARデモは `http://localhost:8000/index.html` にアクセスしてください。
    - マウス操作デモは `http://localhost:8000/mouse.html` にアクセスしてください。

## 使用技術とクレジット

- **レンダリング:** [Three.js](https://threejs.org/)
- **VRM読み込み:** [@pixiv/three-vrm](https://pixiv.github.io/three-vrm/)
    - [ドキュメント](https://pixiv.github.io/three-vrm/packages/three-vrm/docs/)
- **モデル:**
    - `Yamakoshi_radish01.vrm`
    - `VRM1_Constraint_Twist_Sample.vrm`（コード内で利用可能）

## ライセンス

このプロジェクトはMIT Licenseの下で公開されています。

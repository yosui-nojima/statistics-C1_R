# 2023年度　統計学C-Ⅰ工（地）水曜４限
2023年5月17日 15:10~16:40

## データ解析の再現性
エクセルなどの表計算ソフトにおけるメニュー操作やコピー＆ペーストを通して行ったデータの集計・加工・分析およびグラフ化（可視化）の作業は記録できず、結果の再現性が低い。\
一方、RやPythonといったプログラミング言語を用いた解析では、データの読み込みから結果の出力まで、「手作業」を極力排除してデータ解析を自動化するため、結果の再現性が高い。
## Rについて
- Rはデータ分析や統計解析のために開発されたソフトウェアで、プログラミング言語としても十分な機能を備えている。
- プログラミング言語といってもCやJavaなどの言語よりも比較的簡単。順番に処理を記述していけば一通りの分析が可能であり、プログラミング言語としうより「分析ツール」という感覚で使用している人も多い。
- 無料で入手できる統計解析に特化したプログラミング言語で、統計解析で最も広く使われている。
- 基本的な統計解析機能が標準パッケージに含まれており、初期状態で一通りの統計分析を行うことが可能。
- 様々な分野に適した拡張パッケージが提供されており、適宜インストールして使用することが可能。
- Rは、開発者のRoss Ihaka、Robert Clifford Gentlemanにより開発され、Rという名称は両者のイニシャルでもある。
- 現在は、R Development Core Teamによってメンテナンス・拡張がされている。
## Rのインストール
1. [https://www.r-project.org/](https://www.r-project.org/)をクリック。

2. 『download R』をクリック 
<img width="1281" alt="スクリーンショット 2023-05-12 17 58 31" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/98ff8d0d-6ace-480b-87f3-12390f5956ec">　　

3. 任意のミラーサイトのリンクをクリック
<img width="1282" alt="スクリーンショット 2023-05-12 17 59 28" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/fe001245-d16e-4891-8843-e189ec59ae0f">

4. 『Download R for Windows』をクリック。※これまOSはWindowsの場合です。その他のOSの場合は、適切なリンクをクリック。
<img width="1281" alt="スクリーンショット 2023-05-12 17 59 50" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/b697ec92-2e79-4f48-a596-51128e9c23a5">

5. 『install R for the first time』をクリック。
<img width="1281" alt="スクリーンショット 2023-05-12 18 00 20" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/e473ef83-c4a9-4a10-8c66-c46a80ab2e59">

6. 『Download R-4.3.0 for Windows』をクリック。
<img width="1280" alt="スクリーンショット 2023-05-12 18 00 36" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/c2d3fa70-6719-4e6a-a736-7c5fa0843c7f">

7. ダウンロードフォルダにある『R-4.3.0-win.exe』をダブルクリック。

8. 『はい』をクリック。
<img width="456" alt="スクリーンショット 2023-05-12 18 01 16" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/b9a5bbcb-b00f-4ce0-beb8-f79c34aaf2c4">

9. 『日本語』が選択されていることを確認して、『OK』をクリック
<img width="298" alt="スクリーンショット 2023-05-12 18 01 28" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/ea809e0c-60d7-4b1a-a5a3-d6435604d936">

10. 『次へ』をクリック。
<img width="499" alt="スクリーンショット 2023-05-12 18 01 36" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/f6e429a9-9de3-4174-9135-1ef590579ed3">

11. 『次へ』をクリック。
<img width="499" alt="スクリーンショット 2023-05-12 18 01 45" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/1f96df4d-f577-45e9-b3dd-1245fecfc90e">

12. ３つともチェックされていることを確認して、『次へ』をクリック。
<img width="498" alt="スクリーンショット 2023-05-12 18 02 13" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/d2cb8733-7fd0-435d-addb-9d6ddc78ba44">

13. 『いいえ』が選択されていることを確認して、『次へ』をクリック。
<img width="498" alt="スクリーンショット 2023-05-12 18 02 25" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/c242ab9c-b886-4468-babd-7194eee9bc1a">

14. 『次へ』をクリック。
<img width="498" alt="スクリーンショット 2023-05-12 18 02 35" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/9c8202e5-449f-417b-8228-66304d227395">

15. 『次へ』をクリック。
<img width="498" alt="スクリーンショット 2023-05-12 18 03 01" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/a01101c3-3c20-431b-8b88-a2118f91d33b">

16. 『完了』をクリック。
<img width="499" alt="スクリーンショット 2023-05-12 18 03 28" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/a17715e3-cb45-4241-a119-583d60efafce">

## RStudioについてインストール
Rは単独で実行することも可能ですが、統合開発環境（Integrated Development Environment; IDE）というプログラムの記述や実行、デバックなどに必要なツールが一体化されているツールを利用して使用する方が便利です。\
IDEとして、最も一般的なのが『**RStudio**』です。

## RStudioのインストール
1. [https://posit.co/download/rstudio-desktop/](https://posit.co/download/rstudio-desktop/)をクリック。
2. 『DOWNLOAD RSTUDIO DESKTOP FOR WINDOWS』をクリック。
<img width="1689" alt="スクリーンショット 2023-05-12 18 06 09" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/cbd65843-7320-4d42-9082-02a7effbe601">

3. ダウンロードフォルダにある『RStudio-2023.03.0-386.exe』をダブルクリック。

4. 『はい』をクリック。
<img width="459" alt="スクリーンショット 2023-05-12 18 06 32" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/acec8bde-146a-40a3-8e16-93021ab094d3">

5. 『次へ』をクリック。
<img width="581" alt="スクリーンショット 2023-05-12 18 06 42" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/6f51eeda-5881-4ea5-87d1-51bcbf392049">

6. 『次へ』をクリック。
<img width="581" alt="スクリーンショット 2023-05-12 18 06 50" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/e23f8828-bbeb-4623-9c78-0530ca535bd6">

7. 『インストール』をクリック。
<img width="581" alt="スクリーンショット 2023-05-12 18 07 01" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/aa33e51e-e412-47ef-ad3a-78568df05032">

8. 『完了』をクリック。
<img width="581" alt="スクリーンショット 2023-05-12 18 08 00" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/aba744d2-fca0-49a7-bb9d-500b71c79271">

## R、RStudioの起動
1. デスクトップの左下にある検索窓に「**Rstudio**」と入力。
<img width="833" alt="スクリーンショット 2023-05-12 19 26 40" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/144cd66e-19ff-4e86-8ec0-c7e09629a2eb">

2. 『タスクバーにピン留めする』をクリック。
<img width="832" alt="スクリーンショット 2023-05-12 18 09 08" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/3c28c517-5824-4305-b687-38d5473e774d">

3. 『開く』をクリック。
<img width="833" alt="スクリーンショット 2023-05-12 18 09 19" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/4920043f-4d37-4f34-9e48-8e6057679cfd">

4. 『Use your machine's default 64-bit version of R』が選択されていることを確認して、『OK』をクリック。
<img width="390" alt="スクリーンショット 2023-05-12 18 09 33" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/32f428a1-6d00-4bd1-90b9-9e98f2e01f40">

5. クラッシュレポートを提供するかどうかを聞いています。『はい』でも『いいえ』でもどちらでもかまいません。
<img width="558" alt="スクリーンショット 2023-05-12 18 10 03" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/31644000-459e-45b5-91ff-06d194ac3dde">

6. 以下の画面が表示されればインストール成功です。
<img width="1186" alt="スクリーンショット 2023-05-12 18 10 25" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/44fe9f84-12da-406c-ba39-f9a3a5e7d7de">


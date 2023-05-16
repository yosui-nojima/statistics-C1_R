# 2023年度 統計学C-Ⅰ工（地）水曜４限 2023年5月17日 15:10~16:40
# R実習

## 1. データ解析の再現性
『再現性』とは、同一の結果が同一の実験手法・解析手法によって得られるとき、それら結果の一致の度合いの高さを示す。\
自分の解析結果を研究室内や会社内の他の人が同じ解析をする場合、エクセルなどの表計算ソフトにおけるメニュー操作やコピー＆ペーストを通して行ったデータの集計・加工・分析およびグラフ化（可視化）の作業は記録できず、結果の再現性が低い。\
一方、RやPythonといったプログラミング言語を用いた解析では、スクリプトを作成することでデータの読み込みから結果の出力まで、「手作業」を極力排除してデータ解析を自動化することができ、結果の再現性が高い。
## 2. Rについて
- Rはデータ分析や統計解析のために開発されたソフトウェアで、プログラミング言語としても十分な機能を備えている。
- プログラミング言語といってもCやJavaなどの言語よりも比較的簡単。順番に処理を記述していけば一通りの分析が可能であり、プログラミング言語としうより「分析ツール」という感覚で使用している人も多い。
- 無料で入手できる統計解析に特化したプログラミング言語で、統計解析で最も広く使われている。
- 基本的な統計解析機能が標準パッケージに含まれており、初期状態で一通りの統計分析を行うことが可能。
- 様々な分野に適した拡張パッケージが提供されており、適宜インストールして使用することが可能。
- Rは開発者のRoss Ihaka、Robert Clifford Gentlemanにより開発され、Rという名称は両者のイニシャルでもある。
- 現在は、R Development Core Teamによってメンテナンス・拡張がされている。
## 3. Rのインストール
1. [https://www.r-project.org/](https://www.r-project.org/)をクリック。

2. 『download R』をクリック 
<img width="1281" alt="スクリーンショット 2023-05-12 17 58 31" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/4aac52a6-1dbc-4b02-8017-1884b22075ee">

3. 任意のミラーサイトのリンクをクリック
<img width="1282" alt="スクリーンショット 2023-05-12 17 59 28" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/6ce700c8-3208-4ecf-9b9b-d554208ca33f">

4. 『Download R for Windows』をクリック。※OSがWindowsの場合です。その他のOSの場合は、適切なリンクをクリック。
<img width="1281" alt="スクリーンショット 2023-05-12 17 59 50" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/45d7a416-d118-4976-a01d-28b364377207">

5. 『install R for the first time』をクリック。
<img width="1281" alt="スクリーンショット 2023-05-12 18 00 20" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/0664941a-2ba9-4336-88be-1f89fe75e0b6">

6. 『Download R-4.3.0 for Windows』をクリック。
<img width="1280" alt="スクリーンショット 2023-05-12 18 00 36" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/115e9834-ed4e-40cf-8235-8c2f944805ec">

7. ダウンロードフォルダにある『R-4.3.0-win.exe』をダブルクリック。

8. 『はい』をクリック。
<img width="456" alt="スクリーンショット 2023-05-12 18 01 16" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/ce94e6cd-c523-469f-893a-fe8c88dc1383">

9. 『日本語』が選択されていることを確認して、『OK』をクリック
<img width="298" alt="スクリーンショット 2023-05-12 18 01 28" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/40b2ddeb-88ea-4c6e-85a6-15142f0427d3">

10. 『次へ』をクリック。
<img width="499" alt="スクリーンショット 2023-05-12 18 01 36" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/a2bf35e3-4e8d-455e-9362-e44937d6df86">

11. 『次へ』をクリック。
<img width="499" alt="スクリーンショット 2023-05-12 18 01 45" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/fe46d9ff-eec3-4809-9c09-b2e88f1951ba">

12. ３つともチェックされていることを確認して、『次へ』をクリック。
<img width="498" alt="スクリーンショット 2023-05-12 18 02 13" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/0196f8d4-7821-4a74-82e9-29ea036092d2">

13. 『いいえ』が選択されていることを確認して、『次へ』をクリック。
<img width="498" alt="スクリーンショット 2023-05-12 18 02 25" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/22efda67-df58-44ab-8c1c-06297ece2f84">

14. 『次へ』をクリック。
<img width="498" alt="スクリーンショット 2023-05-12 18 02 35" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/321ecf1e-54fb-410e-935b-502fa433dd4f">

15. 『次へ』をクリック。
<img width="498" alt="スクリーンショット 2023-05-12 18 03 01" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/08a9de90-28c9-4666-9c71-5765772b4206">

16. 『完了』をクリック。
<img width="499" alt="スクリーンショット 2023-05-12 18 03 28" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/d3a92ecd-fcae-4dcd-83d6-ca4f6d91e400">

## 4. RStudioについて
Rは単独で実行することも可能ですが、統合開発環境（Integrated Development Environment; IDE）というプログラムの記述や実行、デバックなどに必要なツールが一体化されているツールを利用して使用する方が便利です。\
IDEとして、最も一般的なのが『**RStudio**』です。

## 5. RStudioのインストール
1. [https://posit.co/download/rstudio-desktop/](https://posit.co/download/rstudio-desktop/)をクリック。
2. 『DOWNLOAD RSTUDIO DESKTOP FOR WINDOWS』をクリック。
<img width="1689" alt="スクリーンショット 2023-05-12 18 06 09" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/1c73a85f-2e90-40d0-b688-72065f49efa7">

3. ダウンロードフォルダにある『RStudio-2023.03.0-386.exe』をダブルクリック。

4. 『はい』をクリック。
<img width="459" alt="スクリーンショット 2023-05-12 18 06 32" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/cdf85869-047e-4fd9-9b87-eb2fc029179b">

5. 『次へ』をクリック。
<img width="581" alt="スクリーンショット 2023-05-12 18 06 42" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/a3cde434-c58c-4ae4-afc8-754d7290502e">

6. 『次へ』をクリック。
<img width="581" alt="スクリーンショット 2023-05-12 18 06 50" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/b1b44146-1b25-4e86-af9b-4f1a639b6491">

7. 『インストール』をクリック。
<img width="581" alt="スクリーンショット 2023-05-12 18 07 01" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/bc1da0ca-1556-4dc7-9c8c-7f934a81cf85">

8. 『完了』をクリック。
<img width="581" alt="スクリーンショット 2023-05-12 18 08 00" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/755296ff-0098-4aff-896a-fc539b1b8ae1">

## 6. RStudioによるRの起動
1. デスクトップの左下にある検索窓に「**rstudio**」と入力。
<img width="833" alt="スクリーンショット 2023-05-12 19 26 40" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/ee077434-7271-4371-a408-b92b6aeb964f">

2. 『タスクバーにピン留めする』をクリック。
<img width="832" alt="スクリーンショット 2023-05-12 18 09 08" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/bb2fbd8b-49a8-46a0-af8b-8fa4731ef73b">

3. 『開く』をクリック。
<img width="833" alt="スクリーンショット 2023-05-12 18 09 19" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/8c237bbe-a88b-4bce-917d-be5648e3ec80">

4. 『Use your machine's default 64-bit version of R』が選択されていることを確認して、『OK』をクリック。
<img width="390" alt="スクリーンショット 2023-05-12 18 09 33" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/837e2729-a6c3-4b53-b57e-c04035d1442a">

5. クラッシュレポートを提供するかどうかを聞いている。どちらでもかまわない。
<img width="558" alt="スクリーンショット 2023-05-12 18 10 03" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/9594333a-d3a3-4783-a104-a90c4be3d925">

6. 以下の画面が表示されればインストール成功。
<img width="1186" alt="スクリーンショット 2023-05-12 18 10 25" src="https://github.com/yosui-nojima/statistics-C1_R/assets/85273234/c45549af-ddb6-42ac-93ab-083ce71c7434">

## 7. R実行の準備
『Console』に直接入力して実行してもかまわないが、スクリプトとして記録・保存できないため、\
タブから、File → New File → R Scriptを選択し、クリック。\
『Console』の上に、『Untitled1』という画面が表示される。ここに下記**８．Rの文法**のコードを入力すること。

## 8. Rの文法
一行ずつ実行すること。\
行の説明やコメントを入れる際は、『#』を使う。実行する際、『#』以降は無視される。
### 算術演算
```
3 + 2       #和
3 - 2       #差
3 * 2       #積
3 / 2       #商
3 ^ 2       #累乗

3^2         #スペースはなくてもよい
```
### オブジェクトへの格納（代入操作）
```
a <- 1      #1をAに格納
A <- 2	    #2をAに格納
b <- a + A  #a+Aをbに格納
print(b)    #bを表示
b	    #print()を書かなくても表示される
```
### ベクトル
```
a <- c(1, 2, 3)	#(1, 2, 3)をあに格納
A <- c(4:6)   	#(4, 5, 6)をAに格納
b <- a + A    	#a+Aをbに格納
b               #bを表示
b * 2           #b×2を表示
```
### 関数を使った記述統計量の計算
Rでは、『関数』と呼ばれる計算を便利にするいくつかの機能がデフォルトでインストールされている。\
例えば、ベクトル```a```の平均を算出する際、下記のようにしてもよいが、
```
(1+2+3)/2
```
ベクトルの要素の数が多くなると対応できないため、汎用性のあるコードとは言えない。\
総和を算出する関数に```sum()```があり、ベクトルの要素の数を出力する関数に```length()```がある。\
そこで、この２つの関数を組み合わせると、
```
a <- c(1,2,3)
length(a)       #ベクトルの要素の数
sum(a)          #ベクトルの要素の和
sum(a)/length(a)　#ベクトルの要素の平均値
```
とすると、```a```の要素の数が増えても、その度にコードを書き換える必要がないため上記よりは汎用性のあるコードとなった。\
Rには```mean()```という関数もあり、これを使うと関数１つで平均値を算出する。
```
a <- c(1,2,3)
mean(a)         #ベクトルの要素の平均値
```
また、標本不偏分散を算出する関数```var()```、平方根を算出する関数```sqrt()```を用いて、標本不偏分散、標本不偏標準偏差、標本分散、標本標準偏差を算出できる。
```
a <- c(1,2,3)
var(a)          #ベクトル要素の標本不偏分散
sqrt(var(a))    #ベクトル要素の標本不偏標準偏差
var(a)*((length(a)-1)/length(a))    #ベクトルの要素の標本分散
sqrt(var(a)*((length(a)-1)/length(a)))    #ベクトルの要素の標本標準偏差
```
### 論理
```
bool <- c(TRUE, FALSE, F, T)    #論理値
bool                            #TはTRUEの略、FはFALSEの略
sum(bool)                       #T/Fは1/0として扱われる

"pen" == "pen"     #比較演算（同じ）
"pen" == "apple"
"pen" != "apple"   #比較演算（異なる）
"pen" != "pen"

1 < 2              #比較演算（より小さい）
1 >= 2             #比較演算（より大きいか同じ）

is_apple <- fr1 == "apple"       #比較演算の結果を格納
is_apple

is_apple <- fruites == "apple"   #比較演算の結果を格納
is_apple
```
### 型
```
class(a)         #オブジェクトの型を表示する
class(fr1)
class(fruites)
class(is_apple)
str(a)           #型と構造、内容の一部を表示する
str(fr1)
str(fruites)
str(is_apple)
```
### ベクトルの要素を取り出す
```
Nums <- seq(4, 62, 2)   #4から62まで間隔が2の数列を作成
Nums
str(Nums)

head(Nums)     #最初の6つ
head(Nums, 8)  #最初の8つ
tail(Nums, 8)  #最後の8つ

Nums[3]      #3つめの要素
Nums[2:5]    #2つめから5つめまでの要素
Nums[-3]     #3つめ以外の要素
```
### 要素の追加
```
Nums <- append(Nums, 64)          #最後に要素を追加
Nums

Nums <- append(Nums, 2, after=0)  #先頭に追加
Nums                              #'after'で位置を指定
```
### マトリクス（行列）
```
Nums <- matrix(Nums, 8, 4)   #Numsを8×4の行列に変換
Nums
```
### row（行）とcolumn（列）の指定
```
Nums[1, 2]   #row 1, column 2
Nums[2, 1]   #row 2, column 1
Nums[, 2]    #すべてのrow, column 2
Nums[2, ]    #row 2, すべてのcolumns

class(Nums)  #型の確認
str(Nums)
```
### forループ（一定範囲内での繰り返し操作）
10行✕1列の空のマトリクスを作成し、n+1(n=1,2,3,,,10)の計算結果を1行ごとに格納していく。
```
data <- matrix(nrow = 10, ncol = 1) #空のマトリクス作成
for (x in 1:10) {
  data[x,] <- x + 1 #n+1(n=1,2,3,,,10)の計算結果を1行ごとに格納
}
data #結果の表示
```
## パッケージのインストールと読み込み
下記コードには、Rにデフォルトでインストールされている関数には含まれていない関数を必要とするため、下記で追加インストールする。
複数の関数が１つのパッケージとして公開されている。パッケージ単位でインストールする。
```
install.packages("reshape2") #ライブラリのインストール（最初のみ実行）
install.packages("ggplot2")  #ライブラリのインストール（最初のみ実行）
```
上記は一度インストールすれば次回から再度実行する必要はない。（Rをアンインストールした場合は再度インストール必要）\
インストールしただけでは使用することはできない。下記でパッケージを使用可能な状態にする。\
これはRを起動するたびに行う必要がある。
```
library(reshape2) #パッケージの読み込み
library(ggplot2) #パッケージの読み込み
```
## 標準正規分布に従う母集団からn=3, 4, 8, 32の標本をm回抽出したときの標本不偏分散と標本分散を確認する
### 母集団の生成
まず平均0、分散1の標準正規分布に従う母集団を生成する。
```
set.seed(xxx)  #乱数を指定（xxxの箇所に学籍番号の下３桁の値を入力すること。例：set.seed(123)）
num <- rnorm(n = 100000, mean = 0, sd = 1) #標準正規分布に従う乱数を生成。
hist(x = num, breaks = 100)
```
- set.seed; 乱数を指定。これを指定することで```rnorm```関数から毎回同じ乱数を生成させる。
- rnorm; 正規分布に従う乱数を生成。rnormの()内には```n =```,```mean =```,```sd =```の３つの条件を指定しており、それぞれを引数という。引数を指定しない場合は各関数がデフォルトで指定している値が自動で指定される。
  - n; 集団の大きさを指定
  - mean; 平均値を指定
  - sd; 標準偏差を指定
- hist; ヒストグラムを出力する関数
  - x; ベクトルを指定
  - breaks; 階級の数を指定

#### a. 標本不偏分散を確認する
```
data <- matrix(nrow = 1000, ncol = 4) #空の行列を生成
for (x in 1:1000) { #標本不偏分散を出力 #mの範囲（m==1,2,3,,,1000)を指定
  data[x,1] <- var(sample(x = num, size = 3*x)) #n=3のときの標本不偏分散を計算
  data[x,2] <- var(sample(x = num, size = 4*x)) #n=4のときの標本不偏分散を計算
  data[x,3] <- var(sample(x = num, size = 8*x)) #n=8のときの標本不偏分散を計算
  data[x,4] <- var(sample(x = num, size = 32x))  #n=32のときの標本不偏分散を計算
}
colnames(data) <- c("n3", "n4", "n8", "n32") #列名を定義
data.m <- melt(data) #行列をデータを加工
colnames(data.m) <- c("M", "n", "S^2") #列名を定義
ggplot(data.m, aes(x = M, y = `S^2`, color = n)) + geom_line() + ylim(0, 2) +
  theme(panel.background = element_blank(), axis.line=element_line(colour = "black"), panel.grid = element_line(colour = "gray")) +
  theme(axis.text.x = element_text(colour = "black", size = 30), axis.title.y = element_text(size = 30, colour = "black"), axis.title.x = element_text(size = 30, colour = "black"), axis.text.y = element_text(size = 30, color = "black"), legend.text = element_text(size = 30, color = "black"), legend.title = element_text(size = 30, color = "black"))
```
#### b. 標本分散を確認する
```
data <- matrix(nrow = 1000, ncol = 4) #空の行列を生成
for (x in 1:1000) { #標本不偏分散を出力 #mの範囲（m==1,2,3,,,1000)を指定
  data[x,1] <- var(sample(x = num, size = 3*x))*((3-1)/3) #n=3のときの標本分散を計算
  data[x,2] <- var(sample(x = num, size = 4*x))*((4-1)/4) #n=4のときの標本分散を計算
  data[x,3] <- var(sample(x = num, size = 8*x))*((8-1)/8) #n=8のときの標本分散を計算
  data[x,4] <- var(sample(x = num, size = 32*x))*((32-1)/32)  #n=32のときの標本分散を計算
}
colnames(data) <- c("n3", "n4", "n8", "n32") #列名を定義
data.m <- melt(data) #行列をデータを加工
colnames(data.m) <- c("M", "n", "S'^2") #列名を定義
ggplot(data.m, aes(x = M, y = `S'^2`, color = n)) + geom_line() + ylim(0, 2) +
  theme(panel.background = element_blank(), axis.line=element_line(colour = "black"), panel.grid = element_line(colour = "gray")) +
  theme(axis.text.x = element_text(colour = "black", size = 30), axis.title.y = element_text(size = 30, colour = "black"), axis.title.x = element_text(size = 30, colour = "black"), axis.text.y = element_text(size = 30, color = "black"), legend.text = element_text(size = 30, color = "black"), legend.title = element_text(size = 30, color = "black"))
```

- sample; 母集団から単純無作為抽出法により標本を抽出
  - x; ベクトルを指定
  - size; 標本の大きさを指定
- colnames; 列名を出力
- melt; データを可視化するためのデータ加工\
※ggplotによる可視化のコードは、現時点で理解する必要はありません。

## 中心極限定理を確認する
```
m <- 1 #サイコロの個数 #7以上の値を入れると処理が遅くなるため、1~6の整数を入力すること。
deme <- c(1, 2, 3, 4, 5, 6) #サイコロの出目を指定（今回は通常の6面体サイコロ）
deme.rep <- rep(deme, m) #```deme```ベクトルの要素をm回繰り返す
all <- combn(x=deme.rep, m=m) #nCrで計算される全ての組み合わせを出力
all <- t(all) #転置（```unique```関数は行方向についての重複を除去するため、```unique```を実行する前に```t()```で転置する）
all <- unique(all) #重複を除去（combn関数はベクトル内の要素は全て独立とみなすため、重複を除く）
all <- t(all) #転置（重複を除去したので、再度転置しても元に戻す）

mean <- colMeans(all) #列方向について平均値を算出（各組み合わせの平均値を算出）
mean.d <- data.frame(table(round(mean, digits = 2))) #各平均値の度数を算出
mean.d$Probability <- NA #各平均値の確率を格納するための空の列を生成。列名を```Probability```とする。
colnames(mean.d)[1] <- "Mean" #平均値の列に```Mean```という列名を指定
for (x in 1:nrow(mean.d)) { #forループ（```nrow```は行数を出力する関数。```1:nrow```で1から```mean.d```の行数までループを続ける）
  mean.d$Probability[x] <- mean.d$Freq[x] / sum(mean.d$Freq) #各度数と度数の総数から確率を算出
}
#プロット
ggplot(mean.d, aes(x = Mean, y = Probability)) +
  geom_point(size = 3) + 
  geom_col(aes(x=Mean), width = 0.01, color = "black")
```
- rep; ```x =```で指定したベクトルを指定した回数繰り返す
  - x; ベクトルを指定
- combn; #nCrで計算される全ての組み合わせを出力
- t; 転置
- unique; 行方向について重複を除去
- colMeans; 列方向について平均値を算出
- data.frame; オブジェクトの型をデータフレームにする
- table; 度数を出力
- round; 指定した桁数を四捨五入した値を返す
  - digits; 小数点第何位まで表示させるか指定。四捨五入して出力。
- colnames; 列名を出力\
※ggplotによる可視化のコードは、現時点で理解する必要はありません。

**```m <- 1```を実行した後は```m```の値を1ずつ増やして実行。\
ただし、7以上の値を入れると処理が遅くなるため、1~6の整数を入力すること。**

## 母平均の区間推定（仮想データを使った解析）
[e-Stat](https://www.e-stat.go.jp/)は、各府省が公表する統計データを一つにまとめ、統計データの検索をはじめとした、さまざまな機能を備えた政府統計のポータルサイト。\
このデータベースから、学校保健統計調査（小・中・高の生徒の身長・体重などのデータ）のうち、大阪府在住17歳男性の身長の平均・標準偏差（令和3年度集計）を[参考](https://www.e-stat.go.jp/stat-search/file-download?statInfId=000032258889&fileKind=0)に仮想データを生成する。
### 母集団の生成
```
set.seed(xxx)  #乱数を指定（xxxの箇所に学籍番号の下３桁の値を入力すること。例：set.seed(123)）
popu <- rnorm(100000, mean = 170.7, sd = 5.97) #rnorm : Normal Disribution(正規分布)を作成するコマンド。平均170.7、標準偏差5.97になるように100000人分のデータを正規分布に従うように生成。
hist(x = popu, breaks=100)
```
```
n <- 100
res <- matrix(NA, nrow = n, ncol = 1000)
for (i in 1:1000) {
  res[, i] <- sample(popu, size = n)
}
```

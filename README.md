# robosyshomework2

robosyshomework2は、ROSを使って何かをするという授業の課題提出リポジトリである。
今回は、RVizというソフトを用いて北陽のレーザーレンジファインダUTM-30LXで取得した点群をリアルタイムで表示した。
-----------------------------------------------------------
実行環境
OS:Windows10に仮想環境でVirtualBoxにUbuntu14.04を入れて動かす
ソフト:RViz
LRF:UTM-30LX
-----------------------------------------------------------
実行方法
Ubuntuを起動する。
以下をコマンドに打ち込む。
$sudo apt-get install ros-indigo-ung-node
$cd /dev
$ls -l ttyACM*
  crw-rw---- 1 root dialout 166, 0 Aug 11 14:30 ttyACM0
$sudo chmod a+rw /dev/ttyACM0
$ls -l ttyACM*
  crw-rw-rw- 1 root dialout 166, 0 Aug 11 14:35 ttyACM0
$roscore
$rosrun rviz rviz

RVizの設定の以下を変更する。
Global Optionsをlaserにする。
addを押してaxesを追加する。
addを押してlaserscanを追加する。
laserscanのトピック名を/scanにする。
ColorTransformerをFlatColorにする。
-----------------------------------------------------------
実行結果は以下リンクに載っている。
https://www.youtube.com/watch?v=PgnyfLI4eLY
-----------------------------------------------------------
参考文献
使用したRVizは、以下にある。
https://github.com/ros-visualization/rviz/tree/indigo-devel

このRVizを使ってレーザーレンジファインダを動作させる方法は以下のROSBOOKを参照した。
http://irvs.github.io/rosbook_jp/

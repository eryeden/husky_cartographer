# Husky modified

# とりあえずやること
* sick-timの追加
  * descriptionのemptyにsick-timの定義を追加
  * gazeboにおいても実行可能なのかをチェックする
  * husky.urdf.xaro
	+ urdf_extras としてempty.urdfがロードされる
  * HUSKY_URDF_EXTRASとして外部ファイルを読む設定がある。emptyはそこで読むようにパスの設定がなされている。
* GoogleSLAMの追加


# やったこと
* sick-timの追加
  1. husky_description のみをHusky repsからクローン
  2. husky_description/urdf/husky.urdf.xacroの末尾にhusky_tim551.urdf.xacroのインクルード命令を追加
  
``` bash
$ mkdir -p husky_test/src
$ cd husky_test/src
$ catkin_init_workspace
$ cp <husky_descrition> .
$ cd ..
$ catkin_make
$ source ./devel/setup.bash
```
これによって、<husky_descrition>パッケージへのパスが上書きされる。
なので、ここで行った修正は roslaunch 等で起動したhusky_baseにおいても適用される





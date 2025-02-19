
# 山手線オーバーレイ地図

web GISのオンラインマップで，任意の地域に山手線，東京都，東京科学大学（大岡山キャンパス）を重ねるwebアプリです．
知らない土地のスケール感を掴むための物です．

http://toruseo.jp/yamanote-overlay-map/

## 参考情報

### データソース

山手線駅座標
https://qiita.com/butchi_y/items/3a6b70b38e13dc56ef13

東京都外周
https://www.e-stat.go.jp/gis/statmap-search?page=1&type=2&aggregateUnitForBoundary=A&toukeiCode=00200521&toukeiYear=2015&serveyId=A002005212015&prefCode=13&coordsys=2&format=shape

東京科学大学外周
https://www.openstreetmap.org

### ChatGPT o1 pro prompt

web GISのオンラインマップで，任意の地域に山手線を重ねるwebアプリを書いてください


地図をドラックで移動しても山手線は常に画面の中心にあるようにしてください．


これのサイズを，メルカトル座標系のゆがみを考慮して現地の縮尺に合わせた形にしてください．


地域によってkm単位での大きさが違います．東京だと縦の長さが約11.4kmですが，バンコクだと13.5kmになります．メルカトルのゆがみを正しく補正できていないと思います．地域にかかわらず，正確なkmで表示するようにしてください．コードが正しいか確認してください．


良いですね．では次に以下の機能を実装してください．

図形の候補が複数あり，いずれもpolylineの座標が内部的に定義されている．
プロットする図形をチェックボックスで選択できる

//その後，手動でデータ差し替えと，Claude 3.5 Sonnetによる補助のもと微調整

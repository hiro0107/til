# DataFrame

Sparkは、DataFrameというクラスを使用する。(以前はRDDを使用していたが、現在はDataFrameが主流になっている)

# Map内での新規DataFrame

map/flatMap系の中でcreateDataFrameは使えないらしい。
使いたいユースケースはいくらでも思いつくが、そういうものだと思い、別の方法でやるしかない。

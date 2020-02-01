# 2019gsc_Atsuko-Nakanishi
2019年ゼミ論レポジトリhttps://docs.google.com/document/d/1Itanha2eji_JaF_7JxZA2gHgHyp3ay9NIcT8aZ3K5dE/edit?usp=sharin
https://docs.google.com/presentation/d/128HNG6Zvw7h2Rzmmzcc2v2vbs2l3Yp3JxxVUmJ6mbBw/edit#slide=id.g7d29f3ceef_0_99
# 概要
 本研究は、National Network for Emergency Mapping(以下、N2EM)が主体となって行っている、災害時におけるボランティアセンター情報のデータ化作業を、2019年10月に発生した台風19号の作業経験をもとにマニュアル化したものである。
近年、災害時においては、各地で被害に対応するためボランティアセンター(以下、VC)が開設さていれるが、ボランティア希望者が膨大な数存在するVCの情報を詳細に把握するのは困難である。
例えば、2019年10月に発生した台風19号では、長野、千葉、福島、宮城、岩手、栃木、埼玉、東京、茨城、群馬、神奈川、静岡などで120箇所を超えるVCが開設された。そして、VCの情報は災害状況や天候などによって常に更新され続ける。次被害を防ぐために雨天時などにボランティアが一時募集中止になることや、ボランティアが必要人数集まったためにボランティアが閉鎖される場合がある。そのような情報を個人で収集し続けることには計り知れない労力が必要だ。しかしながら、確実に被災地のニーズに確実に応えるためには、ボランティア希望者は正確な情報を迅速に網羅することが求められる。
そこで、N2EMはGoogle spread sheetを用いてボランティアセンター情報を可視化する作業を行った。ボランティアに参加するに当たり必要となる情報を効率よく把握できるデータを作成することで、ボランティア希望者とVCのニーズを確実にマッチングさせることを目標とした取り組みである。
このデータ入力作業は、前述のとおり膨大な情報量に対応する必要があるため、複数人で行わなければならない。作業協力者が多ければ多いほど、ボランティア希望者に迅速に情報を伝えることができる。そのため、作業工程を共有する資料の作成が必要と考えた。本論文では、今後災害時に多くの人がデータ入力作業に取り組めるよう、作業の一連の流れを紹介する。



# 全体構成(IMRAD形式)

## Introduction:
私は2019年10月に発生した台風19号の被害により開設されたVCの情報を可視化する作業に取り組んだ。VCが開設された後、各VCはfacebookやホームページなどによりセンターの情報を発信する。基本的に、地図や電話番号など、ボランティア希望者にとって必要な情報はそこから得ることになる。しかし、120箇所を超えるVCの情報をSNSやホームページから個人で収集することは困難である。そこで、VCの情報を地図上で把握できる状態にし、オープンデータとして公開することで、ボランティア希望者の負担を減らすことを目的とし、データ化に取り組んだ。



## Methods:
台風19号により開設された各VCの
･都道府県名
･市町村名
･センター名(ex.〇〇災害防災センター受付)
･電話番号
･e mail address
･住所
･経度(十進数)
･緯度(十進数)
･詳細URL
・VCの活動状況
以上の情報をspreadsheetに入力した。
まず、電話番号、e mail address、住所の情報は各VCが開設したSNSやHPから得た。災害ボランティア支援プロジェクト会議が特設サイトを作成し、各VCが発信した情報を県ごとにまとめているため、特設サイトに載せられているVCの情報を抽出した。
緯度、経度については、 地理院地図、OpenStreetMap 、 ひなたGIS 等を使い、二次利用可能なライセンスの地図をベースに調査した。しかし、これらのサイトのみを参考に緯度経度を割り出した場合、本来のVCの位置情報とずれが生じる場合があるため、Googleマップのジオコーディングを参考資料として使用した。
VCの活動状況については、状況をコード化して入力した。コードは以下のとおりである。
0: 災害ボランティアセンター活動終了
1: 災害ボランティアセンター活動中(原則毎日活動、天候条件により中止含む)
2: 限定活動中(市内在住者、事前予約者のみ、活動日限定など特定条件)
3: 活動中止中
4: 地元での活動終了、ただ他地域への派遣活動を継続中
9: 不明
各VCがネットワークを通して発信した活動状況をもとに、コードを入力する。
毎週木曜日に情報収集、金曜日に情報発信と、情報更新の曜日を設定した。

## Results:
一連の作業により、問題点が明らかになった。まず一つは更新される大量のVCの情報の処理が追いつかないことだ。VCは、天候やニーズにより募集状況が逐一更新され続ける。金曜日に情報を発信したとしても、発信直後にVCが情報を更新するという可能性がある。今回はN2EMのメンバー、酪農学園大学の学生、古橋研究室の学生の協力があったが、さらに多くの人手が必要になると考える。


## Discussion:
今後VCのデータ入力作業が必要になる際、現段階のマニュアルを更新し続ける必要がある。今回、多くの学生の手を借り作業に取り組んだが、その中で多くの作業ミスが発生した。顕著に目立った作業ミスは以下のとおりである。
・VCの情報ではなくは社会福祉協議会の情報を記載してしまう。(社会福祉協議会と隣接しているVCが多いために混同してしまう)
・名称に受付場所と記載し忘れる。
・閉鎖されたVCの情報を記載してしまう。
このようなミスは、新規の作業協力者が増えるほど発生率が高くなる。データ入力作業は多くの人手が必要になるため作業初心者にも取り組んでもらう必要がある。今後、作業で起こりやすいミスを網羅してあらかじめ作業用マニュアルに注意事項として書き込むなどの対策をとることが必要になる。

## Conclusion:
この研究を通じ、現段階での作業用マニュアルが作成された。今後、今回の台風19号よりもさらに被害の大きな災害が起こる可能性がある。その際に今のマニュアルでは対応しきれないことや新たな問題が発生するであろう。VCのデータ化作業中に起きた作業ミスや問題点を細かく把握し、随時作業用マニュアルを更新していくべきである。
## Reference/参考文献:
卒業論文本文中に記載。

## Acknowledgements/謝辞:
本研究を進めるにあたり古橋教授をはじめ多くの方々より多大な助言を賜りました。厚く感謝を申し上げます。


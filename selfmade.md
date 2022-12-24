
## 四方が10 cm以内PCBを使った自作キーボード
<br>

ElecrowやJLCPCBでは、四方が10cm以内の大きさのPCBを安価（１〜２ドル）で製造してくれます。
<br>
いざ、その大きさでは、マクロパッドは作れるが、普通のキーボード（ここでは、アルファベット26文字の入力ができるものを普通と考えます）は難しいと思っていました。
<br>
しかし、調べてみると、かぎざら屋さんのMiniAxeと言う素晴らしい36キーの分割キーボードが、この大きさの条件を満たしていることがわかりました。
<br>
そこで無謀にも、そのようなものを自分でも作れないかと設計したのが、cool640です。
<br>

<blockquote class="twitter-tweet" data-theme="dark"><p lang="ja" dir="ltr">PCBが100mmX100mm内の大きさで、<a href="https://twitter.com/hashtag/%E8%87%AA%E4%BD%9C%E3%82%AD%E3%83%BC%E3%83%9C%E3%83%BC%E3%83%89?src=hash&amp;ref_src=twsrc%5Etfw">#自作キーボード</a> が作れるかなと思い、挑戦しました。先日はPCBが150mmX100mmで <a href="https://twitter.com/hashtag/cool650?src=hash&amp;ref_src=twsrc%5Etfw">#cool650</a> になったので、今回は <a href="https://twitter.com/hashtag/cool640?src=hash&amp;ref_src=twsrc%5Etfw">#cool640</a> として、二つをケーブルで繋ぐと格子配列の分割になります。新しいこととして、<a href="https://twitter.com/hashtag/promicro?src=hash&amp;ref_src=twsrc%5Etfw">#promicro</a> と <a href="https://twitter.com/hashtag/%E3%83%A9%E3%82%BA%E3%83%91%E3%82%A4Pico?src=hash&amp;ref_src=twsrc%5Etfw">#ラズパイPico</a> に対応してみます。 <a href="https://t.co/dft7Hg7RUM">pic.twitter.com/dft7Hg7RUM</a></p>&mdash; m.ki（エム キ） (@0002ozlet) <a href="https://twitter.com/0002ozlet/status/1496460445955280901?ref_src=twsrc%5Etfw">February 23, 2022</a></blockquote>

<br>
後発ゆえに、pro microのみで動くのであれば、目新しさもないと思いました。そこで、cool836picoで使用実績のある、raspberry pi Picoとpro microの両方で動くものにしようと思う設計しました。
<br>
<br>

イメージ的にMCU部分は、pro microがスイッチ2個分、パイピコが3個分のスペースで置けるだろうし、その間にTRRSジャック一つ分の余裕があれば、何とかなるかなと考えました。そうなると、キー数は横5キーで、縦4キーの格子配列が適当だろうと、徐々に方針がさだまってきました。ちょうど、夜の散歩中に、妄想しながら、方向性を詰めていきました。
<br>
<br>
あとは設計です。Keyboard Layout Editerのサイトで、片手分20キーの格子配列を作りました。そして、jsonファイルを書き出して、kicadのプラグインで読み込むと、あっという間に配列されたものができました。ちょっと仕事の休みをもらっていたので、時間があったのですぐに作業に取り掛かることができました。
<br>
<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">10cmX10cm以内のPCBで、<a href="https://twitter.com/hashtag/%E8%87%AA%E4%BD%9C%E3%82%AD%E3%83%BC%E3%83%9C%E3%83%BC%E3%83%89?src=hash&amp;ref_src=twsrc%5Etfw">#自作キーボード</a> できるかなという課題の答えの一つです。<a href="https://twitter.com/hashtag/%E3%83%A9%E3%82%BA%E3%83%91%E3%82%A4pico?src=hash&amp;ref_src=twsrc%5Etfw">#ラズパイpico</a> か <a href="https://twitter.com/hashtag/promicro?src=hash&amp;ref_src=twsrc%5Etfw">#promicro</a> のどちらかで動くよう配線した、<a href="https://twitter.com/hashtag/cool640?src=hash&amp;ref_src=twsrc%5Etfw">#cool640</a> になります。二つをケーブルで繋いで分割キーボードになる予定。まずは基板届いたので、先に届いていたアクリルと仮組みしました。 <a href="https://t.co/L4Bbng5rMJ">pic.twitter.com/L4Bbng5rMJ</a></p>&mdash; m.ki（エム キ） (@0002ozlet) <a href="https://twitter.com/0002ozlet/status/1501177149167861761?ref_src=twsrc%5Etfw">March 8, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<br>
<br>
その後、それに合わせたアクリルのスイッチプレイヤーとボトムプレート、カバープレートを設計して発注しました。
<br>
<br>
cool640の目標は、私が自作キーボードを作り始めた時に、とても重宝したSU120のように、安価で誰でも好きに発注できる自作キーボードの基板にしたいと思っていました。それゆえ、あまり頒布することがメインでなく、各自ガーバーデータを発注して、好きにcool640を作ってもらえればいいかなと思っています。
<br>
<blockquote class="twitter-tweet"><p lang="ja" dir="ltr"><a href="https://twitter.com/hashtag/cool640?src=hash&amp;ref_src=twsrc%5Etfw">#cool640</a> が届いて、動作確認ができたら、データはgithub上に置いて、「ご自由に発注してどうぞ」にしたいと思っています。最初の自作の時、<a href="https://twitter.com/hashtag/SU120?src=hash&amp;ref_src=twsrc%5Etfw">#SU120</a> によって <a href="https://twitter.com/hashtag/%E8%87%AA%E4%BD%9C%E3%82%AD%E3%83%BC%E3%83%9C%E3%83%BC%E3%83%89?src=hash&amp;ref_src=twsrc%5Etfw">#自作キーボード</a> の楽しさが増したので、その形に倣えたらいいなと思っています。</p>&mdash; m.ki（エム キ） (@0002ozlet) <a href="https://twitter.com/0002ozlet/status/1497045745970540550?ref_src=twsrc%5Etfw">February 25, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
<br>
それでも発注することのハードルが高いと思う人のため、boothでの頒布もしています。値段の方は、手間賃を含むと、1枚500円になってしまいますね。
 <br>
 <br>
cool640を作ったあと、四方10cm以内の条件で、他の配列のキーボードを作ることができないかと自問自答した結果出来上がったのが、cool536です。
<br>
<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">昨日、思いつきで設計しました。先ほど、<a href="https://twitter.com/hashtag/elecrow?src=hash&amp;ref_src=twsrc%5Etfw">#elecrow</a> に発注をかけました。先週も、<a href="https://twitter.com/hashtag/cool445?src=hash&amp;ref_src=twsrc%5Etfw">#cool445</a> と名付けたものを発注して、今週は、<a href="https://twitter.com/hashtag/cool536?src=hash&amp;ref_src=twsrc%5Etfw">#cool536</a> となる <a href="https://twitter.com/hashtag/100mmX100mm%E4%BB%A5%E5%86%85%E3%81%AEPCB?src=hash&amp;ref_src=twsrc%5Etfw">#100mmX100mm以内のPCB</a> で作る <a href="https://twitter.com/hashtag/%E8%87%AA%E4%BD%9C%E3%82%AD%E3%83%BC%E3%83%9C%E3%83%BC%E3%83%89?src=hash&amp;ref_src=twsrc%5Etfw">#自作キーボード</a> です。カラムスタッガードに挑戦です。夏休みを満喫できそうです。 <a href="https://t.co/3cqAOGAGIp">pic.twitter.com/3cqAOGAGIp</a></p>&mdash; m.ki（エム キ） (@0002ozlet) <a href="https://twitter.com/0002ozlet/status/1548638040725172224?ref_src=twsrc%5Etfw">July 17, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<br>
<br>
カラムスタッガードにしたため、リバーシブルの基板となりました。中指で入力する縦列の関係上、パイピコを載せるのが無理とわかりました。その分空いたスペースに何か入れようと思った結果、現在のような、ロータリーエンコーダーが2個または、OLEDディスプレイ、追加基板を使ってPIM447trackballを追加できるような使用となりました。ちょうど、cool536設計のちょっと前に、cool650にロータリーエンコーダーを載せたり、cool640にロータリーエンコーダーを載せたりと、私の中でロータリーエンコーダー祭りが開かれていました。結局、ピン数の関係で、cool640のロータリーエンコーダーは難しいとわかり、諦めました。cool650はロータリーエンコーダーも装着可の基板になりました。
ずっと仕事場でメインで使っているキーボードは、cool943Sという2年前にSU120で最初作って、その後、kicadで設計した40％分割キーボードです。ロウスタッガードから離れられませんでした。そこから、cool650、cool640でオルソスタッガードもいけるかもと思うようになり、遂にcool536でカラムスタッガードになりました。
# question_answer.md
ワークサンプル提出


質問内容
カリキュラム中の、 
『4.ifの条件式について』内のコードについて曖昧な点があったので質問します。

if true # trueという値そのもの
  puts "あなたは未成年です(2)" # 処理が実行される
end

if trueで始まる式を、自分は「もしtrueであれば、以下の処理を実行する」という意味だと考えてます。
しかし、なんの式に対して、何がtrueなのか？
上のif age < 20は分かりやすいです。「もしageが20より小さいならば〜」という条件の式がある。
しかしこのif trueは、何がtrueの時に実行されるのかがよくわかりません。
教えてください。


■if文■
●if文の基本構文●
if文は次のような構文である．

if(条件式)
{
  条件式が真(true)だった時に実行される部分
}
else
{
  条件式が偽(false)だった時に実行される部分
}
括弧内の条件式の結果が真(true)か偽(false)によって動作が分岐して，条件式の結果次第でどちら一方だけを実行する．条件式が真になることを「条件(式)が成立する」と表現する．

「else」以下は必要なければ省略することもできる．また，条件が成立した時，しなかった時に実行される部分が実行文ひとつだけの場合には，中括弧を省略することもできる．

●複合されたif文●
条件が成立したとき，しないときに実行する部分には，さらに別のif文を書くこともできる．これにより複雑な条件分岐を記述することができる．

if(条件式1)
{
  if(条件式2)
  {
      実行部分A
  }
  else
  {
      実行部分B
  }
}
else{
  if(条件式3)
  {
      実行部分C
  }
  else
  {
      実行部分D
  }
}
この例では，次のように動作し，4つの実行部分(A,B,C,D)のうちひとつだけ実行が行われる．(他は実行されない)

条件式1と条件式2が両方成立したとき → 実行部分Aを実行
条件式1が成立，条件式2が成立しない → 実行部分Bを実行
条件式1が成立せず，条件式3が成立 → 実行部分Cを実行
条件式1と条件式3が両方成立しない → 実行部分Dを実行
ここで実行部分といっているのは，複数の実行文(代入文やif文やswitch文など)を含んで良い．

●連続したif文●
複数のif文を使ってよく書かれるプログラム例が次のような連続的なif文である．

if(条件式1)
{
    条件式1が成立したときの実行部分 
}
else if(条件式2)
{
    (条件式1が成立せず)条件2が成立したときの実行部分 
}
else if(条件式3)
{
    (条件式1と条件式2が成立せず)条件式3が成立したときの実行部分 
}
else
{
    条件式1も2も3も成立しないときの実行部分 
}
この例は，最初に説明したように，各elseのところの実行文が次のif文ひとつだけなので，中括弧を省略して書いてある．省略せずに書けば，本来は次のような意味である．(省略しない方が逆に読みにくく，書くのも面倒なので普通はこうは書かない)

if(条件式1)
{
    条件式1が成立したときの実行文 
}
else
{
    if(条件式2)
    {
        (条件式1が成立せず)条件式2が成立したときの実行文 
    }
    else
    {
        if(条件式3)
        {
            (条件式1と条件式2が成立せず)条件式3が成立したときの実行文 
        }
        else
        {
            条件式1も2も3も成立しないときの実行文 

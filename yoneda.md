## 米田の補題と自然変換

ここでは自然変換を定義し、その上で米田の補題を証明していきます。
数学の色々な概念を導入することは避け、基本的な集合についての知識の範囲内で収まるように説明することを心がけています。

### 集合と写像
ここではまず圏について述べるために必要な集合と写像の言葉について復習します。
また、これらが圏や関手、自然変換の例を与えることを見ていきます。

様々な集合に関する操作において自然な同一視、自然な写像というものが出てきますが、これらが自然変換の例であるということを述べています。

具体的には写像の集合Homを取る操作や冪集合を取る操作、直積を取る操作などについて書いてあります。

[pdf](set.pdf)
公開日2018年7月11日

### 順序集合
ここでは順序集合について紹介しています。
順序集合というのは集合とその要素間の大小関係を抽象化したもので、例えば通常の整数全体の集合に通常の大小関係を定めたものは順序集合の例です。

これ以外にも、集合Xの冪集合P(X)を考えると、それらの要素の間に集合が含まれるか否かということから大小関係を考えることができ、これも順序集合の例を与えています。
このような順序集合においては、全ての要素の間に必ずしも大小関係が成り立つとは限りません。

順序集合たちを考える上で、それらの関係を記述するために順序集合の射というものを定義します。
これは二つの集合の間の写像の中で、順序関係を保つように定まっているもののことです。
例えば上の整数全体と通常の大小による順序集合においては、全てを+1するという写像は順序集合の射ですが、-1掛けるという写像は順序集合の射になりません。

順序集合をここで紹介したのは、それが単純な圏の例を与えるためです。
つまり、ある順序集合があれば、それを一つの圏とみなすことができます。
例えば整数全体の集合と通常の大小関係から定まる圏、ある集合Xの冪集合P(X)と包含関係による大小関係から定まる圏、といったようにです。

この観点から、順序集合に対する米田の補題というべき性質を紹介しました。
ある順序集合Xにおいて、その要素を特定するためにはその要素以下の要素を全て列挙すればよいというものです。
全ての要素が一列に並んでいるような順序集合ではこれは当たり前で、要するに順番に並べて何番目かを見ればわかるということをいっています。

このような内容を以下のpdfにまとめました。

[pdf](poset.pdf)
公開日2018年7月12日

### 圏と関手
ここでは圏と関手の定義を紹介し、基本的な例をいくつか紹介します。

圏とは対象と呼ばれるものの集まりと、各対象の間に射と呼ばれる矢印の集まりを定めたものです。
例えば集合の圏であれば、集合全て集めたものが対象、二つの集合の間の射は二つの集合の間の写像です。

関手とは二つの圏を結びつけるもので、それぞれの対象をどのように対応させるか、それぞれの射をどのように対応させるか、をしかるべき条件をみたすように決めます。

前に紹介した順序集合は特別な性質をみたす圏とみなすことができます。
順序集合Xが与えられたとき、圏をその対象がXの要素全体、xとyの間の射としてもしx <= y であれば一つ存在し、そうでなければ射は存在しない、とします。
一般の圏においては、二つの対象の間の射はたくさんあってもよいのですが、もし二つの対象の間の射が1つ以下であるような圏を考えると、それは順序集合を考えるのと同じことになります。

また表現可能関手と呼ばれる特別な関手を定義します。
これは圏Cの対象xを用いて定まる、圏Cから集合の圏Setsへの関手です。
詳細な定義はpdfに書きますが、
この関手は圏Cにおける対象xと他の対象との関係を全て記述するものであり、
このような表現可能関手の性質を明らかにするのが米田の補題です。

[pdf](cat_funct.pdf)
公開日2018年7月13日


### 自然変換
ここまでいくつかの例において、自然な対応、自然な写像といったものがでてきました。
ここでは改めてその例を見ながら、自然変換の定義を確認していきます。

自然変換は二つの関手を結び付けるためのものです。
例えば、二つの集合の組(X,Y)から、その直積X x Yを対応させることで関手が定まり、
一方で、(X, Y)からY x Xを対応させることでも関手が定まります。
この二つの関手は、見た目は異なるものの、X x Yという集合とY x Xという集合は二つの成分を入れ替えることで、同一視できます。
ここでポイントとなるのは、X x YとY x Xの同一視がXやYという集合を色々入れ替えても全く統一的にできるというところにあります。
このような性質をもって、自然変換を定義します。

このpdfでは、自然変換の定義を一般的に行う前に、いくつかの例を通して自然変換という概念に触れてもらうという構成にしてみました。
特に、冪集合の例は、この後の米田の補題の応用としてドモルガンの定理を証明する際に必要になるので、ぜひ手を動かして考えながら読んでいただければと思います。

二つの圏C, Dに対して、その間の関手全体の圏C^Dを考えることができ、
この関手の圏の射こそが自然変換です。
pdfの終わりに、このようにして自然変換を定義しています。

[pdf](nat.pdf)
公開日2018年7月19日


### 米田の補題と表現可能関手
ここでは米田の補題についてその主張と証明を紹介します。

表現可能関手と呼ばれる良い関手があります。
これは圏Cの対象を用いて定義されるCから集合の圏への反変関手です。
実はここまでにも出てきたものですが、まずはこれを定義しいくつかの例を見ます。

次に米田の補題の主張を紹介します。
米田の補題は圏Cを表現可能関手を考えることでCから集合の圏への関手のなす圏に埋め込めることを主張するもので、これにより圏Cの様子を集合の言葉を用いて調べることができます。

さらに、数直線上の関数から定まる関手の例を用いて、米田の補題がどのようなことを主張しているのか見たのち、米田の補題を証明します。
できるだけ式変形を丁寧に説明しましたが、逆に長く読みづらくなってしまったかもしれません。

最後に、冪集合関手について米田の補題を応用することで、ドモルガンの定理を証明します。
ここでも具体例を通して米田の補題の証明に触れるので、上の証明がわかりづらい場合にも具体例と合わせてお読みいただくとよいと思います。

[pdf](yoneda.pdf)
公開日2018年9月21日

[上のページ](category.md)
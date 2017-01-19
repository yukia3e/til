# UnityのAttribute
http://tsubakit1.hateblo.jp/entry/2015/01/03/203843

- 複数記載する場合  
[SerializeField, Range(0, 1)]

- [ExecuteInEditMode]  
Playモードでないとき(==Editモード)にスクリプトを実行できるようになる。  
http://qiita.com/okuhiiro/items/0121fc26c0b80a4673a0

- [AddComponentMenu(“〜”)]  
Componentメニューへの表示  
http://www.wisdomsoft.jp/653.html

- [SerializeField]  
「設計的にはprivateにしたい。だけれどインスペクタで値を調整したい」という場面で利用する  
http://qiita.com/momomo/items/f8c16004123f38e86fc0

- [Range(0, 1)]  
入力可能範囲の指定  


# C#について
- \#region  
C#の機能。エディタ上で折りたたむことができるようになる  
http://icoc-dev.hatenablog.com/entry/2014/01/15/090644

- propertyの記載  
```
public Vector3 emitterCenter {
    get { return _emitterCenter; }
    set { _emitterCenter = value; }
}
```

# rails_tutorial

##  環境構築
- railsはシステムのものでなくrbenv経由でインストールしたものを使用する
which rubyやwhich gemで`/usr/bin/ruby` が出た場合システムのものを使っている

```
$ brew update
$ brew install rbenv ruby-build
```
最初はsystemがデフォルトになっているので
```
$ rbenv versions
* system (set by /Users/${ユーザー名}/.rbenv/version)
```
railsガイドのここに書いてあるバージョンをインストールする。2024.4現在は3.2.3。だがrbenv install -lにないので、3.2.4
https://railstutorial.jp/chapters/beginning?version=7.0#:~:text=%24-,ruby%20%2D%2Dversion,-ruby%203.2.3%20(2024
```
$ rbenv install 3.2.4
$ rbenv global 3.2.4

# 失敗するときは
# https://kenzoblog.vercel.app/posts/m1-chip
$ rbenv install 3.2.4 RUBY_CFLAGS="-w"
```
`/Users/${ユーザー名}/.rbenv/shims/ruby` になればOK

⇨ M2macだと失敗する(解決していない)
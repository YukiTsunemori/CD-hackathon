
# CodeBase-hackathon
Codebase卒業生によるHackathon開催、READMEです。 
今回はmainブランチへpushしていきます。  
以下は、今回使用するRailsのバージョンと、よく使うgitコマンドについてまとめたので、わからなくなったら見返せるようにしました。

# Rails verとデータベース
Railsのヴァージョンは特にこだわりがなければ最新のものを使おうと思います。(今回は、Rails 8.0.2)  GemfileにあるRailsのヴァージョンとローカルのRailsヴァージョンは合わせるようにしてください。  
データーベースはCodebaseでも使用したPostgreSQLを使用しようと思います。  

# gitコマンド
今回、git/githubで履歴管理をおこない、より実際の現場に近い形でアプリケーションをものにしていこうと思います。


## git clone
```
https://github.com/YukiTsunemori/CD-hackathon.git
```

※すでに初期化(git init)済みなのでローカルでこちらの操作は不要です。

## git checkout
実装する機能をfeature/ブランチ名でチェックアウトしましょう。  
"何の作業をしているか"、がわかるようにしましょう。  

例：feature/login_page(or login-page)  

ブランチ名はスネークケースやハイフンを使うなど、様々ですがチーム内で統一した方がいいかも👀

## git add
 
 ```git add .``` or ```git add -A```  
 このコマンドで編集履歴に残す準備をします。    
 上二つのコマンドはよく教材に出てきますが、厳密には全てのファイルの最新情報がアップされるため、事前にpullしておらず白紙(ファイルだけが存在し中身がない)のものまでアップされます。その間、別のメンバーが編集したファイルまでも白紙になるため、addするのは編集したファイルだけを指定する方が確実かもしれません。👀

## git commit 
編集したファイルを後々追跡できるよう記録を残すコマンドです。  
その際、-mオプションをつけることで、"どのファイルに何の機能また描画をつけたか"をメッセージとして残すことができます。
```
git commit -m "Implement login-page(ログイン機能の実装)"
```
## git push
いよいよ、ローカル(手元のPC)からリモート(Github)のリポジトリへ変更をアップロードします。  
チェックアウト後の初回のpushの際は、-u origin ブランチ名をつける必要があります。
```
git push -u origin ブランチ名
```
~~今回、各自が実装する機能またはhtmlなどのファイルをpushする際は、developブランチへpushするようにします。~~  
```
git push origin -u feature/login_page
```

以後のコマンドはgit pushのみでOK👍

## git pull　(特に注意)
git pullでリモートリポジトリの最新情報をローカルリポジトリへ更新します。  
リポジトリの編集は複数人で行うため、誰かがmainへマージしたタイミングでpullするようにしましょう。
pullをせず、自分のPCにある古いファイルを誤ってpush指定しまうと古いファイルが上書きされてしまうので、注意が必要です。📴

# Pull request
各チームの誰か一人がdevelopブランチへのmergeをするか、順番に回すかはチームの判断とします。  
pull requestの教材を松田さんが過去に作成していたものを他の卒業生の方からいただいたので、リンク載せておきます。  
https://docs.google.com/presentation/d/1Lf2MF9g0i9Zxs5H0BOwwrGdWIqBc0qvWE9Yvzf2w_pc/edit?slide=id.ge2fb718087_0_5#slide=id.ge2fb718087_0_5

github command

- githubのsetup

`$ git config --global user.name "Your Name"`

`$ git config --global user.email your.email@example.com`

`$ git config --global push.default matching`

`$ git config --global alias.co checkout`

- 初めてのpush
`$ echo "# experiment_class" >> README.md`

`$ git init`

`$ git add .`

`$ git commit -m "hogehoge"`

`$ git remote add origin https://github.com/jabelic/hogehoge.git`

`$ git push origin master`


- 更新の仕方

`$ git add .`

`$ git commit -m "hogehoge"`

`$ git push origin master`

- クローン

`$ git clone [url]`

- 他のPCのから自分のgithubに変更を加える

githubのsetup -> クローン -> 更新

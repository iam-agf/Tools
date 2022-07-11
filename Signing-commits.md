If you're in a Mac, 

* Create a gpg id. with `gpg --full-generate-key`. Add your mail used for github and any name.
* Type `gpg --list-secret-keys --keyid-format=long` to check the signatures you have registered/created.
* Copy the signature of the key, the text after `4096/HERE`
* Add the key via the terminal with `git config --global user.signingkey KEY-YOU-COPIED-HERE`
* Make git ask you to sign your commits with `git config --global commit.gpgsign true` 

Now each time you want to sign a commit, you have to add the command `-S`. For example:


```
git add file.txt
git commit -S -m "my commit is signed"
```

And that's all.

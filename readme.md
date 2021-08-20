Create a new repository, or reuse an existing one.

Generate a new SSH key:
~~~
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
~~~
Copy the contents of the file ~/.ssh/id_rsa.pub to your SSH keys in your GitHub account settings (https://github.com/settings/keys).

Test SSH key:
~~~
ssh -T git@github.com
~~~
Hi! You've successfully authenticated, but GitHub does not provide shell access.
Change directory into the local clone of your repository (if you're not already there) and run:
~~~
git remote set-url origin git@github.com:username/your-repository.git
~~~
Now try editing a file (try the README) and then do:
~~~
$ git commit -am "Update README.md"
$ git push
~~~

You should not be asked for a username or password. If it works, your SSH key is correctly configured.

ref: [Generating a new SSH key and adding it to the ssh-agent](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

forked by [https://gist.github.com/developius/c81f021eb5c5916013dc](https://gist.github.com/developius/c81f021eb5c5916013dc)

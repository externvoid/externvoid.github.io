---
layout: post
title:  "How to push"
date:   2019年 9月24日 火曜日 06時55分56秒 JST
categories: Default
tags: git
comments: 1
---
## トラブル解消だよね
date:   2019-09-23 21:00:07
2019年 9月24日 火曜日 05時49分56秒 JST

```bash
801> git push
To https://github.com/externvoid/externvoid.github.io.git
 ! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'https://github.com/externvoid/externvoid.github.io.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

806> git pull
fatal: refusing to merge unrelated histories

807> git merge --allow-unrelated-his
tories origin/master
Auto-merging _config.yml
CONFLICT (add/add): Merge conflict in _config.yml
Automatic merge failed; fix conflicts and then commit the result.

808> !v
811> git add _config.yml 
812> git cm -m "fix conflict"
[master dce4081] fix conflict
813> git push
Enumerating objects: 151, done.
Counting objects: 100% (151/151), done.
Delta compression using up to 8 threads
Compressing objects: 100% (147/147), done.
Writing objects: 100% (149/149), 4.41 MiB | 2.24 MiB/s, done.
Total 149 (delta 5), reused 0 (delta 0)
remote: Resolving deltas: 100% (5/5), done.
To https://github.com/externvoid/externvoid.github.io.git
   4ed8a18..dce4081  master -> master
```

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/

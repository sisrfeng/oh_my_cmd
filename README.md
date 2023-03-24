Has been moved to https://gitee.com/llwwff/dotF

---


# Oh-My-Terminal

**zsh+tmux+vim**

 ```bash
 rm -r ~/dotF
 export ALL_PROXY=socks5://你的ip:端口
 yes | (apt-get install git)
 cd ~ && git clone https://github.com/sisrfeng/dotF.git && cd ~/dotF
 bash auto_install.sh
 ```




 ---

## All Other Content is Just for Backup
1. 【已修复】ctrl R 一直是tmux的reload的快捷键，改了tmux.s还是不行，导致vim中用不了ctrl R
2. Something strange:
 And in `~/.zshrc`, I write `source ~/dotF/.zshrc` then `export PS1="@ "  `
 In `~/dotF/.zshrc`, there was already `export PS1=">>at_here>>"`
 Surprisingly,  `~/dotF/.zshrc`, instead of `~/.zshrc` takes effect.
 After removing `~/dotF/.zshrc`, things go right.


### 没事别看:

之前把zplug直接git clone到dot__file下, 导致同步时_,zplug这个submodule难处理. 现在clone到~/下了
* About git submodule
 this arrow means a soft link OR a submodule
 ![image](https://user-images.githubusercontent.com/53520949/134790530-feaea641-0da6-4483-b311-3f8301f9629b.png)

如果希望git clone时，子模块代码也能获取到:
* 方法1
`git clone https://github.com/username/repo名字.git --recurse-submodules `
此时project-main/project-sub-1文件夹是有内容的，（但不是project-sub-1的原作者的最新版本？）

* 方法2
git clone外层repo后，这样拉取子模块的原作者的最新代码
```
git submodule init
git submodule update
```
ref:
https://www.atlassian.com/git/tutorials/git-submodule

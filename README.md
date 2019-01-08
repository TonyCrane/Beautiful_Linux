# Linux美化

## 目录
- [x] README.md
- [x] Forever_by_Shady_S.jpg
- [x] molokai.vim 
- [x] Monaco_Powerline.otf 
- [x] vimrc.txt

---
## 美化
### I. 初步系统优化
- 更改系统时间
- 安装python<br>
	`sudo apt install python`
- 安装git并添加ssh密钥<br>
	`sudo apt install git`<br>
	`git config --global user.name "your_name"`<br>
	`git config --global user.email "you@example.com"`<br>
	`ssh-keygen -t rsa -C "your_email@youremail.com"`一路回车<br>
	`cat ~/.ssh/id_rsa.pub`并复制粘贴到github上<br>
	`ssh -T git@github.com`测试<br>
	`git clone https://github.com/Tony031218/Beautiful_Linux.git`克隆下本仓库
- 添加语言
<pre>
	settings -> Region&Language -> manage installed language -> install/remove languages
	                            -> input sources
</pre>
- 软件更新<br>
	`sudo apt update`<br>
	`sudo apt upgrade`
- 安装GDebi<br>
	`sudo apt install gdebi`
- 卸载libreoffice 安装 WPS(可选)<br>
	`sudo apt remove libreoffice-common`<br>
	从http://www.wps.cn/product/wpslinux/ 上下载WPS
	`sudo dpkg -i wps-office_10.1.0.6757_amd64.deb`
- 卸载firefox 安装 Chrome(可选)<br>
	`sudo apt remove firefox`<br>
	`wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb`<br>
	`sudo dpkg -i google-chrome*`<br>
	`sudo apt -f install`
- 更换更新源<br>
	左下角 -> all -> Software&Updates<br>
	`sudo apt update`
- 安装vim<br>
	`sudo apt install vim`
- 菜单栏位置<br>
	`gsettings set com.canonical.Unity.Launcher launcher-position Bottom`底部<br>
	`gsettings set com.canonical.Unity.Launcher launcher-position Left`左侧

### II. 主题配置

- 安装 Unity-tweak-tool<br>
  `sudo apt install unity-tweak-tool`<br>
  如果出现报错需要安装缺失的包

- 安装 Flatabulous 主题<br>
  `sudo add-apt-repository ppa:noobslab/themes`<br>
  `sudo apt update`<br>
  `sudo apt install flatabulous-theme`主题<br>
  `sudo add-apt-repository ppa:noobslab/icons`<br>
  `sudo apt update`<br>
  `sudo apt install ultra-flat-icons`图标<br>
  unity-tweak-tool -> 主题/图标

- 字体<br>
  Monaco Powerline 也可以选择其他字体,但一定要支持Powerline的,否则后文会出现乱码

### III. 终端Terminal美化

- Terminal zsh<br>
	`sudo apt install zsh`<br>
	`git clone https://github.com/robbyrussell/oh-my-zsh.git`<br>
	`cd oh-my-zsh/tools`<br>
	`./install.sh`
- 更换默认shell<br>
	`chsh`按步骤来输入zsh地址
- zsh插件
	+ 自动补全<br>
		`git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions`
	+ 快速跳转<br>
		`git clone https://github.com/joelthelion/autojump.git`<br>
		`cd autojump`<br>
		`./install.py`按要求把代码填写到~/.zshrc文件尾
	+ 配置<br>
		`vim ~/.zshrc`<br>
		修改60行左右的plugins`plugins=(git autojump zsh-suggestions)`
	+ 修改皮肤<br>
		`~/.zshrc`中的`ZSH_THEME="robbyrussell"`更改

### IV. vim美化
- molokai<br>
	`mkdir ~/.vim/colors`<br>
	将本仓库中的`molokai.vim`复制到`~/.vim/colors/`下
- Powerline<br>
	`sudo apt install python-pip`<br>
	`pip install git+git://github.com/powerline/powerline`<br>
	`pip show powerline-status`<br>
	按照具体位置更改`~/.vimrc`中的`set rtp+=...`一行(后文)
- 插件
	+ pathogen插件管理
		```shell
		mkdir -p ~/.vim/autoload ~/.vim/bundle
		curl -LSso ~/.vim/autoload/pathogen.vim https://tpo.pe/pathogen.vim
		```
	+ nerdtree文件浏览器
		```shell
		cd ~/.vim/bundle
		git clone https://github.com/scrooloose/nerdtree.git
		```
	+ taglist大纲界面<br>
[taglist](https://www.vim.org/scripts/scripts.php?script_id=273)<br>
		下载后解压到`~/.vim/bundle/`下
- vimrc<br>
	将本仓库中的`vimrc.txt`复制到`~/.vimrc`中<br>
	内包含括号匹配,html标签匹配,powerline配置(可能需要改动),cpp.sh.java.py的文件头自动输入,插件的配置(F3打开nerdtree,F4打开taglist)

## 参考
[CSDN博客](https://blog.csdn.net/qq_35208390/article/details/78441013)<br>
[powerline](https://www.linuxprobe.com/use-powerline-for-bash.html)<br>
[vim插件](https://blog.csdn.net/zcube/article/details/42525973)<br>
[monaco powerline字体](https://github.com/ocxo/monaco-powerline-vim)<br>
[monokai主题](https://github.com/sickill/vim-monokai)<br>
[WPS](http://www.wps.cn/product/wpslinux/)

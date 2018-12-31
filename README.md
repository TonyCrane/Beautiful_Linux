# Linux美化

## 目录

---
## 美化
### I. 初步系统优化
- 更改系统时间
- 安装git并添加ssh密钥&nbsp
	`sudo apt install git`&nbsp
	`git config --global user.name "your_name"`&nbsp
	`git config --global user.email "you@example.com"`&nbsp
	`ssh-keygen -t rsa -C "your_email@youremail.com"`一路回车&nbsp
	`cat ~/.ssh/id_rsa.pub`并复制粘贴到github上&nbsp
	`ssh -T git@github.com`测试&nbsp
	`git clone https://github.com/Tony031218/Beautiful_Linux.git`克隆下本仓库
- 添加语言
<pre>
	settings -> Region&Language -> manage installed language -> install/remove languages
	                            -> input sources
</pre>
- 软件更新&nbsp
	`sudo apt update`&nbsp
	`sudo apt upgrade`
- 安装GDebi&nbsp
	`sudo apt install gdebi`
- 卸载libreoffice 安装 WPS(可选)&nbsp
	`sudo apt remove libreoffice-common`&nbsp
	`sudo dpkg -i wps-office_10.1.0.6757_amd64.deb`
- 卸载firefox 安装 Chrome(可选)&nbsp
	`sudo apt remove firefox`&nbsp
	`wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb`&nbsp
	`sudo dpkg -i google-chrome*`&nbsp
	`sudo apt -f install`
- 更换更新源&nbsp
	左下角 -> all -> Software&Updates&nbsp
	`sudo apt update`
- 安装vim&nbsp
	`sudo apt install vim`

### 主题配置

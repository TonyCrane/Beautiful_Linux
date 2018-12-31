# Linux美化

## 目录

---
## 美化
### I. 初步系统优化
- 更改系统时间
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

### 主题配置

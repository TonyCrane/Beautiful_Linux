# Linux美化

## 目录

---
## 美化
### I. 初步系统优化
- 更改系统时间
- 安装git并添加ssh密钥

	`sudo apt install git`
	
	`git config --global user.name "your_name"`
	
	`git config --global user.email "you@example.com"`
	
	`ssh-keygen -t rsa -C "your_email@youremail.com"`一路回车
	
	`cat ~/.ssh/id_rsa.pub`并复制粘贴到github上
	
	`ssh -T git@github.com`测试
	
	`git clone https://github.com/Tony031218/Beautiful_Linux.git`克隆下本仓库
- 添加语言
<pre>
	settings -> Region&Language -> manage installed language -> install/remove languages
	                            -> input sources
</pre>
- 软件更新

	`sudo apt update`
	
	`sudo apt upgrade`
- 安装GDebi
	
	`sudo apt install gdebi`
- 卸载libreoffice 安装 WPS(可选)
	
	`sudo apt remove libreoffice-common`
	
	`sudo dpkg -i wps-office_10.1.0.6757_amd64.deb`
- 卸载firefox 安装 Chrome(可选)
	
	`sudo apt remove firefox`
	
	`wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb`
	
	`sudo dpkg -i google-chrome*`
	
	`sudo apt -f install`
- 更换更新源
	
	左下角 -> all -> Software&Updates
	
	`sudo apt update`
- 安装vim
	
	`sudo apt install vim`

### 主题配置

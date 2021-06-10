# setting
### keyboard
```
sudo apt-get update
sudo apt-get install fcitx-hangul
```
설정 > 지역 및 언어 > 설치된 언어 관리 > 입력기 > fcitx
```
reboot
```


## jupyter lab
### 서비스 등록하기
```
sudo vi /etc/systemd/system/jupyter.service

# 파일 내용
[Unit]
Description=Jupyter Notebook Server

[Service]
User=sasim
ExecStart=/usr/local/bin/jupyter-lab
WorkingDirectory=/home/sasim/jupyter

[Install]
WantedBy=multi-user.target

# 서비스 등록 및 활성화
sudo systemctl daemon-reload 
sudo systemctl enable jupyter.service 
sudo systemctl start jupyter.service

# 서비스 상태 확인
sudo systemctl status jupyter.service
```

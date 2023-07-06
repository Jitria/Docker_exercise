# 기존에 설치된 도커 커뮤니티 에디션과 도커 엔진을 제거
sudo apt-get remove docker docker-engine docker.io containerd runc

# 저장소를 추가하는데 필요한 패키지를 설치
sudo apt-get update
sudo apt-get install apt-transport-https ca-certificates curl gnupg-agent software-properties-common

# 도커 패키지 저장소를 인증하기 위한 인증 키를 추가
curl –fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add –

# 인증 키가 추가됐는지 확인
sudo apt-key fingerprint 0EBFCD88

# 안정 버전을 제공하는 저장소를 추가
sudo add-apt-repository “deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable”

# 새로 추가된 저장소의 패키지 정보를 업데이트한 다음, 도커 엔진 패키지를 설치
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io

# 도커 컴포즈 설치(https://github.com/docker/compose/releases)
sudo curl –L “https://github.com/docker/compose/releases/download/[최신 버전]/docker-compose-$(uname -s)-$(uname -m)” –o /usr/local/bin/docker-compose
sudo chmod –x /usr/local/bin/docker-compose

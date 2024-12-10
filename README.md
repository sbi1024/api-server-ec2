### 특이사항
24.12.09 : health API 추가

# 개요
[[aws] ec2를 통해 백엔드 api 서버 배포하기 (2)](https://sbi1024.github.io/devops/aws/2) 블로그의 게시글에서 sample로 제공되는 프로젝트 입니다.

# 관련 블로그 글
[[aws] ec2를 통해 백엔드 api 서버 배포하기 (1)](https://sbi1024.github.io/devops/aws/1)
[[aws] ec2를 통해 백엔드 api 서버 배포하기 (2)](https://sbi1024.github.io/devops/aws/2)
[[aws] route53을 통해 도메인 구매하고 연결하기](https://sbi1024.github.io/devops/aws/3)
[][aws] elb(load balance)에 https 연결하기(https://sbi1024.github.io/devops/aws/4)


# 사용법
위 블로그의 게시글을 읽으셨다는 가정하에, 아래의 명령어를 통해 위 프로젝트를 aws ec2 ubuntu 환경에서 실행하시면 됩니다.

1. sudo apt update
2. sudo apt install openjdk-17-jdk -y
3. git clone https://github.com/sbi1024/api.git
4. cd api
5. ./gradlew clean build
6. cd ~/api/build/libs
7. sudo java -jar api-0.0.1-SNAPSHOT.jar

# 결과
7번의 `sudo java -jar api-0.0.1-SNAPSHOT.jar` 실행후 port 80 으로 실행되는지 확인필요.

<img width="1885" alt="스크린샷 2024-12-01 오후 2 15 15" src="https://github.com/user-attachments/assets/75985111-5059-4744-a00f-aaed8830af4b">

본인의 ipv4 값으로 브라우저 접속시에 다음과 같은 문구가 화면에 출력되어야 합니다.

<img width="1907" alt="스크린샷 2024-12-01 오후 2 18 18" src="https://github.com/user-attachments/assets/44a9772b-c3b3-496d-b5a2-33bbbd08fb00">

문구가 정상적으로 출력되었다면 ec2를 통해 위 sample 프로젝트가 정상적으로 배포되었음을 알 수 있습니다.

      
      
      

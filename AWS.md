### aws 설치방법
[참고자료](https://docs.aws.amazon.com/ko_kr/cli/latest/userguide/getting-started-install.html)
### 웹서버 (S3) 배포방법
[참고자료](https://lovit.github.io/aws/2019/01/30/aws_s3_iam_awscli/)

docker 컨테이너 통해서.. ?
mysql docker를 하나 띄워서 .. 연결해보라. .. ?

arm 아키텍쳐 기반

EC2로 웹서버 만들기
[참고자료](https://signalfix.net/ko/aws-ec2%EB%A1%9C-%EC%9D%B8%EC%8A%A4%ED%84%B4%EC%8A%A4%EB%A5%BC-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B3%A0-%EC%9B%B9-%EC%82%AC%EC%9D%B4%ED%8A%B8%EB%A5%BC-%ED%98%B8%EC%8A%A4%ED%8C%85%ED%95%98%EB%8A%94)
[참고자료2](https://velog.io/@mingtorr/AWS-EC2%EB%A1%9C-%ED%99%88%ED%8E%98%EC%9D%B4%EC%A7%80-%EB%B0%B0%ED%8F%AC%ED%95%98%EA%B8%B03-EC2-%EC%9D%B8%EC%8A%A4%ED%84%B4%EC%8A%A4-%EC%83%9D%EC%84%B1%ED%95%98%EA%B8%B0)

1. 키페어 가져오기 방법

공개키 얻는 방법
```
$ ssh-keygen -y
```
입력 후 .pem 파일명 입력

권한 바꾸는 방법 !! 반드시 폴더가 아닌 해당 파일에 권한을 부여해야함
*너무 많은 권한이 부여되면 또 에러나므로.. 400으로 부여함.
4(읽기) 2(쓰기) 실행(1)
```
sudo chmod -R [권한] [파일경로]
```

Mac에서 폴더 경로 얻는 방법
cmd+i > 해당 폴더 경로가 나온다~ 복붙해서 사용하면 된다

ssh-rsa 부터 복붙해서 가져오면 된다.

!성공!
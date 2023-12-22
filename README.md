# Jenkins 설치

###### namespace 생성   
`kubectl create namespace jenkins`   

<br>

###### jenkins deployment, service 생성   
`kubectl apply -f jenkins_deployment.yaml`   
`kubectl apply -f jenkins_service.yaml`   

<br>

###### pod 확인   
`kubectl get all -n jenkins -o wide`    
<img width="1036" alt="image" src="https://github.com/2023-opensw/Jenkins/assets/98319466/fefef245-0736-4796-8dde-aaa7988f9020">

<br><br>

###### jenkins 초기 설정   
`kubectl logs <pod name> -n jenkins`   
위의 명령어를 통해 알아낸 jenkins-password 를 이용    <br>
   
`localhost:30000 / <wsl ip>:30000` 으로 접속하여 젠킨스 초기 설정 후 레포지토리 연동   
<img width="626" alt="image" src="https://github.com/2023-opensw/Jenkins/assets/98319466/2fdb7c15-951a-44ac-a2c2-f3810f57e86b">

<br><br>

###### 외부 ip로 포트포워딩
> https://kim519620.tistory.com/entry/WSL-%ED%8F%AC%ED%8A%B8-%ED%8F%AC%EC%9B%8C%EB%94%A9-feat-port-forwarding-TCP%EB%A7%8C-%EC%A7%80%EC%9B%90%ED%95%A8
> https://pickle-link-80b.notion.site/wsl-0c5fcaaa8917403f83e7fd8b8a826db8
> https://velog.io/@momentum96/WSL2-%EC%99%B8%EB%B6%80-%EC%A0%91%EC%86%8D-%EC%84%A4%EC%A0%95


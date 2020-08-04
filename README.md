<h1 align="center"> 👋 AWS EKS Kubernetes Cluster 구성 </h1>
<p>
  <a href="https://sed-gitlab.hanpda.com/jhjeong/test/blob/master/README.md">
    <img src="https://img.shields.io/badge/version-1.0.0-blue.svg?cacheSeconds=2592000" />
  </a>
  <a href="https://sed-gitlab.hanpda.com/jhjeong/test/blob/master/README.md">
    <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" target="_blank" />
  </a>
  <a href="https://github.com/kefranabg/readme-md-generator/graphs/commit-activity">
    <img alt="Maintenance" src="https://img.shields.io/badge/Maintained%3F-yes-green.svg" target="_blank" />
  </a>
</p>

## 개요
> ㅁ Ansible을 사용하여 여러 CloudFormation 템플릿을 관리하는 고 가용성 AWS EKS Kubernetes 클러스터 설정을 보여줍니다.

## 디렉토리 레이아웃
```sh
mzc-eks-cluster/
├── cloudformation # aws cloudformatin 템플릿 디렉토리
│   ├── eks-cluster.yml # eks 클러스터 YAML 파일
│   ├── eks-nodegroup.yml # eks 노드그룹 YAMl 파일
│   └── vpc.yml # ek VPC YAML 파일
├── delete.yml # k8s 어플리케이션 및 eks 리소스 삭제 plybook 파일
├── deploy.yml # k8s 어플리케이션 (wordpress 서비스) 배포 playbook 파일
├── inventory # 작업 할 대상을 정의하는 파일 (여기서는 local)
├── main.yml # eks 리소스 생성하기 위한 plybook 파일
├── README.md 
├── vars # ansible role 구조에서 정적 변수를 정의
│   └── main.yml # aws 셋팅, EKS 클러스터 셋팅, Nodegroup 셋팅, k8s 어플리케이션 셋팅 변수 정의
└── wordpress # WordPress 웹 사이트 (MySQL을 사용하고 영구 저장소에 EBS PV를 사용)를 배포
    ├── mysql-pass.yml # Mysql 인증을 위한 Secret 리소스 YAML 파일
    ├── mysql.yml # Mysql Service, PV, Deployment 리소스 YAML 파일
    └── wordpress.yml # WordPress Service, PVC, Deployment 리소스 YAML 파일
```

## 링크
🤝 [issues page]().

## 작성자
👤 **Jaehwan Jeong**

***


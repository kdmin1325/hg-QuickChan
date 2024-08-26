# 퀵찬 - 시니어를 위한 길 안내 서비스 '부릉'

해커그라운드 해커톤에 참여하는 `퀵찬` 팀의 서비스 `부릉` 입니다.

## 참고 문서

> 아래 두 링크는 해커톤에서 앱을 개발하면서 참고할 만한 문서들입니다. 이 문서들에서 언급한 서비스 이외에도 더 많은 서비스들이 PaaS, SaaS, 서버리스 형태로 제공되니 참고하세요.

- [순한맛](./REFERENCES_BASIC.md)
- [매운맛](./REFERENCES_ADVANCED.md)

## 제품/서비스 소개

<!-- 아래 링크는 지우지 마세요 -->
[제품/서비스 소개 보기](TOPIC.md)
<!-- 위 링크는 지우지 마세요 -->

## 오픈 소스 라이센스

<!-- 아래 링크는 지우지 마세요 -->
[오픈소스 라이센스 보기](./LICENSE)
<!-- 위 링크는 지우지 마세요 -->

## 설치 방법

> **아래 제공하는 설치 방법을 통해 심사위원단이 여러분의 제품/서비스를 실제 Microsoft 애저 클라우드에 배포하고 설치할 수 있어야 합니다. 만약 아래 설치 방법대로 따라해서 배포 및 설치가 되지 않을 경우 본선에 진출할 수 없습니다.**

### 사전 준비 사항
https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-windows?tabs=azure-cli
애저 CLI 설치

```git
az --version
```
이후 설치 버전 확인



```git
git clone https://github.com/Azure-Samples/msdocs-python-flask-webapp-quickstart
```
깃 클론을 통해 로컬에 저장 진행(일반적으로 문서에 있음)

```git
cd $REPOSITORY_ROOT/source_codes/flask
```
백엔드 폴더로 이동


## 시작하기

```git
az login
```
애저 CLI를 통해서 로그인 진행

```
az webapp up --runtime PYTHON:3.9 --sku B1 --logs --resource-group {"자신의 리소스 그룹 이름"} --location KoreaCentral
```
{"자신의 리소스 그룹 이름"} 을 알맞게 변경해주세요.
//이때 속도가 느린 인터넷을 사용하여 접속한다면 오류가 발생할 수 있습니다.

http://<app-name>.azurewebsites.net 에 접속하여 페이지가 나온다면 성공.
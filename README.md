# Model
## Azure-test-250616

## Azure AKS 클러스터 초기 설정 및 Gitpod 연동
- Azure 계정에 로그인하여 AKS 클러스터를 포함한 필수 리소스를 생성했습니다.
- Gitpod 개발 환경에서 Azure CLI 및 Kubectl 설치를 확인하고, Azure SSO를 통해 AKS 클러스터에 접속할 수 있도록 성공적으로 연동했습니다.

![스크린샷 2025-06-16 145400](https://github.com/user-attachments/assets/cbd54516-a217-48e3-9924-8f774d0b659d)
![스크린샷 2025-06-16 145721](https://github.com/user-attachments/assets/f60b1b39-8e34-4b86-a708-4fcbe088dc73)
![스크린샷 2025-06-16 151630](https://github.com/user-attachments/assets/0217613f-c415-40a7-a18f-e6c273ac48e3)
![스크린샷 2025-06-16 153510](https://github.com/user-attachments/assets/f91432a7-e631-49b4-ab99-9446d3bd6e4c)
![스크린샷 2025-06-16 153923](https://github.com/user-attachments/assets/fdf9873d-db51-4edf-83b8-11622029bedf)
![스크린샷 2025-06-16 154131](https://github.com/user-attachments/assets/4788ec59-6c0a-4681-912a-cf8f52e194c7)
![스크린샷 2025-06-16 165006](https://github.com/user-attachments/assets/58a9a771-a3c0-4a82-83d0-10b41b74d105)
![스크린샷 2025-06-16 170247](https://github.com/user-attachments/assets/515d85ff-54e8-4642-8534-7f69080141fc)

## Azure 실행
1. MS 로그인하고, 비밀번호 변경
- 휴대폰 인증이 뜨면 그것도 실행

2. 리소스 만들기
- a071098-rsrcgrp

3. 쿠버네티스 클러스트 만들기
- a071098-aks
- 메모리, 노드 수 설정

4. Gitpod 프로그램 실행
터미널상에서 아래 실행해보면 잘 설치되었는지 확인 가능.
```
az
kubectl
```
5. 재실행시 초기화
```
./init.sh
```
6. Azure Client SSO 설정
```
azure 로그인
az login --use-device-code
1 + Enter
```
7. 쿠버네틱스 로그인
az aks get-credentials --resource-group a071098-rsrcgrp --name a071098-aks

kubectl get all
kubectl get node


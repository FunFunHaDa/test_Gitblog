---
title: "[안드로이드] 액티비티 생명주기"
last_modified_at: 2020-04-07T17:40:00:00+09:00
categories:
  - Android
tags:
  - Android
  - 한국 
toc: true
---

## 액티비티 수명주기
### 수명주기  

상태 | 설명    
--------------       | ---------------
실행(Running)     | 화면 상에 액티비티가 보이면서 실행되어 있는 상태.액티비티 스택의 최상위에 있으며 포커스를 가지고 있음
일시 중지(Paused)  | 사용자에게 보이기는 하지만 다른 액티비티가 위에 있어 포커스를 받지 못하는 상태, 대화상자가 위에 있어 일부러 가려져 있는 경우에 해당함
중지(Stopped)      | 다른 액티비티에 의해 완전히 가려져 보이지 않는 상태

### 수명주기에 따른 상태 변화
![Image](https://user-images.githubusercontent.com/28629625/77538816-b023f700-6ee3-11ea-8f11-1be48deca734.png)

### 자세히
![Image](https://user-images.githubusercontent.com/28629625/77538850-c16d0380-6ee3-11ea-9a5b-cfacb3273230.png)


## MyLifeCycle 프로젝트 생성
![Image](https://user-images.githubusercontent.com/28629625/77538893-d184e300-6ee3-11ea-9334-9381acad6f66.png)

### Button 추가
activity_main.xml --> Button --> text --> "화면 닫기"  
![Image](https://user-images.githubusercontent.com/28629625/77538917-d9dd1e00-6ee3-11ea-81ec-34c7bcc23bfd.png)

MainActivity.java --> 입력  
![Image](https://user-images.githubusercontent.com/28629625/77538955-e8c3d080-6ee3-11ea-86c4-6b91a0338f7a.png)

### Run
![Image](https://user-images.githubusercontent.com/28629625/77538981-f2e5cf00-6ee3-11ea-869c-0036ce57cf6e.png)


### onPause() 상태에서 필요한 데이터 저장, sharedpreferences
MaintActivity --> 입력  
![image](https://user-images.githubusercontent.com/28629625/77539022-03964500-6ee4-11ea-9b04-b53ea01445c6.png)


### 화면 닫기 이후, 재실행 
![image](https://user-images.githubusercontent.com/28629625/77539198-4fe18500-6ee4-11ea-9fd5-5f4866eef406.png)

### 데이터의 복구 
수명주기  메소드가 자동 호출되도록 만든 이유는 사용자가 입력했던 데이터를 복구하거나 상태 정보를 복구할 수 있도록 만들기 위해서입니다


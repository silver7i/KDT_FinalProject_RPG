
# PuffPebble (ref - 롱빈터, 메이플)  
몬스터를 처치하며 레벨을 올리며 성장하는 게임

#### 프로젝트 기간
- 2024.(05.13 ~ 06.28) (1.5개월) / 2인

#### 기술 스택
- C++, UE5 (Blueprint)

#### 담당 역할
- **본인** : 몬스터와 관련된 기능 및 UI, 맵 디자인
- **팀원** : 플레이어 캐릭터와 관련된 기능 구현 및 UI, 전체적인 UI

---
---

``` 몬스터는 Pawn Class 로 구현 ```

#### 일반 몬스터       
      
1. 타겟 감지  
   - 일정 거리 내에 있는 타겟을 감지하면 공격을 위해 움직임  
   - 타겟 감지 전후 속도를 다르게 설정해 자연스러운 이동을 구현함 
   - 애니메이션이 속도 변화에 맞춰 자연스럽게 전환되도록 설정  
<img src="https://github.com/user-attachments/assets/a4df59e2-15d8-42c5-9112-cce014ecf8af" width="45%" height="35%" alt="Target Detect.gif"></img>

   
2. 피격시 효과  
   - 일정 데미지 이상 피격 시 공격 방향에 따른 넉백 효과를 적용  
   - 피해량과 몬스터 상태를 UI로 표시  
<img src="https://github.com/user-attachments/assets/ef28b3a0-31e9-479e-8de9-414c0569c663" width="35%" height="25%" alt="Death.gif"></img>


4. 공격한 타겟 감지  
   - 감지 반경에 타겟이 없더라도 피격 시 공격 대상을 추적  
   - 일정 시간이 지나도 감지반경 안에 들어오지 않으면 타겟팅이 중지되도록 설정함  
<img src="https://github.com/user-attachments/assets/06c614d6-fcde-411d-a1b9-469a509d6964" width="45%" height="35%" alt="타겟 감지2.gif"></img>


#### 보스 몬스터

1. 보스 스킬
   ```
   보스는 HP 비율에 따라 스킬 개수와 발현 시간 간격을 다르게 구현함
   1) HP 70% 이상일 때 스킬 2개, 스킬 재생 간격 10초
   2) HP 70% 이상일 때 스킬 3개, 스킬 재생 간격 5초
   3) HP 70% 이상일 때 스킬 4개, 스킬 재생 간격 0초
   ```  
<img src="https://github.com/user-attachments/assets/6797ce27-d36d-431b-bd12-70bc3dbb1a0e" width="45%" height="35%" alt="보스 스킬1&2.gif"></img>
<img src="https://github.com/user-attachments/assets/9618dafa-967d-45f4-b016-31c4ac1a15cd" width="45%" height="35%" alt="보스 스킬3.gif"></img>
 

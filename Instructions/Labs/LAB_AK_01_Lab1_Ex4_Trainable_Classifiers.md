﻿# 연습 4 - 학습 가능한 분류자 관리

Contoso Ltd. 테넌트에는 "영업 및 마케팅" SharePoint 사이트 모음이 있습니다. 앞으로는 이 사이트 모음을 사용하여 다양한 재무 관련 문서와 보고서를 저장할 예정입니다. 이러한 문서의 특성을 고려해 이러한 파일을 인식하여 레이블을 지정하는 학습 가능한 분류자를 만들어야 합니다. 이 연습에서는 이러한 용도로 사용자 지정 학습 가능한 분류자를 활성화하고 새 분류자를 만듭니다.

**중요!**: 테넌트에서 학습 가능한 분류자를 활성화한 후 사용자 지정 학습 가능한 분류자를 만들 수 있을 때까지는 **7~14일**이 걸립니다. 전체 활성화 프로세스가 완료될 때까지는 새 학습 가능한 분류자 만들기 단추를 사용할 수 없습니다.  그러므로 **지금은 작업 1만 수행**할 수 있으며 나중에 테넌트 내에서 학습 가능한 분류자를 사용할 수 있게 될 때까지 기다려야 합니다.  이러한 랩 지침은 온라인에서 제공됩니다. 학습 가능한 분류자를 새로 만들려면 테넌트가 계속 활성 상태여야 합니다.

### 작업 1 - 학습 가능한 분류자 활성화

사용자 지정 학습 가능한 분류자를 만들려면 테넌트에서 해당 기능을 활성화해야 합니다. 이 기능을 활성화하려면 전역 관리자 권한이 필요합니다. 따라서 Joni Sherman 계정에서 로그아웃한 다음 MOD 관리자 계정을 사용하여 기능을 먼저 활성화합니다.

1. 클라이언트 1 VM(LON-CL1)에는 **lon-cl1\admin** 계정으로, Microsoft 365에는 **Joni Sherman**으로 로그인되어 있는 상태여야 합니다. 

2. 오른쪽 위의 사용자 이미지를 선택한 다음 **로그아웃**을 선택하여 Joni Sherman 계정에서 로그아웃합니다.

3. 브라우저 창을 닫고 새 브라우저 창을 엽니다.

4. **Microsoft Edge**에서 **https://compliance.microsoft.com** 으로 이동합니다.

5. **계정 선택** 페이지가 표시되면 **다른 계정 사용**을 선택하고 **MOD 관리자**로 로그인합니다. 로그인 ID로는 admin@WWLxZZZZZZ.onmicrosoft.com을 사용합니다(여기서 ZZZZZZ는 랩 호스팅 공급자가 제공한 고유 테넌트 ID임).  관리자의 암호는 랩 호스팅 공급자가 제공합니다.

6. 왼쪽 탐색 창에서 **데이터 분류**로 이동합니다.

7. 위쪽 창에서 **학습 가능한 분류자**를 선택합니다.

8. **학습 가능한 분류자 시작하기** 창에서 **검색 프로세스 시작**을 선택합니다.

9. 브라우저 창을 새로 고칩니다.

10. 다음 메시지가 표시된 창 위쪽의 배너를 확인합니다. **학습 가능한 분류자를 만들기 위해 사용자를 설정하려면 현재 사용자의 콘텐츠 위치를 검색하여 조직에 있는 콘텐츠 유형을 파악하는 데 도움이 되는 분석을 생성합니다. 이 프로세스를 완료하는 데 7~14일이 걸립니다.**

11. 클라이언트는 열어 둡니다.

테넌트에서 학습 가능한 분류자를 활성화했습니다. 이제 **학습 가능한 분류자 만들기** 단추를 사용할 수 있게 될 때까지 7~14일 동안 기다려야 합니다.  강의용 설정을 사용 중이어서 학습 가능한 분류자를 만들 수 있을 때까지 7~14일 동안 기다렸다가 처리를 완료할 시간이 없다면, 나중에 학습 가능한 분류자 처리 완료 시 제공된 테넌트에 로그인하여 이 연습의 나머지 작업을 수행할 수 있습니다.  해당 시점에도 테넌트는 활성 상태여야 합니다.

### 작업 2 - 학습 가능한 분류자 만들기

학습 가능한 분류자를 활성화하고 나면 **학습 가능한 분류자 만들기** 단추를 사용할 수 있게 되므로 새 사용자 지정 분류자를 만들 수 있습니다. 이 작업에서는 Joni가 새 학습 가능한 분류자를 만들고, Contoso Ltd.에서 만들어 저장하는 일반적인 데이터 식별용으로 여러 SharePoint 사이트를 선택합니다.

1. 클라이언트 1 VM(LON-CL1)에는 **lon-cl1\admin** 계정으로, Microsoft 365에는 **MOD 관리자**로 로그인되어 있는 상태여야 합니다. 

2. 오른쪽 위의 MA를 선택한 다음 **로그아웃**을 선택하여 MOD 관리자 계정에서 로그아웃합니다.

3. 브라우저 창을 닫고 새 브라우저 창을 엽니다.

4. **Microsoft Edge**에서 **https://compliance.microsoft.com** 으로 이동합니다.

5. **계정 선택** 페이지가 표시되면 **다른 계정 사용**을 선택하고 **Joni Sherman**으로 로그인합니다. 로그인 ID로는 JoniS@WWLxZZZZZZ.onmicrosoft.com을 사용합니다(여기서 ZZZZZZ는 랩 호스팅 공급자가 제공한 고유 테넌트 ID임).  Joni의 암호는 랩 호스팅 공급자가 제공합니다.

6. 왼쪽 탐색 창에서 **데이터 분류**로 이동합니다.

7. 위쪽 창에서 **학습 가능한 분류자**를 선택합니다.

8. **+ 학습 가능한 분류자 만들기**를 선택하여 새 분류자를 만듭니다.

9. **학습 가능한 분류자 이름 지정 및 설명** 페이지에서 다음 정보를 입력합니다.

    - **이름**: Contoso 회사 데이터
    - **설명**: Contoso Ltd.에서 생성하여 저장하는 회사 데이터용 학습 가능한 분류자

10. **다음**을 선택합니다.

11. **사이트 선택**을 선택하여 오른쪽 창을 엽니다.

12. 다음 SharePoint 사이트를 선택합니다.

    - **커뮤니케이션 사이트**
    - **Contoso 뉴스**
    - **Contoso 웹 1**
    - **브랜드**
    - **디지털 이니셔티브 홍보**
    - **Contoso 업무**
    - **영업 및 마케팅**
    - **Contoso 방문 페이지**
    - **Mark 8 프로젝트 팀**
    - **HR**
    - **운영**
    - **소매**
    - **PointPublishing 허브 사이트**
    - **팀 사이트**
    - **경영진**
    - **커뮤니티**
    - **Contoso의 사회 공헌**
    - **Contoso의 복리 후생**
    - **Contoso의 학습 환경**
    - **캠페인 - 이벤트**

13. 선택한 사이트가 목록에 표시될 때까지 기다렸다가 **다음**을 선택합니다.

14. 설정을 검토하고 **학습 가능한 분류자 만들기**를 선택합니다.

15. **학습 가능한 분류자가 생성되었습니다.** 메시지가 표시되면 **완료**를 선택합니다.

16. 이제 1~24시간 동안 기다렸다가 계속 진행해야 합니다. 브라우저는 열어 둡니다.

선택한 SharePoint 사이트의 문서와 파일 분석이 진행됩니다. 이 분석에는 최대 24시간이 걸릴 수 있습니다.

### 작업 3 - 학습 가능한 분류자 게시 
새 학습 가능한 분류자를 만든 후 문서 및 파일 초기 분석이 완료되면 수동 학습 프로세스를 수행해야 합니다. 이 작업에서 Joni는 분류자의 정확도를 게시할 수 있는 수준으로 높이기 위해 분류자 보정을 시작합니다.

1. 클라이언트 1 VM(LON-CL1)에는 **lon-cl1\admin** 계정으로, Microsoft 365에는 **Joni Sherman**으로 로그인되어 있는 상태여야 합니다. 

2. 브라우저 창에는 Microsoft 365 규정 준수 센터 **데이터 분류**에서 **학습 가능한 분류자** 탭이 선택되어 있어야 합니다.

3.  이름이 **Contoso 회사 데이터**이고 유형이 **사용자 지정**인 학습 가능한 분류자를 선택하여 세부 설정을 엽니다.

4. 오른쪽 **세부 정보** 탭을 검토합니다. 구체적으로는 분류자의 원본 사이트, 처리한 항목 수, **상태** 등을 검토해야 합니다. 분류자의 상태는 **테스트 항목 필요**여야 합니다.

5. 분류자 학습용 항목을 추가하려면 **테스트할 항목 추가**를 선택하여 오른쪽 선택 창을 엽니다.

6. **테스트할 항목이 포함된 사이트 선택** 창에서 **+ 사이트 선택**을 선택합니다.

7. 다음 SharePoint 사이트를 선택합니다.

    - **커뮤니케이션 사이트**
    - **Contoso 뉴스**
    - **Contoso 웹 1**
    - **브랜드**
    - **디지털 이니셔티브 홍보**
    - **Contoso 업무**
    - **영업 및 마케팅**
    - **Contoso 방문 페이지**
    - **Mark 8 프로젝트 팀**
    - **HR**
    - **운영**
    - **소매**
    - **PointPublishing 허브 사이트**
    - **팀 사이트**
    - **경영진**
    - **커뮤니티**
    - **Contoso의 사회 공헌**
    - **Contoso의 복리 후생**
    - **Contoso의 학습 환경**
    - **캠페인 - 이벤트**

8. **추가**를 선택합니다.

8. 사이트가 목록에 표시될 때까지 기다렸다가 **추가**를 선택합니다.

9. **개요** 섹션이 업데이트되면 창 위쪽에 새 탭이 표시됩니다.

10. 위쪽 창에서 **검토할 테스트 완료 항목**을 선택합니다.

11. 첫 번째 결과를 검토할 수 있게 될 때까지 15~30분 정도 걸립니다. 목록에 파일이 표시되지 않으면 데이터가 제공될 때까지 브라우저 창을 새로 고칩니다.

12. 목록의 첫 번째 파일 이름을 선택하여 미리 보기 창을 엽니다.

13. **예측** 행의 값이 **일치**이면 해당 파일이 분류자와 일치하는 항목으로 식별된 것입니다. 미리 보기 창 아래에는 **이 항목은 이 분류자와 "일치함"(으)로 예상합니다.** 라는 메시지가 표시됩니다. **일치**를 선택하여 자동 분류를 승인합니다.

14. **예측** 행의 값이 **짝이 아님**이면 해당 파일이 분류자와 일치하는 항목으로 식별되지 않은 것입니다. 미리 보기 창 아래에는 **이 항목은 이 분류자와 "일치하지 않음"(으)로 예상합니다.** 라는 메시지가 표시됩니다. **짝이 아님**을 선택하여 자동 분류를 승인합니다.

15. 목록의 모든 항목에서 이 절차를 진행하여 자동 분류를 승인합니다. 모든 항목을 검토한 후 위쪽 창에서 **개요**를 선택하고 **검토할 테스트 완료 항목**을 다시 선택하여 검토할 다음 항목 집합을 로드합니다.

16. 항목 30개를 검토할 때마다 **자동 재학습이 수행되었습니다.** 창이 표시됩니다. **확인**을 클릭하고 검토할 항목이 더 이상 없을 때까지 이전 단계를 진행합니다.

17. 항목을 충분히 검토하고 나면 오른쪽 위의 **게시** 단추를 사용할 수 있게 됩니다. 사용 가능해지는 즉시 해당 단추를 선택합니다.

18. **분류자 게시** 창에서 **예**를 선택하여 분류자를 게시합니다.

19. **학습 가능한 분류자가 게시되었습니다.** 메시지가 포함된 오른쪽 창이 표시되면 학습 가능한 분류자가 게시된 것입니다.

20. 오른쪽 위의 **X**를 눌러 오른쪽 창을 닫습니다.

21. 주 사이트로 돌아오면 사용자 지정 분류자가 **게시됨**으로 이동되었으며 **상태**가 **사용 준비 완료**로 변경되었음을 확인할 수 있습니다.

22. 브라우저 창은 열어 둡니다.

Contoso Ltd.의 기존 SharePoint 사이트에 저장된 파일과 일치하는 사용자 지정 학습 가능한 분류자를 작성하여 학습시키고 게시했습니다.

# 연습 5 계속 진행 
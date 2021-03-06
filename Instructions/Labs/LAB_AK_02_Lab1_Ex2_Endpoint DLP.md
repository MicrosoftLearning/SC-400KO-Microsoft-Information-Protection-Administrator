# 랩 2 - 연습 2 - 엔드포인트 DLP 관리

Contoso Ltd.에 새로 입사한 준수 관리자인 Joni Sherman이 회사 Microsoft 365 테넌트에서 데이터 손실 방지 기능을 구성하는 작업을 맡게 되었습니다. Contoso Ltd.는 미국의 운전학원입니다. 학원에 등록하는 중요한 고객 정보가 조직 외부로 유출되지 않도록 해야 합니다. 따라서 Microsoft 365 DLP 정책을 구현하는 동시에 조직 내의 디바이스에도 이 보호 기능을 확대 적용하기로 했습니다.

### 작업 1 - 디바이스 온보딩 설정

이 작업에서는 조직에서 디바이스 온보딩 기능을 설정합니다. 

1. 클라이언트 1 VM(LON-CL1)에는 **lon-cl1\admin** 계정으로, Microsoft 365에는 **Joni Sherman** JoniS@WWLxZZZZZZ.onmicrosoft.com(여기서 ZZZZZZ는 랩 호스팅 공급자가 제공한 고유 테넌트 ID임)으로 로그인되어 있는 상태여야 합니다.  Joni의 암호는 랩 호스팅 공급자가 제공합니다.

2. 그리고 **Microsoft Edge**에는 Microsoft 365 규정 준수 포털 탭이 계속 열려 있어야 합니다. 해당 탭이 열려 있으면 탭을 선택하고 다음 단계를 진행합니다. 해당 탭을 닫았다면 새 탭에서 **https://compliance.microsoft.com** 으로 이동합니다.

3. **Microsoft 365 규정 준수** 포털의 왼쪽 탐색 창에서 **설정**을 선택하고 **디바이스 온보딩**을 선택합니다.

4. **디바이스 온보딩 켜기**를 선택합니다.

5. **디바이스 온보딩 켜기** 대화 상자에서 **확인**을 선택하여 디바이스 온보딩을 적용합니다.

6. **디바이스 모니터링 켜기** 대화 상자에서 **확인**을 선택하여 디바이스 모니터링을 적용합니다.

이제 디바이스 온보딩이 사용하도록 설정되었으므로 엔드포인트 DLP 정책을 사용하여 보호할 Windows 10 디바이스 온보딩을 시작할 수 있습니다. 이 기능을 사용하도록 설정하는 프로세스는 최대 30분 이상이 걸릴 수 있으므로 다음 작업으로 진행해도 됩니다.

### 작업 2 - 엔드포인트 DLP에 디바이스 온보딩

이 작업에서는 엔드포인트 DLP 정책을 통해 보호할 수 있도록 로컬 스크립트 옵션을 사용하여 Windows 10 디바이스를 온보딩합니다.

1. **lon-cl1\admin** 계정으로 클라이언트 1 VM(LON-CL1)에 로그인합니다.

2. **Microsoft Edge**에서 **https://compliance.microsoft.com** 으로 이동한 다음 **Joni Sherman**으로 Microsoft 365에 로그인해야 합니다.

3. **Microsoft 365 규정 준수** 포털의 왼쪽 탐색 창에서 **설정**을 선택하고 **디바이스 온보딩**을 선택합니다.

4. **디바이스 온보딩** 페이지의 왼쪽 탐색 창에서 **온보딩**을 선택합니다.

5. **배포 방법** 드롭다운 메뉴에서 로컬 스크립트(최대 컴퓨터 10대에 사용 가능)를 선택하고 패키지 다운로드를 선택합니다.

6. 다운로드 대화 상자에서 **저장**, **폴더 열기**를 차례로 선택합니다.

7. LON-CL1의 **바탕 화면**에 ZIP 파일의 압축을 풉니다. **DeviceComplianceLocalOnboardingScript.cmd** 스크립트가 표시됩니다.

8. 바탕 화면에서 방금 압축을 푼 **DeviceComplianceLocalOnboardingScript.cmd** 파일을 마우스 오른쪽 단추로 클릭하고 **관리자 권한으로 실행**을 선택합니다.  Windows SmartScreen 경고 상자가 표시될 수 있습니다. 이 경우 **추가 정보**를 선택하고 **실행**을 선택합니다.  사용자 계정 컨트롤 창이 표시되면 **예**를 선택하여 이 스크립트가 PC를 변경할 수 있도록 허용합니다.

9. **명령 프롬프트** 화면에서 **Y**를 입력하여 실행을 확인하고 Enter 키를 누릅니다.

10. 스크립트 실행이 완료되면 **아무 키나 눌러 계속 진행**합니다.  온보딩을 완료하려면 1분 정도 걸릴 수 있습니다.

11. 시작 메뉴를 열고 **회사 또는 학교 액세스**를 선택합니다.

12. **회사 또는 학교 액세스** 창에서 **+ 연결**을 선택합니다.

13. **회사 또는 학교 계정 설정** 대화 상자에서 **Azure Active Directory에 이 디바이스 가입** 링크를 선택하고 **Joni Sherman**으로 로그인합니다. 로그인 ID로는 JoniS@WWLxZZZZZZ.onmicrosoft.com을 사용합니다(여기서 ZZZZZZ는 랩 호스팅 공급자가 제공한 고유 테넌트 ID임).  Joni의 암호는 랩 호스팅 공급자가 제공합니다.

14. **조직 확인** 대화 상자에서 테넌트 URL을 검토하고 **가입**을 선택합니다.  디바이스 가입이 실패하면 Azure AD 구성 가입 설정의 문제를 해결해야 합니다. 디바이스가 가입 가능하도록 설정하려면 다음 단계를 수행합니다.
        1. 새 브라우저 탭을 열고 Azure Portal https://portal.azure.com으로 이동합니다.
        1. **MOD 관리자** admin@WWLxZZZZZZ.onmicrosoft.com으로 로그인합니다.
        1. **Azure Active Directory 관리**를 선택합니다.
        1. **디바이스**를 선택합니다.
        1. **디바이스 설정**을 선택합니다.
        1. **사용자당 최대 디바이스 수**가 표시될 때까지 아래로 스크롤하여 값을 **20(권장)** 으로 변경합니다.
        1. 설정을 업데이트한 후 디바이스 연결을 다시 시도해 봅니다.

15. 디바이스가 연결되면 **완료**를 선택합니다.

16. 클라이언트 1 VM(LON-CL1)을 다시 시작합니다.

디바이스를 온보딩하고 엔드포인트 DLP 정책을 사용하여 보호할 수 있도록 Azure AD에 가입시켰습니다.

### 작업 3 - 엔드포인트 DLP 정책 만들기

이 작업에서는 조직의 Windows 10 디바이스에 있는 중요한 데이터를 보호하는 데 사용할 데이터 손실 방지 정책을 규정 준수 센터에서 만듭니다. 여기서 만들 DLP 정책은 사용자가 신용 카드 정보를 포함하는 문서의 콘텐츠를 복사하려고 하면 해당 작업을 차단합니다.

1. lon-cl1\admin 계정으로 클라이언트 1 VM(LON-CL1)에 로그온합니다.

2. Microsoft Edge에서 https://compliance.microsoft.com으로 이동합니다.

3. 로그인 창이 표시되면 JoniS@WWLxZZZZZZ.onmicrosoft.com으로 로그인합니다(여기서 ZZZZZZ는 랩 호스팅 공급자가 제공한 고유 테넌트 ID임). Joni의 암호는 랩 호스팅 공급자가 제공합니다. 힌트: 암호는 앞부분에서 사용한 MOD 관리자와 동일할 것입니다. 

4. **Microsoft 365 규정 준수** 포털의 왼쪽 탐색 창에서 **정책**을 선택하고 **데이터** 아래에서 **데이터 손실 방지**를 선택합니다.

5. **데이터 손실 방지** 창에서 **정책** 탭을 선택하고 **+정책 만들기**를 선택하여 새 데이터 손실 방지 정책 만들기 마법사를 시작합니다.

6. **서식 파일로 시작하거나 사용자 지정 정책 만들기** 페이지에서 왼쪽 창의 **사용자 지정**을 선택하고 가운데 창에서는 **사용자 지정 정책**을 선택해야 합니다. 하지만 이 두 옵션은 이미 기본적으로 선택되어 있으므로(선택되어 있지 않으면 지금 선택) **다음**을 선택합니다.

7. **DLP 정책 이름 지정** 페이지의 **이름** 필드에 *신용 카드 엔드포인트 DLP 정책*을 입력하고 **설명** 필드에는 *엔드포인트에서 신용 카드 번호를 공유할 수 없도록 보호하는 정책입니다.* 를 입력합니다. **다음**을 선택합니다.

8. **정책을 적용할 위치 선택** 페이지에서 **디바이스** 옵션만 선택하고 **다음**을 선택합니다.

9. **정책 설정 정의** 페이지의 **고급 DLP 규칙 만들기 또는 사용자 지정** 옵션을 선택해야 합니다. 이 옵션도 기본적으로 선택되어 있습니다. **다음**을 선택합니다.

10. **고급 DLP 규칙 사용자 지정** 페이지에서 **+ 규칙 만들기**를 선택합니다.

11. **규칙 만들기** 페이지의 **이름** 필드에 *엔드포인트 신용 카드 정보*를 입력합니다.

12. **+ 조건 추가**를 선택하고 드롭다운 메뉴에서 **다음이 포함된 콘텐츠**를 선택합니다.

13. **규칙 만들기** 페이지의 새 **다음이 포함된 콘텐츠** 영역에서 **추가**를 선택하고 드롭다운 메뉴에서 **중요한 정보 유형**을 선택합니다.

14. **중요한 정보 유형** 페이지에서 **신용 카드 번호**를 선택하고 **추가**를 선택합니다.

15. **규칙 만들기** 페이지에서 **+ 작업 추가**를 선택하고 **Windows 디바이스의 활동 감사 또는 제한**을 선택합니다.

16. **클립보드에 복사**를 제외한 모든 체크박스의 선택을 취소합니다.

17. **클립보드에 복사** 뒤에 있는 드롭다운 메뉴에서 **차단**을 선택합니다.

18. **규칙 만들기** 페이지의 **사용자 알림** 섹션에서 스위치를 선택하여 **켜기** 위치로 이동합니다.

19. **인시던트 보고서** 섹션의 **관리 경고 및 보고서에서 이 심각도 사용** 드롭다운에서 **낮음**을 선택합니다.

20. **인시던트 보고서** 섹션에서 **규칙이 일치하는 경우 관리자에게 알림을 보냅니다.** 스위치를 선택하여 **켜기** 위치로 이동하고 옵션을 검토합니다. 기본 설정을 적용하는 경우 정책을 만드는 사용자에게 알림이 표시됩니다.

21. **저장**, **다음**을 차례로 선택합니다.

22. **정책 테스트 또는 켜기** 페이지에서 **예, 지금 켜겠습니다.** 를 선택합니다.

23. **다음**을 선택하고 정책 구성을 검토합니다.

24. **제출**을 선택하여 정책을 만듭니다.

25. 정책이 만들어지면 **완료**를 선택합니다.

DLP 정책을 활성화했습니다. 이 정책은 신용 카드 정보가 포함된 파일의 콘텐츠 복사 시도가 검색되면 해당 시도를 차단하고 사용자에게 알림을 표시합니다.

### 작업 4 - 엔드포인트 DLP 설정 구성

이 작업에서는 Windows 10 디바이스의 한 폴더에 대해 파일 경로 제외를 구성하여 앞에서 만든 엔드포인트 DLP 정책이 해당 폴더의 콘텐츠를 모니터링하지 않음을 확인합니다.

1. 클라이언트 1 VM(LON-CL1)에는 **lon-cl1\admin** 계정으로, Microsoft 365에는 **Joni Sherman**으로 로그인되어 있는 상태여야 합니다. 

2. 그리고 **Microsoft Edge**에는 Microsoft 365 규정 준수 포털 탭이 계속 열려 있어야 합니다. 해당 탭이 열려 있으면 탭을 선택하고 다음 단계를 진행합니다. 해당 탭을 닫았다면 새 탭에서 **https://compliance.microsoft.com** 으로 이동합니다.

3. **Microsoft 365 규정 준수** 포털의 왼쪽 탐색 창에서 **정책**을 선택하고 **데이터** 아래에서 **데이터 손실 방지**를 선택합니다.

4. **데이터 손실 방지** 창에서 **엔드포인트 DLP 설정** 탭을 선택합니다.

5. **엔드포인트 DLP 설** 탭에서 **파일 경로 제외** 영역을 확장하고 **+ 파일 경로 제외 추가**를 선택합니다.

6. **제외할 경로 입력** 필드에 *C:\FilePathExclusionTest*를 입력하고 **+** 를 선택합니다.

7. **추가**를 선택합니다.

엔드포인트 DLP 정책에 대한 일반 예외를 구성했습니다. 앞으로 만드는 모든 정책에서는 여기서 구성한 폴더의 콘텐츠가 무시됩니다.

# 랩 2 - 연습 3로 넘어가세요. 

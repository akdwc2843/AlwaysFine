![header](https://user-images.githubusercontent.com/75381985/219609891-932a76c6-b85d-44d2-b5a9-82e5b0841ad2.jpg)

## AlwaysFine
**AlwaysFine**은 미세먼지와 초미세먼지 수치를 바탕 화면에 표시하는 [Rainmeter](https://www.rainmeter.net) 스킨입니다.

2022년 하반기, 학급에서 미세먼지 수치를 매일 칠판에 기록하는 역할을 담당하게 되었는데, 조금 더 편하게 할 수 있도록 개발했습니다. 대한민국 내 모든 측정소를 지원하고 WHO 기준을 일부 수정한 자체적인 기준을 사용합니다.

## 사용 방법
AlwaysFine은 Windows 10, 11(권장)에서 작동하며, 스킨을 사용하려면 API 키를 입력해야 합니다. [이곳에서](https://www.data.go.kr/data/15073861/openapi.do) API 키를 발급받고, 스킨이 위치한 폴더 내에 'servicekey.inc' 파일을 생성합니다.
<pre>
[Variables]
serviceKey=(SERVICEKEY)
</pre>
이후 (SERVICEKEY)에 **"인코딩" 된 API 키**를 입력하고 저장한 뒤, Rainmeter를 재시작하세요.

## 구동 모습
![1](https://github.com/bunubbv/AlwaysFine/assets/75381985/2588eb52-7bd0-4e85-b61c-98d0ca105136)

스킨 로드 시 미세먼지, 초미세먼지 수치 및 등급을 확인할 수 있습니다. 제물포고등학교와 가장 가까운 송현 측정소가 기본값입니다. 등급은 6단계를 사용하며, 좋음, 양호, 보통, 나쁨, 매우 나쁨, 최악으로 나누어집니다.

![2](https://github.com/bunubbv/AlwaysFine/assets/75381985/907e3808-9286-4f72-93f5-313e8f2152a5)

미세먼지와 초미세먼지 수치에 마우스를 올리면 현재 등급의 범위와 행동 지침을 볼 수 있습니다.

![3](https://github.com/bunubbv/AlwaysFine/assets/75381985/eaa03fd9-dd29-4b11-8889-72fb4584c125)

설정 버튼을 누른 모습입니다. 아무 곳이나 눌러 닫을 수 있으며, 입력 창에 측정소를 입력하고 Enter를 눌러 측정소를 변경할 수 있습니다. 변경한 측정소는 자동 업데이트 전까치 유지되고, 측정소 목록은 위 "측정소 목록" 버튼을 눌러 확인할 수 있습니다.

오른쪽에서 스킨의 버전을 확인할 수 있으며, "깃허브 링크"를 누르면 현재 페이지로 연결됩니다.

## 라이선스
AlwaysFine은 GNU Lesser General Public License v2.1 라이선스로 배포됩니다. 자세한 내용은 [LICENSE](/LICENSE)를 참조하세요.

## 업데이트
* 과거 내역은 별도로 기록하지 않았습니다.
* 2023-05-08 4.0.3
    * 송림 측정소 가동 중단으로 송현 측정소로 변경
* 2023-05-11 4.0.4
    * 업데이트 과정 중 생성되는 다운로드 폴더 삭제
* 2023-05-12 4.0.5
    * 업데이트 스크립트를 인라인으로 실행하여 속도 향상, 업데이트 이후 무한 루프 발생하는 버그 수정
    * 폰트 기본 탑재 및 설치 후 스킨이 자동으로 로드되지 않는 버그 수정
* 2023-08-11 5.0.0
    * 스킨 리팩토링 (불필요한 코드, 변수 정리 및 최적화, 약 Ln 600 > 400)
    * 업데이트 구조 변경으로 안정성 향상
        * 파일 다운로드 구조 변경
        * 파일 무결성 검증 진행
        * 호환성 문제로 요구 버전 윈도우 10으로 상향
        * 오류 방지를 위해 다시 시작 시 업데이트 반영
    * 스킨 디자인 및 폰트 변경
    * 변경한 측정소 정보가 저장되도록 변경
    * 스킨 로드 시 레이아웃 및 설정 자동 적용
    * 오픈 소스로 스킨 배포
    * 기존 8단계 등급에서 7단계로 변경 (심각 삭제)
* 2023-08-12 5.1.0
    * 업데이트 스크립트 버그 수정
* 2023-08-12 5.1.1
    * 레거시 스킨의 호환을 위해 버전 유지
* 2023-08-12 5.1.2
    * 업데이트 스크립트 버그 수정
    * 미세먼지 측정 시간이 잘못 나오는 버그 수정
* 2023-08-12 5.1.3
    * 버전 정보가 잘못 나오는 버그 수정
    * 버전 로드 실패 시 오류 메시지 출력
* 2023-08-14 5.2.0
    * 더 효율적인 구조를 적용하여 불필요한 함수, 변수 정리
    * 코드 리팩토링, 최적화 진행
* 2023-08-15 5.3.0
    * 코드 리팩토링, 최적화 진행
        * 기능이 중복되는 함수 통합
        * 불필요한 변수 삭제
        * 함수, 변수명 정리
        * 데이터 갱신 주기 처리 구조 변경
        * 그 외 유지보수를 위한 구조 변경
        * 불필요한 속성값을 제거하여 최적화
    * 가독성을 위해 고정폭 폰트(Pretendard GOV)로 변경
    * 미세먼지 등급의 글자 수가 다른 경우 간격을 조정하여 가독성 향상
    * 측정소 한 곳이 점검 중이어도 말풍선에 다른 측정소 정보가 나오게 변경
    * 인터넷 문제 혹은 잘못된 측정소 입력 시 상황에 따라 적절한 문구가 나오게 변경
    * 설정 창 페이드 인, 아웃 효과 적용
    * 설정 창의 배경이 실시간으로 변경되지 않던 문제 해결
    * 기존 7단계에서 매우 좋음 단계 삭제
* 2023-08-16 5.4.0
    * 코드 리팩토링, 최적화 진행
        * Windows 10 1909 이전 버전에서 업데이트 시 오류가 발생하는 문제 해결
        * 설정 창에서 입력한 내용이 나오지 않는 문제 해결
        * 업데이트를 Lua가 아닌 내부에서 처리하게 변경
        * 함수, 변수명 정리
    * 미세먼지 수치의 글자 수가 다른 경우 간격을 조정하여 가독성 향상
    * 설정 버튼 토글 기능 추가, 깜빡임 현상 해결
* 2023-08-28 5.4.1
    * 깃허브 링크 변경
    * 부자연스러운 문구 수정
    * 신뢰할 수 없는 측정값을 표시하지 않도록 변경
* 2023-08-30 5.4.2
    * Windows 10 1904에서 업데이트 중 파일이 손상되는 문제 해결
    * 업데이트 이후 스킨을 자동으로 다시 로드
    * 업데이트 코드를 분리하여 스킨 안정성 향상
* 2023-08-30 5.4.3
    * 미세먼지 정보가 갱신되지 않는 문제 해결
    * 코드 구조 개선 및 최적화

## 그 외
* Rainmeter는 HiDPI를 지원하지 않아 시인성 문제가 발생할 수 있습니다. 이를 해결하려면 Rainmeter 폴더(Program Files/Rainmeter)에서 "Rainmeter.exe"를 우클릭한 후, "속성", "호환성", "높은 DPI 설정 변경"에서 "높은 DPI 조정 동작을 재정의합니다."를 활성화하세요.
* [레거시 스킨 \(4.x.x) 보기](https://github.com/bunubbv/alwaysfine/tree/08fc0554353d3b64ec0ebb01d77568ae9ac6dd05)
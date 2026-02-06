1. 주요 개념 비교
StatefulWidget (위젯 중심 상태 관리)
StatefulWidget은 Flutter의 기본 내장 위젯으로, UI(View)와 상태(State)가 하나로 결합된 형태입니다.

통합형 구조: 특정 위젯 내부에서 변수를 선언하고 setState()를 호출하여 화면을 갱신합니다.

제한된 범위: 주로 해당 위젯 내부에 국한된 UI 상태(예: 로딩 애니메이션, 탭 인덱스 등)를 관리할 때 사용됩니다.

강한 결합: 비즈니스 로직과 UI 표현 코드가 한 클래스에 섞이기 쉽습니다.

MVVM (아키텍처 패턴)
MVVM은 데이터(Model), UI(View), 로직(ViewModel)을 엄격히 분리하는 구조적 설계 패턴입니다.

분리된 구조: UI는 오직 ViewModel을 관찰(Observe)하며, 데이터가 변경될 때만 수동적으로 반응합니다.

독립성: ViewModel은 UI(Flutter 위젯)의 존재를 모릅니다. 따라서 UI 없이도 로직 테스트가 가능합니다.

중재자 역할: ViewModel이 Model의 데이터를 가공하여 View가 사용하기 좋은 형태로 제공합니다.

## StatefulWidget vs MVVM 비교

| 구분 | StatefulWidget | MVVM (ViewModel) |
| :--- | :--- | :--- |
| **핵심 목적** | 위젯의 생명주기와 UI 상태 관리 | 관심사 분리 및 비즈니스 로직의 모듈화 |
| **데이터 흐름** | 내부 변수 변경 후 `setState()` 호출 | 데이터 스트림(Provider, Bloc, Signal 등) 구독 |
| **테스트 용이성** | UI 테스트(Widget Test) 위주 | 로직 단위 테스트(Unit Test) 용이 |
| **재사용성** | 위젯 단위로만 재사용 가능 | 로직(ViewModel)을 여러 UI에서 재사용 가능 |
| **복잡도** | 소규모 기능 구현에 적합 | 대규모 프로젝트 및 복잡한 상태 관리에 적합 |

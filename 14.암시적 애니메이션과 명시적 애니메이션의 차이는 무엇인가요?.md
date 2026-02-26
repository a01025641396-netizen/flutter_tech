1. 핵심 정의 (The Core Difference)
"플러터 애니메이션은 제어의 주체와 수준에 따라 암시적과 명시적으로 나뉩니다. 암시적 애니메이션은 프레임워크가 애니메이션의 생명주기를 관리하여 설정된 목표값으로 자동 전환되는 방식이고, 명시적 애니메이션은 개발자가 AnimationController를 통해 시작, 정지, 반복 등 모든 과정을 수동으로 제어하는 방식입니다."

2. 세부 비교 설명
암시적 애니메이션 (Implicit): * AnimatedContainer나 AnimatedOpacity처럼 'Animated'로 시작하는 위젯을 사용합니다.

단순히 대상 속성값(예: 높이, 색상)만 바꾸면 플러터가 알아서 부드럽게 이어줍니다.

장점: 구현이 매우 빠르고 리소스 관리가 자동이라 간단한 UI 인터랙션에 적합합니다.

명시적 애니메이션 (Explicit): * AnimationController를 필수로 사용하며, 보통 'Transition'으로 끝나는 위젯이나 AnimatedBuilder와 함께 사용합니다.

장점: 애니메이션을 무한 반복(Repeat)하거나, 역재생(Reverse), 혹은 특정 시점에서 멈추는 등의 정교한 조작이 가능합니다.

주의점: TickerProvider를 설정하고 사용이 끝나면 반드시 dispose를 호출해 메모리 누수를 방지해야 하는 등 관리 비용이 발생합니다.

플러터 애니메이션은 제어 수준과 구현 방식에 따라 **암시적(Implicit)** 방식과 **명시적(Explicit)** 방식으로 나뉩니다.

| 비교 항목 | 암시적 애니메이션 (Implicit) | 명시적 애니메이션 (Explicit) |
| :--- | :--- | :--- |
| **제어 주체** | Flutter 프레임워크 (자동) | 개발자 (수동 제어) |
| **핵심 도구** | `Duration`, `Curve` | `AnimationController`, `TickerProvider` |
| **위젯 명칭** | `AnimatedX` (예: AnimatedContainer) | `XTransition` (예: RotationTransition) |
| **구현 난이도** | 낮음 (선언적 방식) | 높음 (명령적 방식) |
| **제어 범위** | 시작값에서 목표값으로 단순 전환 | 재생, 정지, 반복, 역재생, 특정 시점 제어 |
| **상태 관리** | 프레임워크가 내부적으로 관리 | `dispose()` 호출 등 생명주기 관리 필요 |
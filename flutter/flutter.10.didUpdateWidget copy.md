StatefulWidget에서 didUpdateWidget은 어떤 상황에서 사용하나요?
부모 위젯이 재구성되어 현재 위젯에 전달하는 설정값(Property)이 변경되었지만, 위젯의 State 객체는 유지해야 할 때 사용합니다.

예시: 부모로부터 받은 userId가 변경되었을 때, oldWidget.userId와 현재 widget.userId를 비교하여 다를 경우에만 새로운 사용자 정보를 다시 로드하는 로직을 수행합니다.
StatefulWidget의 생명주기에 대해 설명하세요.
createState(): 위젯의 상태 객체를 생성합니다.

initState(): 상태 초기화를 수행합니다. (최초 1회)

didChangeDependencies(): 상위 위젯(Theme, Locale 등)의 데이터가 바뀔 때 호출됩니다.

build(): 화면을 그립니다. setState 시 재실행됩니다.

didUpdateWidget(): 부모 위젯에 의해 설정값이 바뀔 때 호출됩니다.

dispose(): 위젯이 트리에서 제거되며 리소스를 해제합니다.
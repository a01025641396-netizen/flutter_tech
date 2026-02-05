## Flutter 스크롤 위젯 비교 (ListView vs ListView.builder vs SingleChildScrollView)

| 구분 | ListView | ListView.builder | SingleChildScrollView + Column |
| :--- | :--- | :--- | :--- |
| **렌더링 방식** | 모든 아이템을 한 번에 생성 | 화면에 보이는 아이템만 생성 (Lazy) | 모든 위젯을 한 번에 생성 |
| **데이터 규모** | 소규모 (정적 데이터) | 대규모 또는 무한한 데이터 | 소규모 (다양한 위젯 조합) |
| **메모리 효율** | 낮음 (아이템 수에 비례) | **매우 높음** | 낮음 |
| **주요 용도** | 설정 화면, 고정된 메뉴 | 뉴스 피드, 연락처 목록 | 입력 폼, 상세 페이지 레이아웃 |

# "세 방식의 가장 큰 차이점은 렌더링 방식에 따른 메모리 효율성입니다. ListView와 SingleChildScrollView는 모든 위젯을 한 번에 메모리에 올리는 반면, ListView.builder는 화면에 보이는 부분만 동적으로 생성하는 지연 로딩 방식을 취합니다."
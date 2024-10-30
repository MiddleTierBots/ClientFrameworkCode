유니티 클라이언트 샘플 코드입니다.

기본적으로는 클라이언트내의 어떤 씬에서 실행하더라도 구동이 되는 구조가 목표이며, 프레임워크의 주축이 되는 코드는 다음과 같습니다.

AppContext - 클라이언트의 가장 윗단에서 실행되는 메인 로직이며, 클라이언트의 상태등을 보관하고 최상위단에서 게임 로직 실행의 중점이 되는 스크립트입니다.

NetClientLogic - 메인 로직이 구현되는 스크립트이며, 대부분의 데이터 관리, 컨텐츠 로직을 담당하는 중추 스크립트입니다.

TimeManager - SingleTon 패턴으로 구성된 시간 관리 스크립트이며, 유니티 자체의 시간 로직을 보강하여 일시정지, 애니메이터 타임 스케일등의 기능을 보강하기 위해 구성된 스크립트입니다.

Resources - SingleTon 패턴으로 구성된 리소스 관리 스크립트이며, 프리로드된 리소스를 관리하고, 필요한때 GC Call을 통해 메모리 클리닝, 최적화 목적으로 만들어진 스크립트입니다.

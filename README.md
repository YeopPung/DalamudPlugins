## Dalamud 플러그인 레포지토리

이 레포지토리는 한국 [Dalamud](https://github.com/dohwacorp/Dalamud)에서 사용되는 플러그인을 제공합니다.

플러그인들은 서드파티 개발자로부터 관리됩니다. 플러그인이 여기 있다고 우리가 보증한다는 의미는 아니며, 제출 규칙/표준을 준수한다는 의미일 뿐입니다.

대다수의 플러그인은 해외 Dalamud 공식 제공 플러그인 [PluginDistD17](https://github.com/goatcorp/PluginDistD17)에서 제공되는 플러그인을 한국 Dalamud에서 동작하는 버전으로 제공됩니다.

### 플러그인 설치

플러그인을 설치하기 위해서는 Dalamud.Updater를 이용하여 Dalamud를 활성화를 해야합니다. Dalamud가 로드된 이후에 `/xlplugins` 게임 명령어를 통해 플러그인 설치를 열 수 있습니다.

여기에서 플러그인을 수동으로 다운로드할 필요가 없습니다. 플러그인 설치는 게임 내에서 직접 처리됩니다.

### 이러한 플러그인은 거절됩니다.

 - *자동*, 사용자의 직접적인 상호작용 없이 데이터를 가져오거나 요청을 만드는 경우
 - *스펙을 벗어난 방식*, 플레이어가 일반적인 방법으로 불가능한 작업을 서버에 요청하는 경우

#### 플러그인 추가/업데이트

플러그인의 하위 폴더를 만들어 PR을 생성합니다. 하위 폴더의 이름은 플러그인의 "InternalName"(DLL 파일명)으로 지정하고 같은 이름의 [플러그인 정의 Json](https://github.com/goatcorp/DalamudPlugins/blob/master/plugins/owofy/owofy.json)을 포함해야 합니다. 또한 플러그인 DLL, 종속성, 리소스 및 플러그인 정의 json이 포함된 "latest.zip"이라는 압축 파일도 플러그인 DLL과 같은 폴더에 포함되어야 합니다.

플러그인 아이콘은 "YourPlugin/images/"에 "icon.png"로 저장해야 합니다. 아이콘은 플러그인의 기능을 대표할 수 있어야 하며, 투명도가 있어야 하고 최대 512×512 픽셀이어야 합니다.

로컬에 설치된 플러그인의 AssemblyVersion이 이 리포지토리에 푸시된 플러그인 정의 json의 "AssemblyVersion" 필드와 일치하지 않으면 플러그인을 강제로 다시 다운로드해야 합니다.

이에 대한 샘플은 [sample plugin](https://github.com/goatcorp/DalamudPlugins/blob/master/plugins/owofy)을 참조하세요.

#### 플러그인 테스트

새 플러그인을 출시하거나 큰 변경을 할 때는 먼저 이 저장소의 ``testing`` 폴더에 플러그인을 PR해 주세요. 이렇게 하면 테스트 릴리스를 받기로 선택한 사용자가 설치 관리자에서 플러그인을 볼 수 있습니다. [Discord](https://discord.gg/Fdb9TTW9aD)에 가입하여 테스트를 공유 할 수 있습니다.

이 과정은 보통 일주일 이상 걸리지 않지만, 충돌을 일으키거나 플러그인 업데이트를 방해할 수 있는 더 큰 문제를 걸러내는 데 도움이 됩니다.

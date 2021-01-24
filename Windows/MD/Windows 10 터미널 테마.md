# Windows 10 터미널 테마

1.  windows terminal 설치

2.  WSL2 (Windows Subsystem for Linux 2) 설치

    윈도우 10에서 네이티브로 리눅스 실행 파일을 실행 가능하게 하는 서비스로, 리눅스가 호환되는 터미널을 제공해준다.

    1.  powershell을 관리자 모드로 염
    
    2.  dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart (WSL 활성화)
    
    3.  dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart (VM platform 활성화)
    
    4.  https://docs.microsoft.com/ko-kr/windows/wsl/install-win10#step-4---download-the-linux-kernel-update-package 여기로 이동
    
    5.  최신 Linux 커널 업데이트 패키지 다운 후 설치
    
    6.  재부팅
    
    7.  microsoft store에서 Ununtu 20.04 LTS 설치 후 실행
    
    8.  아이디 비번 설정
    
    9.  sudu apt update && sudu apt upgrade
    
    10.  설치 완료 후, powerShell 관리자 권한으로 열고 wsl -l -v
    
    11.  wsl --set-version Ubuntu-20.04 2 (Ubuntu의 버전을 2로 변경)
    
    12.  WSL 2에 커널 구성 요소 업데이트가 필요합니다. 이게 뜨면 Linux 커널 업데이트를 해줘야함
    
    13.  https://github.com/romkatv/dotfiles-public/tree/master/.local/share/fonts/NerdFonts 가서 폰트 4개다 받고 설치
    
    14.  터미널 키고 settings 들어가서 defaultProfile을 Ubunt로 변경
    
    15.  아래 defaults 영역에 "fontFace": "MesloLGS NF" 추가
    
    16.  우분투에서 sudo apt install zsh
    
    17.  sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" 실행
    
    18.  Oh My Zsh 테마 설치 (https://github.com/ohmyzsh/ohmyzsh/wiki/Themes) 테마주소
    
    19.  ```
         git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
         echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc
         ```
    
         위 코드 실행
    
    20.   vim ~/.zshrc
    
    21.  i를 눌러서 ZSH_THEME=robbyrussell을 ZSH_THEME="powerlevel10k/powerlevel10k"로 수정
    
    22.  p10k configure 하면 세팅화면 열림
    
    23.  zshrc에서 LS_COLORS="ow=01;36;40" && export LS_COLORS 추가



## terminal 테마 변경

1.  https://terminalsplash.com/ 원하는 테마의 code 복사

2.  windows terminal에서 ctrl + , 로 세팅 킴

3.  schemes [] 대괄호 안에 코드 잘 넣음

4.  name을 ubuntu의 터미널에  "colorScheme" 라는 key 넣고 value값으로 넣음

5.  default에

    "useAcrylic": true,

    "acrylicOpacity": 0.4


Step 1: 설정 파일 만들기

  sudo nano /etc/udev/rules.d/99-usb-rules.rules


Step 2: 아래 두 줄을 복사해서 붙여넣기 (Ctrl+Shift+V)
(nano 에디터가 열리면 아래 내용을 붙여넣고, Ctrl+O -> Enter로 저장한 뒤, Ctrl+X로 빠져나옵니다.)


  KERNEL=="ttyACM*", MODE="0666"  
  KERNEL=="video*", MODE="0666"


Step 3: 설정 적용하기


  sudo udevadm control --reload-rules
  sudo udevadm trigger


  USB 권한 관련을 해결하는 방법입니다. udev 규칙을 만들어서 해결합니다.

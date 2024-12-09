# Tetris-BlockBusters
## Introduction
LOL(League of Legends)이라는 게임도 이제 어느덧 출시한지 15주년이 되어 갑니다. 어릴 적 스타크래프트 밀리와 유즈맵을 하던 시절을 떠올리면 실내 흡연이 가능하던 담배 찌든 피시방 냄새가 떠오르곤 합니다. Tetris도 5060 어르신들에겐 향수를 불러일으키는 게임입니다. 이러한 고전 근본 비디오 게임 Tetris를 java로 재구현해보았습니다.
## Basic Tetris Rules
![Block move](https://github.com/user-attachments/assets/250ebb6f-d26c-4fd0-b0d8-9ccfa56ba1a6)  ![Block rotation](https://github.com/user-attachments/assets/896d595f-5943-49a5-b906-dc6805f7c024)

위와 같이 Tetris는 block들을 좌, 우, 아래로 움직이고 움직이는 동안 회전시킬 수 있습니다.

![Remove line](https://github.com/user-attachments/assets/c7d4b905-1bc3-43ed-bed0-85d20941d04e) ![Game end](https://github.com/user-attachments/assets/c9970eaa-734c-45db-85b4-b65292b36ede)

Block들을 잘 쌓아서 완성된 줄을 만들게 되면 줄이 사라집니다. 하지만, 상단까지 block들이 쌓이게 되면 게임이 종료됩니다.


## How to play
./src/main/TetrisGame.java 실행합니다.

## Overall Code Design
![image](https://github.com/user-attachments/assets/03ff6327-d346-4892-8d04-e11f388f7ea4)

Tetris-BlockBusters는 위 그림과 같이 총 3개의 package로 구성되어 있습니다. Package들의 기능에 대해서 간략하게 설명하자면:
 - main - TetrisGame의 메인 함수를 포함하고 있는 package입니다. main 함수에서 코드를 실행해 게임을 시작할 수 있습니다.
 - model - Tetris 게임에 필수적인 보드와 블록, 사용자(점수, 등수), 그리고 배경 음악이나 글씨체에 관련된 class들이 포함되어 있습니다.
 - view - Start, end 또는 실제로 game을 진행할때 필요한 graphic에 관련된 class들이 포함되어 있습니다.

## Single Play
![image](https://github.com/user-attachments/assets/bff2c55a-faa3-4b0f-b5de-14c4c45b06d3)

Single mode로 게임을 진행하게 되면 UserID와 난이도를 설정하게 됩니다.
난이도는 전반적으로 block이 내려오는 속도에 관련되어 있고 이를 delay라고 하겠습니다. 난이도에 대한 자세한 설명은 아래와 같습니다:
 - Easy - 격좌 추가 / 500ms 
 - Normal - 500ms
 - Hard - 350ms

![ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/093ed401-7ccf-428a-86a3-871379806698)

Single mode 게임 진행 예시 영상입니다.
![image](https://github.com/user-attachments/assets/7c063bb2-2709-4037-95ec-835f3bb503e5)

게임이 종료되면 해당 난이도에서 가장 높은 점수를 받은 Top3 user의 ID와 점수가 출력됩니다. 그리고 선택할 수 있는 옵션이 3가지가 주어집니다.
 - Retry - 같은 난이도와 같은 User ID로 게임을 재실행 
 - New User - 새로운 User ID와 난이도를 새롭게 설정하여 게임을 실행
 - Exit - 프로그램 종료



## Multi Play
## Debugging Issues

## Program Manual
Manual 파일을 따로 만들었습니다. 다음 파일을 참고해주세요! →
[Manual.pdf](https://github.com/user-attachments/files/18059193/Manual.pdf)
## Demo Video
Single play에 대한 demo video입니다.(Multi play도 블록 동작은 같아서 생략했습니다.) 다음 파일을 참고해주세요! →
![Tetris_demoVideo](https://github.com/user-attachments/assets/78292bba-84d2-4234-9d59-7aa42ed7e49a)

## Conclusion

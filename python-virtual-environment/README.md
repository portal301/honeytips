# Virtual Environment for Python Package Management

- pyenv : 파이썬 버전 바꾸고 싶을 때 (ex. switching python v3.11.x to v3.12.x)

- venv : 파이썬 버전은 바꾸기 어려우나, 같은 파이썬 버전 내에서 패키지 환경만 바꾸고 싶을 때

아래의 명령어를 통해 requirements.txt에 기재된 파이썬 패키지들을 일괄적으로 설치하거나 설치된 패키지 목록을 export할 수 있습니다.

#### requirements.txt 

         save:
         pip freeze > requirements.txt
         install:
         pip install -r requirements.txt


* recommended file tree
  
  바탕화면 - portal301 - robot - ur_rtde & main

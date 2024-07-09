
### 1. Pyenv-pyvirtualenv
Ref: 

[1] https://vhrehfdl.tistory.com/135

[2] https://medical8282.tistory.com/entry/Ubuntu-2004-pyenv-%EC%84%A4%EC%B9%98-%EB%B0%8F-%EB%B2%84%EC%A0%84-%EA%B4%80%EB%A6%AC-%EB%B0%A9%EB%B2%95


#### 1.1. pyenv
On CLI,

(1) Install

           // sudo apt-get install -y make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl git
           sudo apt-get install -y make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev xz-utils tk-dev git

(2) Get pyenv git

           git clone https://github.com/pyenv/pyenv.git ~/.pyenv

(3) Settings

           echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
           echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
           echo 'eval "$(pyenv init --path)"' >> ~/.bashrc
           echo 'eval "$(pyenv init -)"' >> ~/.bashrc
           source ~/.bashrc
   
(4) Check installable python versions & install & execute

           pyenv install -list
           pyenv install 3.10.13
           pyenv shell 3.10.13

           python -V

#### 1.2. pyenv virtualenv
On CLI,

(1) Virtualenv (could be installed already)

           git clone https://github.com/yyuu/pyenv-virtualenv.git ~/.pyenv/plugins/pyenv-virtualenv

(2) Create a virtual environment

           // pyenv virtualenv 3.x.y [env_name]
           pyenv virtualenv 3.10.13 urenv

(3) Activate & deactivate
           pyenv activate [env_name]
           pyenv deactivate



## Example - UR RTDE
#### !! Activate pyenv-virtualenv before following the guide. 
Setup guide: https://sdurobotics.gitlab.io/ur_rtde/installation/installation.html

           pyenv activate [env_name]

           sudo add-apt-repository ppa:sdurobotics/ur-rtde
           sudo apt-get update
           sudo apt install librtde librtde-dev

           ...


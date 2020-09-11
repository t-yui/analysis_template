FROM ubuntu:18.04

# DESCRIPTION : Dockerfile for pystan from jupyter
# REFERENCE : http://rf00.hatenablog.com/entry/2019/01/03/180656
# USAGE:
# 1.   $ docker build -t pystan .
# 2.   $ docker run -v ${path_to_dir}/${target_directory}:/Development/mounted_dir -it --name pystan -p 8888:8888 pystan /bin/bash
#          - ここで、docker 環境中の /Development/mounted_dir ディレクトリにローカルの ${path_to_dir}/${target_directory} ディレクトリをマウントしている
# 3.   $ jupyter notebook --allow-root
# 4.   http://localhost:8888 にアクセス
# 5.   token を入力してログイン
#          - http://(74916b581cf6 or 127.0.0.1):8888/?token=[ここに token が表示される]

# install utility command
RUN apt-get update && \
    apt-get install -y --no-install-recommends wget sudo software-properties-common build-essential && \
    apt-get install -y git

# install anaconda
RUN sudo apt-get update && \
    mkdir downloads && \
    wget -q https://repo.continuum.io/archive/Anaconda3-2018.12-Linux-x86_64.sh -P ./downloads/ && \
    bash ./downloads/Anaconda3-2018.12-Linux-x86_64.sh -b
ENV PATH $PATH:/root/anaconda3/bin

# setup jupyter
RUN jupyter notebook --generate-config && \
    sed -i -e "s/#c.NotebookApp.ip = 'localhost'/c.NotebookApp.ip = '0.0.0.0'/" /root/.jupyter/jupyter_notebook_config.py && \
    sed -i -e "s/#c.NotebookApp.allow_remote_access = False/c.NotebookApp.allow_remote_access = True/" /root/.jupyter/jupyter_notebook_config.py

# install packages
RUN pip install pystan

# make target directory to be mounted
RUN mkdir Development && \
    mkdir Development/mounted_dir

EXPOSE 8888
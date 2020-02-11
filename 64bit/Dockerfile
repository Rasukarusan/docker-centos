FROM centos:7
RUN yum -y update && yum -y install \
  vim \
  less \
  ltrace
RUN mkdir -p /root/.vim/colors
RUN mkdir /root/workspace
COPY ./dotfiles/vimrc /root/.vimrc
COPY ./dotfiles/jellybeans.vim /root/.vim/colors
COPY ./dotfiles/bashrc /root/.bashrc

FROM centos:7
RUN yum -y update && yum -y install \
  vim \
  less \
  ltrace \
  gcc \
  make \
  zsh \
  git \
  wget
RUN ln -sf /usr/share/zoneinfo/Asia/Tokyo /etc/localtime
RUN mkdir -p /root/.vim/colors
RUN mkdir /root/workspace /root/.zsh
RUN git clone https://github.com/mollifier/anyframe /root/.zsh/anyframe
RUN git clone --depth 1 https://github.com/junegunn/fzf.git /root/.fzf && /root/.fzf/install
COPY ./dotfiles/zshrc /root/.zshrc
COPY ./dotfiles/zsh-my-theme.sh /root/zsh-my-theme.sh
COPY ./dotfiles/vimrc /root/.vimrc
COPY ./dotfiles/jellybeans.vim /root/.vim/colors
COPY ./dotfiles/bashrc /root/.bashrc

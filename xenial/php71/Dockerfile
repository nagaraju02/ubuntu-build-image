FROM ubuntu:xenial

ENV DEBIAN_FRONTEND noninteractive

RUN \
  apt-get update && \
  apt-get install -y language-pack-en-base && \
  export LC_ALL=en_US.UTF-8 && \
  export LANG=en_US.UTF-8 && \
  apt-get install -y python-software-properties software-properties-common curl && \
  curl -sL https://deb.nodesource.com/setup_7.x | bash - && \
  curl -sL https://sentry.io/get-cli/ | bash && \
  add-apt-repository ppa:ondrej/php && \
  apt-key adv --recv-keys --keyserver hkp://keyserver.ubuntu.com:80 0xF1656F24C74CD1D8 && \
  echo "deb http://mirror.aarnet.edu.au/pub/MariaDB/repo/10.1/ubuntu xenial main" >> /etc/apt/sources.list.d/mariadb101.list && \
  echo "deb-src http://mirror.aarnet.edu.au/pub/MariaDB/repo/10.1/ubuntu xenial main" >> /etc/apt/sources.list.d/mariadb101.list && \
  apt-get update && \
  apt-get install -y \
    php7.1 \
    php7.1-cli \
    php7.1-dev \
    php7.1-opcache \
    php7.1-bcmath \
    php7.1-bz2 \
    php7.1-common \
    php7.1-curl \
    php7.1-dba \
    php7.1-enchant \
    php7.1-gd \
    php7.1-imap \
    php7.1-json \
    php7.1-ldap \
    php7.1-mbstring \
    php7.1-mcrypt \
    php7.1-pspell \
    php7.1-readline \
    php7.1-soap \
    php7.1-xml \
    php7.1-zip \
    php7.1-mysql \
    php-imagick \
    php-redis \
    php7.1-sybase \
    git \
    nodejs \
    ruby \
    packaging-dev \
    dh-make \
    git-buildpackage \
    reprepro \
    libmariadbclient-dev \
    && \
  apt-get remove -y python-software-properties software-properties-common && \
  apt-get autoremove -y && \
  rm -rf /var/lib/apt/lists/*

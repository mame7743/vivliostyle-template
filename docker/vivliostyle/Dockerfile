FROM node:20-slim

WORKDIR /app

# 必要なパッケージをインストール
RUN apt-get update && apt-get install -y \
    git \
    curl \
    build-essential \
    libgtk2.0 \
    libnss3-dev \
    libatk-bridge2.0-0 \
    libdrm-dev \
    libxkbcommon-dev \
    libgbm-dev \
    libasound-dev \
    fonts-ipaexfont \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# vivliostyle
RUN npm install -g @vivliostyle/cli

WORKDIR /app

# npm プロジェクトを初期化
RUN npm init --yes
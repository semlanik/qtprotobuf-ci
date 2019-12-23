FROM ubuntu:19.04
RUN apt-get -qq update && apt-get -qq install -y libgrpc++-dev \
    protobuf-compiler-grpc libgrpc++1 \
    libgrpc-dev \
    libgrpc6 \
    build-essential \
    cmake \
    golang \
    wget \
    libdbus-1-3 \
    libfreetype6 libfontconfig libx11-6 \
    libgl1-mesa-dev \
    libsm6 \
    libice6 \
    libxext6 \
    libxrender1 \
    doxygen \
    libgtest-dev && apt-get clean
COPY qt_installer.qs /qt_installer.qs
RUN wget --quiet https://download.qt.io/official_releases/qt/5.13/5.13.2/qt-opensource-linux-x64-5.13.2.run -P / && chmod +x /qt-opensource-linux-x64-5.13.2.run && /qt-opensource-linux-x64-5.13.2.run -platform minimal --script /qt_installer.qs && rm /qt-opensource-linux-x64-5.13.2.run

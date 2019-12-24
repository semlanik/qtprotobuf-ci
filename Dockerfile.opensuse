FROM opensuse/leap
RUN zypper --non-interactive ref && zypper --non-interactive in go
RUN zypper --non-interactive in wget \
                             cmake \
                             libXrender1 \
                             libXext6 \
                             libSM6 \
                             Mesa-libGL1 \
                             libfreetype6 \
                             libX11-6 \
                             libdbus-1-3 \
                             fontconfig \
                             libICE6 \
                             gcc-c++ \
                             Mesa-devel \
                             libgthread-2_0-0 \
                             && zypper --non-interactive in --type pattern devel_C_C++
COPY qt_installer.qs /qt_installer.qs
RUN wget --quiet https://download.qt.io/official_releases/qt/5.13/5.13.2/qt-opensource-linux-x64-5.13.2.run -P / && chmod +x /qt-opensource-linux-x64-5.13.2.run && /qt-opensource-linux-x64-5.13.2.run -platform minimal --script /qt_installer.qs && rm /qt-opensource-linux-x64-5.13.2.run

VERSION 0.8

FROM scratch

ARG image=fs:latest

fs:
    FROM scratch
    COPY . /
    SAVE IMAGE --push ${image}

disk:
    ARG file
    FROM scratch

    COPY /${file} /disk/
    SAVE IMAGE --push ${image}

userdata:
    FROM ubuntu:latest
    RUN apt-get update && apt-get install -y genisoimage
    WORKDIR /workdir
    COPY user-data user-data
    RUN touch meta-data
    RUN genisoimage -output /workdir/userdata.iso -volid cidata -joliet -rock user-data meta-data

    SAVE ARTIFACT /workdir/userdata.iso AS LOCAL userdata.iso
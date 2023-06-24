# Android Continuous Integration
## Instruction
- Build

    pull latest app builder image from docker images registry then create new image with updated context and push into image registry

    >note: each builder image includes java, gradle and required development kits


- Debug

    create container with **assembleDebug** entrypoint to build debug version apk then save it as "*job artifact*".   
    container will terminate after building apk

    > debug job run only on dev branch commits

- Release

    create container with **assembleRelease** entrypoint to build release version apk then save it as "*job artifact*".   
    container will terminate after building apk

    > release job run only on tagged commits

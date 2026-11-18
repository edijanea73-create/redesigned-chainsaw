# redesigned-chainsaw
.github/workflows/android.yml.

name: Gerar APK Samuel Sensi

on:
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - uses: actions/setup-java@v4
        with:
          distribution: temurin
          java-version: '17'

      - name: Instalar Gradle
        run: |
          wget https://services.gradle.org/distributions/gradle-8.9-bin.zip
          unzip -q gradle-8.9-bin.zip

      - name: Compilar APK
        run: |
          unzip -q SamuelSensi-Android-Projeto.zip
          cd SamuelSensi-Android
          ../gradle-8.9/bin/gradle assembleDebug

      - uses: actions/upload-artifact@v4
        with:
          name: Samuel-Sensi-APK
          path: SamuelSensi-Android/app/build/outputs/apk/debug/app-debug.apk
          

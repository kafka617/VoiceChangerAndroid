# Voice Changer Android

Project Android native Kotlin, bukan project Flutter. Karena itu, GitHub Actions harus menjalankan Gradle dan tidak boleh mencari `pubspec.yaml`.

## Build APK di GitHub Actions
1. Ekstrak ZIP ini.
2. Upload seluruh isi folder ini ke root repository GitHub. Pastikan `settings.gradle.kts`, `build.gradle.kts`, `app/`, dan `.github/` langsung terlihat di root repository.
3. Buka tab **Actions**.
4. Pilih **Build Voice Changer APK** lalu klik **Run workflow**, atau push ke branch `main`/`master`.
5. Setelah selesai, buka run yang berhasil dan unduh artifact **VoiceChanger-debug-apk**.
6. Artifact berisi `app-debug.apk`.

Workflow memakai JDK 17 dan Gradle 8.9 untuk Android Gradle Plugin 8.7.3.

## Fitur
- Normal, Robot, Echo, Radio
- Mikrofon ke output audio secara langsung
- Izin mikrofon diminta saat tombol MULAI ditekan

Gunakan headset untuk mengurangi feedback. Efek DSP sederhana ini bukan kloning suara atau pengubah identitas suara.

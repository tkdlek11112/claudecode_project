# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 프로젝트 개요

Flutter 웹 전용 프론트엔드. 앱(Android/iOS) 빌드는 사용하지 않음.

## 주요 명령어

```bash
# 의존성 설치
flutter pub get

# 웹 개발 서버 실행
flutter run -d chrome

# 웹 빌드
flutter build web

# 테스트
flutter test
flutter test test/<test_file>.dart  # 단일 테스트
```

## 구조

- `lib/main.dart` — 앱 진입점 및 루트 위젯
- `lib/` — 기능별 디렉토리로 확장 (예: `screens/`, `widgets/`, `services/`)
- `web/` — 웹 전용 설정 파일

## 참고

- 웹 전용이므로 `flutter run` 시 항상 `-d chrome` 또는 `-d web-server` 사용
- Django 백엔드 연동 시 `http` 패키지를 `pubspec.yaml`에 추가
- CORS 이슈는 백엔드 Django 설정에서 해결

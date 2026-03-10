# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 프로젝트 개요

Django 6.0 기반 백엔드 API 서버. Flutter 웹 프론트엔드와 연동.

## 환경 설정

```bash
cd backend
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt  # requirements.txt가 없으면 pip install django
```

## 주요 명령어

```bash
# 개발 서버 실행
python manage.py runserver

# 마이그레이션
python manage.py makemigrations
python manage.py migrate

# 테스트 실행
python manage.py test
python manage.py test <app_name>.tests.<TestClass>  # 단일 테스트

# 슈퍼유저 생성
python manage.py createsuperuser
```

## 구조

- `backend/settings.py` — 프로젝트 설정 (DB: SQLite, 개발 시 DEBUG=True)
- `backend/urls.py` — 루트 URL 라우팅
- `templates/` — Django 템플릿
- 새 앱은 `python manage.py startapp <name>` 으로 생성 후 `INSTALLED_APPS`에 등록

## 참고

- Flutter 웹과 연동 시 CORS 설정 필요 (`django-cors-headers` 추가)
- API 개발 시 `djangorestframework` 사용 권장

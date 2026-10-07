# Hex Loader (Go + Fyne) — CI/CD

Учебный проект: GUI-приложение на Go (Fyne) с автоматической сборкой под Linux, macOS, Windows через GitHub Actions и публикацией в GitHub Releases.

---

## 📸 Скриншоты

### 1. Работающее приложение
<img width="1496" height="944" alt="Снимок экрана 2026-10-07 094442" src="https://github.com/user-attachments/assets/47e7eb39-a0ff-429f-9b90-b7c5e8cdab25" />


### 2. GitHub Actions — успешный CI/CD
<img width="1630" height="637" alt="Снимок экрана 2026-10-07 100916" src="https://github.com/user-attachments/assets/58f0c1e8-6cae-4fb6-8b0f-d04951b0bf51" />


### 3. GitHub Release v1.0.0 — 3 бинарника
<img width="1583" height="875" alt="Снимок экрана 2026-10-07 102232" src="https://github.com/user-attachments/assets/5b0ccd30-2850-4544-a28f-b1a03537544a" />

---

## ⬇️ Скачать

Бинарники доступны в разделе **Releases**:
* 🐧 **Linux x64** — `hex-loader-linux-x64`
* 🍎 **macOS ARM** — `hex-loader-macos-arm64`
* 🪟 **Windows x64** — `hex-loader-windows-x64.exe`

---

## 🛠 Сборка и запуск локально

```bash
# Клонирование репозитория
git clone https://github.com/Evgeny65ok/hex-loader.git
cd hex-loader

# Установка зависимостей и запуск
go mod tidy
go run .
```

---

## 🔁 CI/CD Автоматизация

Конфигурация описана в файле: `.github/workflows/ci.yml`

* **Push в ветку `main`** ➔ Запускается только `job test` (тестирование и проверка кода).
* **Push тега `v*` (например, v1.0.0)** ➔ Запускается `job test` + `job release` (параллельная сборка 3 бинарников и их публикация на GitHub).

---

## 👤 Автор

* **Evgeny65ok** — [GitHub Профиль](https://github.com/Evgeny65ok)

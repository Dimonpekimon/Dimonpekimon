# Привет 👋

Пишу голосовых ассистентов для Windows. Не «умную колонку» в облаке, а
программу, которая живёт на своём компьютере, слышит без интернета и не мешает
работать.

Всё началось с желания сказать в пустую комнату «компьютер, сделай громче» — и
чтобы это сработало. Сейчас это два проекта и несколько тысяч строк кода.

---

## 🎙 Пятница — голосовой ассистент

[![Репозиторий](https://img.shields.io/badge/исходники-Pyatnitsa--Vosk-1f2937?style=flat-square&logo=github&logoColor=white)](https://github.com/Dimonpekimon/Pyatnitsa-Vosk)
[![Релиз](https://img.shields.io/badge/скачать-v3.6-7ff0bd?style=flat-square&logo=windows&logoColor=black)](https://github.com/Dimonpekimon/Pyatnitsa-Vosk/releases)
[![Запуск](https://img.shields.io/badge/запуск-Пятница.exe-2563eb?style=flat-square&logo=windows&logoColor=white)](https://github.com/Dimonpekimon/Pyatnitsa-Vosk/releases/download/v3.6.0/Pyatnitsa-3.6.0.exe)

Ассистент, на котором я обкатываю всё: распознавание, синтез, разбор команд,
интерфейс.

- **92 команды** и 1542 формулировки — от «сделай громче» до «напомни через
  20 минут позвонить маме».
- **Слышит и говорит офлайн.** Vosk распознаёт фразу за 0.2–0.5 с на обычном
  CPU, Piper синтезирует голос локально. Звук никуда не уходит.
- **Понимает разговор.** После ответа 12 секунд можно продолжать без оклика, а
  команду можно сказать сразу после «Пятница» — без паузы на «Да, сэр?».
  Обращение снимается из любого места фразы и в любом падеже.
- **Показывает, нужен ли оклик.** В окне видна метка: `○ скажи «Пятница»` или
  `● без оклика · 8 с`. Больше не приходится гадать и повторять дважды.
- **Живёт в прозрачном окне** поверх рабочего стола: компактные столбики или
  полный диалог с историей.

```text
Вы:     «Пятница, сделай громче и напомни через 20 минут позвонить маме»
Пятница: «Сделал, сэр. Напомню в 22:57.»
Вы:     «а который час?»        ← оклик уже не нужен
Пятница: «Сейчас 22:41, сэр.»
```

---

## 🤖 Jarvis — с чего всё началось

[![Репозиторий](https://img.shields.io/badge/исходники-Jarvis--1f2937?style=flat-square&logo=github&logoColor=white)](https://github.com/Dimonpekimon/Jarvis-)

Первая версия: Ollama с Mistral локально, оклик по слову, несколько команд и
много попыток подружиться с метеослужбой. Многому научился на его ошибках —
именно здесь стало понятно, что распознавание должно быть быстрым, а
интерфейс — не консолью.

---

## Стек

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Electron](https://img.shields.io/badge/Electron-47848F?style=flat-square&logo=electron&logoColor=white)
![Windows](https://img.shields.io/badge/Windows-0078D4?style=flat-square&logo=windows11&logoColor=white)

**Речь:** Vosk, Piper, edge-tts, SAPI
**Мозг:** Gemini, OpenAI-совместимые шлюзы, Ollama
**Ещё:** NumPy, sounddevice, PyInstaller, Win32 API

---

## Как я к этому отношусь

Ассистент должен быть **предсказуемым**. Если он иногда срабатывает, а иногда
нет — это не ассистент, а лотерея. Поэтому в проекте есть метка оклика, окно
разговора и 473 автопроверки: почти каждая странность, которая меня раздражала,
превращалась в тест.

И ещё: **локально — значит быстро и приватно**. Облако остаётся только для
того, где оно действительно нужно, — для свободных вопросов.

---

<p align="center">
  <i>Сделано на Windows, для Windows, с любовью к тишине в комнате.</i>
</p>

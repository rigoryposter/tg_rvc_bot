# Бот в Telegram, который преобразует голос с помощью rvc

Этот бот в Telegram принимает ваши голосовые сообщения и конвертирует их с помощью rvc.
Так же есть функция автоматического создания ИИ каверов

**Существует портативная версия бота, с уже установленными библиотеками [Portable TG RVC Bot](https://huggingface.co/Daswer123/RVC_TG_BOT/tree/main)**

Как только скачаете портативную версию, запустите update_path.bat и начните с пунка 5 в [Гайде по установке](https://github.com/daswer123/tg_rvc_bot/edit/main/README.md#гайд-по-установке)

В качестве бонуса в портативной версии, уже установленна модель Ливанова и вы можете сразу создать конфиг персонажей и протестировать бота

DEMO

https://github.com/daswer123/tg_rvc_bot/assets/22278673/80639ac0-76b2-4942-a45a-43ecd6ed6757

# Ключевые особенности
1) Быстрое создание ИИ каверов, достаточно лишь песни в виде аудиофайла или ссылки на ютуб ролик
2) Преобразование голоса в голос персонажа
3) Возможность тонко настроить преобразование голоса

# Гайд по установке:
1) Убедитесь что у вас установленны: [Python 3.10.x](https://www.python.org/downloads/release/python-3109/), [Node JS 18+](https://nodejs.org/dist/v18.16.1/node-v18.16.1-x64.msi), [Microsoft builders Tools 2019](https://visualstudio.microsoft.com/ru/visual-cpp-build-tools/) , [ffmpeg](https://ffmpeg.org/), [CUDA 11.7](https://developer.download.nvidia.com/compute/cuda/11.7.0/local_installers/cuda_11.7.0_516.01_windows.exe) или [CUDA 11.8](https://developer.download.nvidia.com/compute/cuda/11.8.0/local_installers/cuda_11.8.0_522.06_windows.exe)
2) Создаете бота в botFather
3) клонируете этот репозиторий
4) Запускаете `install.bat` в корневой папке
5) Как только загрузка закончилась заходите в папку utils и запускаете `create main config.bat`, вам нужно будет указать ваш ключ к боту
6) Далее вы должны сформировать структуру ваших голосовых моделей, зайдите в папку MODELS и прочитайте [Readme](https://github.com/daswer123/tg_rvc_bot/tree/main/MODELS#readme), там указана примерная структура папок которая должна быть
   
![image](https://github.com/daswer123/tg_rvc_bot/assets/22278673/713ed830-cf18-4e3f-a4bf-6812b7d3dcdd)

6) Как вы создадите структуру голосовых моделей, запустите скрипт `create characters config.bat` в папке `utils`
7) Все готово! теперь запускайте `start.bat` и начинайте работать с ботом

# Примечания по работе бота
1) Как только добавите нового персонажа,  не забудьте снова запустить скрипт `create characters config.bat` в папке `utils`
2) Бот не расчитан на очень большой поток людей, но сообщения выдает корректно и в правильном порядке
3) Все сообщения от пользователей сохраняются в папке sessions
4) В боте исползуется Mangio-RVC-Fork
5) Бот был протестирован на Windows 10 , RTX 3090, Cuda 11.8

# Credit
1)[Mangio-RVC-Fork](https://github.com/Mangio621/Mangio-RVC-Fork) - Модифицированная версия RVC с новыми методами преобразования
2)[python-audio-separator](https://github.com/karaokenerds/python-audio-separator) - Разделение аудио на вокал и инструментал с помощью MDX архетектуры
3)[Silero TTS](https://github.com/snakers4/silero-models) - TTS на русском языке
4)[doremi](https://github.com/jpmchargue/doremi) - Библеотека для автотюна


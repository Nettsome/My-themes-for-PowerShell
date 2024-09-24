
Туториал от Microsoft: https://learn.microsoft.com/ru-ru/windows/terminal/tutorials/custom-prompt-setup#use-terminal-icons-to-add-missing-folder-or-file-icons

Видосик, по которому я настраивался: https://www.youtube.com/watch?v=kgibCYZVSKw&t=681s 

**Скачал какие-то иконки после которых у меня ничего не изменилось**
![[Скачал какие-то иконки.png]]

Скачал PowerShell 7 версии.

Установил новый шрифт CaskaydiaCove Nerd Font Mono вот отсюда: https://www.nerdfonts.com/font-downloads

Поменял шрифт в параметрах консоли и при этом еще и поменял консоль по умолчанию на Microsoft PowerShell (v7 который).
После у меня разукрасился nvim, добавились стрелочки.

Дальше я установил программу Oh-my-posh, которая позволит настраивать темы для консоли PowerShell 

**Installation OhMyPosh**
https://ohmyposh.dev/docs/installation/windows

```PowerShell
winget install JanDeDobbeleer.OhMyPosh -s winget
```

**Customize PowerShell with OhMyPosh**
https://ohmyposh.dev/docs/installation/customize

Инициализация тем (вроде бы)
```PowerShell
oh-my-posh init pwsh --config ~/jandedobbeleer.omp.json | Invoke-Expression
```

**Установка темы**
```PowerShell
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH/jandedobbeleer.omp.json" | Invoke-Expression
```

**Установка другой темы**
Вводим в терминале
```PowerShell
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH/ " | Invoke-Expression
                                                     ^
```
Нажимаем `Ctrl + Space` там, где стоит курсор `^`. Вылезет список всех тем.
Выбираем тему и вводим название темы на место курсора

**Пример установки другой темы:**
```PowerShell
oh-my-posh init pwsh --config  "$env:POSH_THEMES_PATH/neko.omp.json" | Invoke-Expression
```

Вот что получилось:
```PowerShell
😺💬 Meow! What should I do next? ...                                                                      🏡 ~ ⌚ 15:34 
😀💬 ~ oh-my-posh init pwsh --config  "$env:POSH_THEMES_PATH/neko.omp.json" | Invoke-Expression
```




Нужно еще добавить получившуюся команду в $Profile (т.е. в профиль PowerShell)  





[[Обзор тем Oh-My-Posh]]
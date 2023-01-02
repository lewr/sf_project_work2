0. Добро пожаловать в мой учебный проект!
1. Адрес репозитория https://github.com/lewr/sf_project_work2
2. Для получения доступа к нему сообщите ваш email аккаунта github мне на почту rybnikov.lev@gmail.com
3. Правила именование веток.

main - основная ветка с кодовой базой;  
feature_XXX - ветки для разработки нового функционала;  
stable - ветка с стабильным кодом для прода;  
bugfix_XXX - ветки для оперативного исправления кода;  

Разработка нового функционала:  
main -> feature_XXX -> main -> stable

Исправление общих ошибок:  
stable -> bugfix_XXX -> stable -> main

Вливание в ветки main и stable СТРОГО через merge request (pull request).

Feature и baugfix оформляем СТРОГО в Issues.

4. Начало работы с репозиторием

Клонирование репозитория, ОБЯЗАТЕЛЬНАЯ установка имени и email.

    git clone git@github.com:lewr/sf_project_work2.git  
    cd sf_project_work2  
    git config.name "You name"  
    git config.email "You email"  


Также можете использовать другие параметры, указанные в [примере](https://github.com/lewr/sf_project_work2/blob/main/config.example "config.example")

5. шпаргалка для работы с git

создать ветку feature_XXX (перед этим обязательно: переключится на основную ветку, получить последние изменения)

    git checkout main
    git pull
    git checkout -b feature_XXX

создать ветку bugfix_XXX (перед этим обязательно: переключится на stable ветку, получить последние изменения)

    git checkout stable
    git pull
    git checkout -b bugfix_XXX

После внесения изменения необходимо закомитить и создать pull request

    git commit -a -m 'описание коммита'
    git push origin

Далее на странице [репозитория](https://github.com/lewr/sf_project_work2 "репозиторий") необходимо создать pull request. Исходная ветка - ту что залили, целевая ветка - main (в случае feature) или stable (в случае bugfix). После code review необходимо нажать кнопку merge.

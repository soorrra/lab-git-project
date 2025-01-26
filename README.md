# lab-git-project

# Создание структуры проекта:
git clone https://github.com/soorrra/lab-git-project 
cd lab-git-project  
mkdir src 
mkdir tests  
type nul > src/main.py  
type nul > src/utils.py  
type nul > tests/test_main.py  
type nul > README.md  
type nul > .gitignore  
type nul > requirements.txt  
Код добавленный в main.py:  
"# main.py  
print("Hello World")
Код добавленный в utils.py:  
"# utils.py"  
# Инициализация репозитория и первый коммит:
git add .  
git commit -m "Initial project setup"  
git push origin main  
# Разработка новых функций/компонентов: 6 Работа с ветками:
git checkout -b feature/add-numbers  
git add .  
git commit -m "Add add_numbers function"  
git push --set-upstream origin feature/add-numbers  
git checkout main  
git checkout -b feature/multiply-numbers  
git add .  
git commit -m "Add multiply_numbers function"  
git push --set-upstream origin feature/multiply-numbers  
# Создание pull request'ов:  8 Обработка конфликтов:
git checkout feature/add-numbers  
git add .  
git commit -m "Modify add_numbers"  
git push  
git checkout feature/multiply-numbers  
git add .  
git commit -m "Modify multiply_numbers "  
git push  
git add .  
git commit -m "Resolve merge conflict"  
# Работа с тегами:
git tag v1.0  
git push origin v1.0  
# Работа с stash:
git stash  
git stash apply  
# Работа с rebase:
git checkout -b feature/new-function  
git add .  
git commit -m "Add new_function"  
git add .  
git commit -m "Use new_function"  
git rebase main  
# Работа с cherry-pick:
git log --oneline  
git checkout main  
git cherry-pick <commit-hash>  
# Работа с .gitignore:
git add .  
git commit –m “”  
git push  
# История и восстановление изменений:
git log --oneline --graph --all  
git restore src/utils.py  
git reset --hard c3040fa хэш коммита из ветки feature/multiply-numbers  

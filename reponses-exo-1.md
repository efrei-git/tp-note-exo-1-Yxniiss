Question 1:

mkdir mon_projet && cd mon_projet
git init

git commit --allow-empty -m "Commit 0"
git commit --allow-empty -m "Commit 1"
git branch branch-1
git commit --allow-empty -m "Commit 4"
git commit --allow-empty -m "Commit 5"
git checkout branch-1
git commit --allow-empty -m "Commit 2"
git commit --allow-empty -m "Commit 3"
git checkout main
git merge branch-1 -m "Fusion de branch-1 dans main"

git log --all --decorate --oneline --graph

Question 2:
git branch branch-2
git checkout branch-2
git commit --allow-empty -m "Commit 7"
git commit --allow-empty -m "Commit 8"
git checkout main
git commit --allow-empty -m "Commit 9"
git checkout branch-2
git commit --allow-empty -m "Commit 10"

git log --all --decorate --oneline --graph

Question 3 :

git rebase main branch-2
git log --all --decorate --oneline --graph

question 4 :

git checkout main
git merge branch-2

git log --all --decorate --oneline --graph

question 5:
echo "reponses-exo-1.md" >> .gitignore
git add .gitignore
git commit -m "Ajout de .gitignore"
sed -i '/reponses-exo-1.md/d' .gitignore
git add reponses-exo-1.md
git commit -m "Réponses exercice 1"

question 6:
git remote add origin https://github.com/efrei-git/tp-note-exo-1-Yxniiss
git push origin main

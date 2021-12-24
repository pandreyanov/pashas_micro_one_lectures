jupyter-book build ./; ghp-import -n -p -f _build/html
git add *; git commit -m "auto commit"; git push -u origin

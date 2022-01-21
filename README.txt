pip install sphinxcontrib-mermaid
pip install sphinx-proof

conda install -c conda-forge jupyter-book

rm -rf ./_build; jupyter-book build ./; ghp-import -n -p -f _build/html

git add *; git commit -m "auto commit"; git push -u origin

cd /Users/pasha/Documents/GitHub/pashas_micro_one_lectures; jupyter-book build ./; ghp-import -n -p -f _build/html; git add .; git commit -m "auto commit"; git push -u origin
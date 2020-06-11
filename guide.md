# Guide til brug af workshop template



Opret GitHub repo:

Navn: `workshop_[navn]`



Lav en ny side med hugo:

`hugo new site [workshop navn]`



Initialiser git repo

`git init`



Tilføj workshop template som remote:

`git remote add temp git@github.com:caldissKjelmann/workshop_template.git`



Fetch og reset:

`git fetch temp master`
`git reset --hard FETCH_HEAD`



Tilføj tema (fjern først mappen)

`git rm themes/hugo-theme-learn`

`git submodule add -f https://github.com/matcornic/hugo-theme-learn.git themes/hugo-theme-learn`



Tilføj repo

`git remote add upstream [...]`



Hvis der skal merges med eksisterende repo:

`git pull upstream master --allow-unrelated-histories`



Kopier `add_gh-pages.sh` ud af repo og fjern

`git rm add_gh-pages.sh`



Tilføj `add_gh-pages.sh` til `.gitignore`

`echo "add_gh-pages.sh" >> .gitignore`

(add og commit)



Tilføj indhold med parser script (`parse_ws-md.py`)



Indsæt billeder i static-mappen



Rediger tabeller fra HTML til markdown

https://jmalarcon.github.io/markdowntables/



Ændr forside (`_index.md`)



Opdater `config.toml`

- Main URL skal svare til GitHub Pages URL



Skub ændringer til master



Kopier deploy script tilbage igen og kør (Opret `gh-pages` branch som deployment branch (`add_gh-pages.sh`) )

https://gohugo.io/hosting-and-deployment/hosting-on-github/#deployment-of-project-pages-from-your-gh-pages-branch



Skub public til `gh-pages` (`commit_gh-pages`)


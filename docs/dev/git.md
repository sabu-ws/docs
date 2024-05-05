# Git
Use git

## Pull or Push
```
git add . OR git add myfile
git commit -m « this is m’y commit »
git pull

if « Already Up To Date »
{
  git push
} 
else if « conflit »
{
  Check and merge local conflit
  git push
}
else
{
  Give Up Dude :D
}
```

## Merge branch
```
git merge and see doc dude
```

## Si problème
```
Erreur lors d'un git pull :
hint: You have divergent branches and need to specify how to reconcile them.
hint: You can do so by running one of the following commands sometime before
hint: your next pull:
hint: 
hint:   git config pull.rebase false  # merge
hint:   git config pull.rebase true   # rebase
hint:   git config pull.ff only       # fast-forward only
hint: 
hint: You can replace "git config" with "git config --global" to set a default
hint: preference for all repositories. You can also pass --rebase, --no-rebase,
hint: or --ff-only on the command line to override the configured default per
hint: invocation.
fatal: Need to specify how to reconcile divergent branches.

Si les fichiers n'ont pas étés modifiés par 2 personnes (donc ne sont pas en conflit)(voir dans vscode) -> git merge puis git pull puis git push
```
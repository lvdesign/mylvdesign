
bundle exec jekyll serve --livereload

bundle exec jekyll build --trace



git status

// https://lea.verou.me/2011/10/easily-keep-gh-pages-in-sync-with-master/
git checkout gh-pages // go to the gh-pages branch
git rebase master // bring gh-pages up to date with master
git push origin gh-pages // commit the changes
git checkout master // return to the master branch

git push

My suggestion would be to create gh-pages as an --orphan branch and only include the publication-ready material in it. You would have to clone from your master in a different local directory, use git checkout --orphan gh-pages to create gh-pages and then delete all the unnecessary files using git rm -rf .. From there you can go on and push to gh-pages after having added your publish-only files. Refer to Github docs for more info:
https://help.github.com/articles/creating-project-pages-manually/



Mettre _site dans _docs pour mise en ligne de gh_pages avec root _docs
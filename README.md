# to deploy a new version to the repository:
# we don't build an executable - we just push the source
# the make just verifies
make
git checkout -b v0.0.5
git add .
git commit -m "revision v0.0.5"
git push --set-upstream origin v0.0.5
git checkout master
git merge v0.0.5
git push

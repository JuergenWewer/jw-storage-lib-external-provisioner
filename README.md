# to deploy a new version to the repository:
# we don't build an executable - we just push the source
# the make just verifies
enter the new version in go.mod
make
git checkout -b v0.0.6
git add .
git commit -m "revision v0.0.6"
git push --set-upstream origin v0.0.6
git checkout master
git merge v0.0.6
git push

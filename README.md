# to deploy a new version to the repository:
# we don't build an executable - we just push the source
# the make just verifies
make
git checkout -b v0.0.3
git add .
git commit -m "revision v0.0.3"
git push
git push --set-upstream origin v0.0.3
git checkout master
git merge v0.0.3

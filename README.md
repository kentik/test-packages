# test-pckages

## Copy from packages
```bash
export PACKAGE=kagent/v1.8.4
rm -rf tmp_download
gh release download -R kentik/packages ${PACKAGE} -D tmp_download
gh release create -R kentik/test-packages ${PACKAGE}
gh release upload -R kentik/test-packages ${PACKAGE} tmp_download/*
```

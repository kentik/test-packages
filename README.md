# test-pckages

## Copy from packages
```bash
export PACKAGE=kagent/v3.0.1
rm -rf tmp_download
gh release download -R kentik/packages ${PACKAGE} -D tmp_download
gh release create --generate-notes -t ${PACKAGE} -R kentik/test-packages ${PACKAGE}
gh release upload -R kentik/test-packages ${PACKAGE} tmp_download/*
```

# helm commands

- 查看最终被渲染的helm chart

```
helm install --debug --dry-run goodly-guppy ./mychart.
helm template --debug

#is your go-to tool for verifying that your chart follows best practices
helm lint 

#This is a good way to see what templates are installed on the server
helm get manifest

```


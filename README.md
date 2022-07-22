# tools

## Git

### Clean up local branches
`git branch | select-string -notmatch master | foreach {git branch -d ("$_").Trim() --force}`

## Powershell

### View command history in vscode
`code (Get-PSReadlineOption).HistorySavePath`

## VsCode

### Find using outside of namespace
`\n(.*?)\s+namespace`

### Save without auto format
`ctrl+k, ctrl+shift+s`

## Chrome Devtools

### Monitor all JS events
`monitorEvents(event)`

## kubectl

### View details on single pod
`kubectl describe pod hostname -n=namespace`

### List pods in namespace
`kubectl get pods -n=namespace`

### Stream logs for one pod
`kubectl logs -f hostname -n=namespace`

### Scale pod replicas
`kubectl scale statefulsets hostname -n=namespace --replicas=1`

## Webhooks
`hookbin.com`


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

### Set up from scratch
1. az login
2. az account list -o table
3. az account set --subscription <subscription_id>
4. az aks list
5. az aks get-credentials --resource-group <resource_group> --name <name_of_aks_service>

### View details on single pod
`kubectl describe pod hostname -n=namespace`

### List pods in namespace
`kubectl get pods -n=namespace`

### Stream logs for one pod
`kubectl logs -f hostname -n=namespace`

### Scale pod replicas
`kubectl scale statefulsets hostname -n=namespace --replicas=1`

## Webhooks

### Test webhook functionality
`hookbin.com`

### Ngrok - test local resources remotely
`https://ngrok.com/`

## Java

### Import self signed cert into main cacerts key store (under %JAVA_HOME%)
```
keytool -cacerts -list -v
keytool -cacerts -delete -alias cosmos_emulator
keytool -cacerts -importcert -alias cosmos_emulator -file <path to file>
```

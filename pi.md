Useful extensions:
- Web Search - https://pi.dev/packages/pi-web-access (pi install npm:pi-web-access)
- Context reduction - https://pi.dev/packages/context-mode (pi install npm:context-mode)
- AI asks you questions - https://pi.dev/packages/@juicesharp/rpiv-ask-user-question (pi install npm:@juicesharp/rpiv-ask-user-question)
- Permissions - https://pi.dev/packages/@gotgenes/pi-permission-system (pi install npm:@gotgenes/pi-permission-system)
- Todo list rendered inline - https://pi.dev/packages/@juicesharp/rpiv-todo (pi install npm:@juicesharp/rpiv-todo)
- Add planning mode - https://pi.dev/packages/@plannotator/pi-extension (pi install npm:@plannotator/pi-extension)
- If you need MCP - https://pi.dev/packages/pi-mcp-adapter (pi install npm:pi-mcp-adapter)

Permissions config I have gone for:
```json
{
  "permission": {
    "*": "ask",
    
    "read": "allow",
    "write": "allow",
    "edit": "allow",
    
    "todo": "allow",
    "web_search": "allow",
    "source_check": "allow",
    "ask_user_question": "allow",
    "fetch_content": "allow",
    "get_search_content": "allow",
    
    "mcp_status": "allow",
    "mcp_list": "allow",
    "mcp_search": "allow",
    "mcp_describe": "allow",
    
    "path": {
      "*": "allow",
      "*.env": "deny",
      "*.env.*": "deny",
      "*.env.example": "allow",
      "*secret*": "ask",
      "*.pem": "deny",
      "*.key": "deny",
      "id_rsa*": "deny",
      "~/.ssh/*": "deny",
      "~/.aws/credentials": "deny",
      "~/.config/gcloud/*": "deny"
    },
    
    "bash": {
      "*": "ask",
      
      "cat *": "allow",
      "head *": "allow",
      "tail *": "allow",
      "less *": "allow",
      "more *": "allow",

      "ls *": "allow",
      "tree *": "allow",
      "stat *": "allow",
      "file *": "allow",
      "wc *": "allow",
      "du *": "allow",
      "df *": "allow",

      "grep *": "allow",
      "egrep *": "allow",
      "fgrep *": "allow",
      "rg *": "allow",
      "find *": "allow",
      "fd *": "allow",

      "diff *": "allow",
      "cmp *": "allow",
      "comm *": "allow",
      "md5sum *": "allow",
      "sha1sum *": "allow",
      "sha256sum *": "allow",
      "cksum *": "allow",

      "pwd": "allow",
      "whoami": "allow",
      "id": "allow",
      "hostname": "allow",
      "uname *": "allow",
      "date": "allow",
      "uptime": "allow",
      "ps *": "allow",
      "printenv *": "allow",
      "which *": "allow",
      "type *": "allow",

      "git status": "allow",
      "git diff *": "allow",
      "git log *": "allow",
      "git show *": "allow",
      "git blame *": "allow",
      "git ls-files *": "allow",
      "git branch": "allow",
      "git remote -v": "allow",
      
      "git rev-parse *": "allow",
      "git check-ignore *": "allow",
      
      "git * --dry-run *": "allow",
      "git * -n *": "allow",

      "kubectl get *": "allow",
      "kubectl describe *": "allow",
      "kubectl logs *": "allow",
      "kubectl top *": "allow",
      
      "kubectl * secret": "ask",
      "kubectl * secret *": "ask",
      "kubectl * secrets": "ask",
      "kubectl * secrets *": "ask",
      "kubectl * secret/*": "ask",
      "kubectl * secrets/*": "ask",
      
      "kubectl * vaultstaticsecret": "allow",
      "kubectl * vaultstaticsecret *": "allow",
      "kubectl * vaultstaticsecrets": "allow",
      "kubectl * vaultstaticsecrets *": "allow",
      "kubectl * vaultstaticsecret/*": "allow",
      "kubectl * vaultstaticsecrets/*": "allow",

      "rm -rf *": "deny",
      "sudo *": "ask"
    },
    
    "external_directory": {
      "*": "ask",
      "~/.pi/*": "allow"
    }
  }
}
```

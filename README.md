### thefuck
---
https://github.com/nvbn/thefuck

```py
def match(command):
  return ('permission denied' in command.output.lower()
    or 'EACCES' in command.output)
    
def get_new_command(command):
  return 'sudo {}'.format(command.script)
  
enabled_by_default = True

def side_effect(command, fixed_command):
  subprocess.call('chomd 777 .', shell=True)
  
priority = 1000
requires_output = True
```

```sh
pip install thefuck
eval $(thefuck --alias)
export THEFUCK_FULES='sudo::no_command'
eval $(thefuck --alias --enable-experimental-instant-mode)

```

```
```



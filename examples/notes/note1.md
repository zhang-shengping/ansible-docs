### run ansible locally
A way:
1. define `ansible_playbook_python: /root/f5-venv/bin/python` in variables file such as (group_vars/f5-test.yaml)
2. define `connection: local` for one play and its tasks
3. define `ansible_python_interpreter: "{{ ansible_playbook_python }}"` in playbook as vars as well
4. delete all `delegate_to: localhost`

B way:
1. just define `delegate_to: localhost` for every local task.
2. delete all the things defined in way A

Notes:
node name in inventory should not the same as local or 127.0.0.1, when local define in playbook

### refer:
http://willthames.github.io/2018/07/01/connection-local-vs-delegate_to-localhost.html

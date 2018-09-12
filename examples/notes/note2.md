### how to debug ansible
A way:
1. run command with `-vvv` such as `ansible-playbook -vvv -i inventory/hosts playbook.yaml`

B way:
1. inject pdb breakpoint into module code.
2. configure your `json` format variables file, refer to the module defined
3. run command such as `python bigip_device_license.py /root/f5-ansible/examples/0002-license-bigip/group_vars/f5-test.json`
4. do forget to source activate python virtualenv

### BIGIP where to use different type dossiers to get different licenses

1. For Production Env: https://activate.f5.com/license
2. For Production Dev Env: https://license.f5net.com/license

**to get register key from: https://license.f5net.com**

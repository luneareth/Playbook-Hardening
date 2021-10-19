>> Dwi
## How To Use

### WARNING

Test only : Centos 7 and Rocky Linux 8.4
Take your own risk!!!

## Roles :

1. luneareth_iam for hardening OS
2. app_croncat_near_blockchain for auto deplyoment app croncat near blockchain


### Varaible Global Roles luneareth_iam:

```
    - user_root: root
    - user_admin: luneareth
    - user_app: app
    - password_luneareth: "$6$4YJgt5xxxXtIl2WTN/3$GJPEKYAosq2bElROiiXByGAI8wEddgE7.RN1LpyAGLs4KD8KwU7S70wg2zbtENxak2T6CRdh9iySM..mzNX5a0"
    - password_app: "$6$ERarx7DYOxx9k1wP3k$Kr8Wp6L8NcfKmG2C8S9jtEGCpYH2RNYBHhDShKv7HNDzgEpff8voNoy6a.NQFJl7orfOIh11fFyk89HLbQHBu/"
    - password_root: "$6$f5hXa3ExxxbOaonKXYh$m38.zKqfxoyCSc/k9iDWeqNyxUES1GIFmJzs.GxMFb/uTxuCzNNewlaXeV4SHPx1PneMo3sr.z1x.qQTYmngn."
    - public_key: "ssh-rsa xxxxxxxxxxx"
``` 

### How To Generate Password

Using Python:

```
python3 -c 'import crypt; print(crypt.crypt("password"))'
```

or 

Using Ruby:

```
ruby -e 'puts "password".crypt("$6$saltsalt$")'
```

### Varaible Global Roles luneareth_app-croncat:

```
account_near: "luneareth.tesnet"
```

### How To Execute Global Ansible

Execute :

```
ansible-playbook -i inventories/production/hosts -l app  server-iam.yml --ask-vault-pass   -K 
```

# DONATE

1. Ethereum : 0xB0e6e6c379389bBB30fACD427e02d74d27ec0C78

2. Near Blockchain : ohmeth.near 

3. Mina Protocol : B62qiiBBXKN5CdgXv7wPkXxC1prdzQxwfaTMAi3isAeb9F7gCbzi5dU
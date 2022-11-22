# sops-kms

# Prerequisites
Install sops
   ```
   brew install sops
   ```

# Encrypting the keys
To encrypt the keys run the following command (only 1st time)
   ```
   sops -e --in-place secrets/credentials.yaml
   ```

# Decrypting the keys
To decrypt the keys run the following command
   ```
   sops -d secrets/credentials.yaml
   ```
# Editing the keys
To decrypt the keys run the following command
   ```
   sops secrets/credentials.yaml
   ```

# Cloudformation deploy
```
aws cloudformation deploy \
--stack-name sops-kms \
--template-file ./cloudformation.yaml \
--capabilities CAPABILITY_NAMED_IAM \
--region us-east-1
```

# Useful resources
https://github.com/mozilla/sops
https://swiety-python.blogspot.com/2021/02/mozilla-sops-secrets-operations.html

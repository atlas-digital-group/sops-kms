# sops-kms
[sops](https://github.com/mozilla/sops) is an editor of encrypted files that supports YAML, JSON and
BINARY formats and encrypts with AWS KMS and PGP

# Prerequisites
Install sops
   ```
   brew install sops
   ```
# Cloning the repository
Clone the repository by executing the following command
   ```
   git@github.com:atlas-digital-group/sops-kms.git
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

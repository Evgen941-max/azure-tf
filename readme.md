# Instruction


# Init bin-file:

```bash
    terraform plan -out=main.tfplan
```

# Apply bin-file:

```bash
    terraform apply main.tfplan
```

# Init delete bin-file:

```bash
    terraform plan -destroy -out=planfile
```

# Apply delete bin-file:

```bash
    terraform apply planfile
```

# When you run "terraform apply main.tfplan", you need add private ssh-key, you can use this command:

```bash
    terraform output -raw tls_private_key > id_rsa
    terraform output public_ip_address
```

# And you can try connect to VM:

```bash
    ssh -i id_rsa azureuser@<public_ip_address>
```
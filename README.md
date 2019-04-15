# Bitwarden decrypt CLI

> This is a port of the Bitwarden NodeJS CLI to Python focused on decryption of secrets

## Why this project ?

We use Ansible to manage infrastructures and use a lookup plugin to grab hundred of secrets. Each secret is retrieven 
with the native NodeJS CLI in about 0.85s on my computer. When you have hundreds of secrets, that makes long minutes to wait.

According to https://github.com/bitwarden/cli/issues/67, node looks like to suffer from slow bootstrap.

This port to Python is aimed to increase secrets lookup performance. First benchmarks spotted that secrets could be 
retrieven in around 0.15s with this port.


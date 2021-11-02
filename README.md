### Usage Instructions

1. Clone repository.
2. Install the Azure CLI for your respective operating system: https://docs.microsoft.com/en-us/cli/azure/install-azure-cli.
3. Install Terraform for your respective operating system: https://learn.hashicorp.com/tutorials/terraform/install-cli.
3. Using your CLI, run ``` az login ``` and authenticate with your Azure account.
4. Move into the repository ``` cd <repository-name> ```.
5. Run ``` terraform init ```
7. Run ``` terraform apply ```
8. Non-sensitive variables will be displayed after terraform apply is complete.
8. Point your browser to http://<public_ip> .
9. To retrieve the SSH key ``` terraform output -raw vm_tls_private_key > ~/.ssh/azure_vm.pem ```
10. To SSH into the virtual machine instance
    ``` chmod 600 ~/.ssh/azure_vm.pem ```
    ``` ssh -i ~/.ssh/azure_vm.pem azureuser@<public_ip> ```
11. Run ``` terrafom destroy ``` so you don't get billed.

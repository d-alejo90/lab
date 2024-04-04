## IaC - Tipos de Enfoques
Hay 2 tipos de enfoques para IaC. declarativo(funcional) y imperativo(procedimental).

- Declarativo (funcional): Se enfoca en describir el estado deseado del sistema, sin especificar los pasos para llegar a ese estado. Se describe la infraestructura que se quiere tener, pero no cómo llegar a ella. Ejemplo: Terraform.
  - Quiero tener un bucket S3 llamado mybucket con permisos privados.
  - ```resource "aws_s3_bucket" "mybucket" {
    bucket = "mybucket"
    acl = "private"
  }
  ```
  - 
- Imperativo (procedimental): Se enfoca en describir los pasos que se deben seguir para llegar al estado deseado. Se describe cómo llegar a la infraestructura deseada. Ejemplo: Ansible.
  - `aws s3 mb s3://mybucket`
  - `aws s3 cp file.txt s3://mybucket`
  - `aws ec2 launch-instance --image ami-123456`

## Que es IaC?

Infraestructura como código (IaC) es el proceso de gestionar y aprovisionar la infraestructura de TI a través de scripts de configuración en lugar de configuración manual. Los scripts pueden ser en lenguajes de programación o en lenguajes de configuración específicos de la herramienta que se esté utilizando.

- Terraform
- CloudFormation
- Pulumi
- Azure Resource Manager


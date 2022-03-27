# aws-subnet
https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/subnet

vpc_id is the id on the vpc this subnet is in

resource "aws_subnet" "main" {
  vpc_id     = aws_vpc.main.id
  cidr_block = "10.0.1.0/24"

  tags = {
    Name = "Main"
  }
}
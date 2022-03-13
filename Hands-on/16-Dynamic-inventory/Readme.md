# Dynamic inventory

* Create custom inventory directory

* Create .yaml file under the newly created directory and paste below code which uses `aws_ec2` plugin

```
---
plugin: aws_ec2
aws_access_key: <YOUR-AWS-ACCESS-KEY-HERE>
aws_secret_key: <YOUR-AWS-SECRET-KEY-HERE>
keyed_groups:
  - key: tags
    prefix: tag
```

* Modify `ansible.cfg` file
* Find the [inventory] section and add the following line to enable the ec2 plugin

```enable_plugins = aws_ec2```

* Now test the dynamic inventory configuration by listing the ec2 instances

```ansible-inventory -i <inventory-file-path><filename>.yaml --list```

* The above command returns the list of ec2 instances with all its parameters in JSON format

* Post this you can add this line into inventory file

```inventory      = <inventory_path><filename>.yaml```

* Do ping check of all hosts

```ansible all -m ping```

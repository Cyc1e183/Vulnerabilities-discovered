Affected version: Wordpress before 5.8.2

Vulnerable path: /wp-admin/update.php.

Causes of vulnerability:

![1638930926342](https://user-images.githubusercontent.com/61731702/145139507-39406ce4-e15b-4e6a-8d96-2ef5d746e74e.png)


WordPress does not restrict the extension of Plugins uploaded by users, which allows attackers to upload arbitrary files, such as PHP, HTML, etc.For example uploading php files:`<?php phpinfo();?>`. The uploaded file will be saved in /wp-content/uploads/[year]/[month]/filename.



![1638931129724](https://user-images.githubusercontent.com/61731702/145139512-c51bb424-64d4-448d-9826-7c7a536ba87d.png)


![1638931163062](https://user-images.githubusercontent.com/61731702/145139514-63adcfec-d205-4727-b297-7058161a3cdb.png)


Repair suggestion: Strict restrictions on uploaded plugin extensions.


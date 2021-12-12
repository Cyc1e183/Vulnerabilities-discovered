Affected version: Wordpress before 5.8.2

Vulnerable path: /wp-admin/theme-install.php.

Causes of vulnerability:

![1638932151821](https://user-images.githubusercontent.com/61731702/145712117-f57b72c7-6a7a-4b0b-a04f-967964b2d866.png)


WordPress does not restrict the extension of Themes uploaded by users, which allows attackers to upload arbitrary files, such as PHP, HTML, etc.For example uploading php files:`<?php phpinfo();?>`. The uploaded file will be saved in /wp-content/uploads/[year]/[month]/filename. We can access the uploaded files through http://x.x.x.x/wp-content/uploads/[year]/[month]/filename, and GETSHELL.

![1638932199102](https://user-images.githubusercontent.com/61731702/145712120-14023cf1-8ef1-481f-bddb-c1e72d20396b.png)

![1638931163062](https://user-images.githubusercontent.com/61731702/145712126-b40d5f2d-e972-4f1f-a616-49235114d37e.png)


Repair suggestion: Strict restrictions on uploaded themes extensions.

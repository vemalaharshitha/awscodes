# awscodes
codes to upload
sudo apt update
sudo apt install mysql-server -y
sudo mysql
CREATE DATABASE library;
USE library;

CREATE TABLE BOOKS(
    id INT PRIMARY KEY,
    title VARCHAR(20),
    author VARCHAR(20),
    publisher VARCHAR(20)
);
INSERT INTO BOOKS VALUES(101, 'Ramayana', 'Valmiki', 'Yamini');
INSERT INTO BOOKS VALUES(102, 'Mahabharata', 'Vyasa', 'Harshitha');
INSERT INTO BOOKS VALUES(103, 'Harrypotter', 'Rowling', 'Harshitha');
SELECT * FROM BOOKS;
exit;
//ec2
#!/bin/bash
# Update system packages
yum update -y

# Install Apache web server
yum -y install httpd

# Enable Apache to start on boot
systemctl enable httpd

# Start Apache service
systemctl start httpd

# Create a simple web page
echo '<html><h1>Hello World!</h1></html>' > /var/www/html/index.html
//s3
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": [
        "s3:GetObject"
      ],
      "Resource": [
        "arn:aws:s3:::your-bucket-name/*"
      ]
    }
  ]
}



take note on the following:
1. dapat absolute server path padung sa .htpasswd file
  ** if unsure sa abs path, try <?php echo __FILE__; ?> sa directory kung asa ang .htpasswd (usually root)
2. dapat ang password nka md5(APR) from this online generator http://www.htaccesstools.com/htpasswd-generator/

Note :
1. Make it sure that the .htpasswd file path is in absolute path.
  *** You can use the <?php echo __FILE__; ?> in PHP in displaying the path.
  
2. Generate the password using the following scripts :
bcrypt
$ htpasswd -nbB myName myPassword
myName:$2y$05$c4WoMPo3SXsafkva.HHa6uXQZWr7oboPiC2bT/r7q1BB8I2s0BRqC

MD5
$ htpasswd -nbm myName myPassword
myName:$apr1$r31.....$HqJZimcKQFAMYayBlzkrA/

SHA1
$ htpasswd -nbs myName myPassword
myName:{SHA}VBPuJHI7uixaa6LQGWx4s+5GKNE=

CRYPT
$ htpasswd -nbd myName myPassword
myName:rqXexS6ZhobKA

OR

From this online generator http://www.htaccesstools.com/htpasswd-generator/


Referenece : http://httpd.apache.org/docs/2.4/misc/password_encryptions.html

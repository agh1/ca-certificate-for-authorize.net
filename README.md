# ca-certificate-for-authorize.net
Ye olde certificate authority certificate needed for authorize.net

An upgrade to the ca-certificates package in Ubuntu removes the certificate authority certificate that's needed for 
connecting to Authorize.net.  This is the certificate you need.

1. create a folder for the extra certificate authority certificates

sudo mkdir /usr/share/ca-certificates/extra

2. put that certificate in the appropriate directory

cd /usr/share/ca-certificates/extra

sudo wget [url of the raw certificate file]

3. reconfigure the ca-certificates package

sudo dpkg-reconfigure ca-certificates

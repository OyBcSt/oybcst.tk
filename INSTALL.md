#Install OyBcSt

This will be the public facing 'portal' to the website.  I am using Jetstream2, m3.quad with Ubuntu 20, 16GB RAM and 100GB root volume.

##Installing NGINX.  
Thank you again [Digital Ocean](https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-20-04)

Set a new .vimrc after creating a new instance with `set paste` to turn off auto-indenting with pastes.

I had to remove 'default' from sites-enabled.

##Get SSL cert
For now, I am pointing this to main.oybcst.tk, since the RShiny one is pointing at the apex domain.

[Digital Ocean - Let's Encrypt](https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-ubuntu-20-04)

Actually, I have to do this later, because server block has to match...

##Put stuff on it.
'Install' bootstrap.

```
wget https://github.com/twbs/bootstrap/releases/download/v4.5.3/bootstrap-4.5.3-dist.zip
unzip bootstrap-4.5.3-dist.zip 
cp -r css /var/www/oybcst.tk/html
cp -r js /var/www/oybcst.tk/html
rm -fr ~/bootstrap-4.5.3-dist*
```

Make sure to 'git clone' to 'html' and put js and css in gitignore.






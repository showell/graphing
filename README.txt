This is an example way to create a generic graphing engine that can take
customized data sources.  It is not intended to grow into a project; it's
mostly just example code to get a quick start with nginx and jqplot.

example usage:
    http://localhost:8000/graphing/foo.html?url=/graphing/foo.json

jqplot:
    https://bitbucket.org/cleonello/jqplot/downloads/

nginx:
    http://mjijackson.com/2009/07/install-nginx-on-osx
    sudo vim /opt/local/etc/nginx/nginx.conf
    sudo kill `cat /opt/local/var/run/nginx/nginx.pid`
    sudo /opt/local/sbin/nginx

    virtual host setup:
        server {
            listen       8000;

            location ~ /jqplot/ {
                root   /Users/steve;
                index  index.html index.htm;
            }

            location ~ /graphing {
                root   /Users/steve;
            }
        }


TODO:
    figure out way to access url thru query vars (impossible thru nginx?)

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
            # listen       somename:8080;
            # server_name  somename  alias  another.alias;

            location ~ /jqplot/ {
                root   /Users/steve;
                index  index.html index.htm;
            }

            location ~ /graphing {
                root   /Users/steve;
            }
        }


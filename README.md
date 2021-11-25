# nginx-proxy

Docker-compose files to connect multiple docker-containers with nginx

## Usage

Start the container with

```shell
docker-compose up -d
```

## Configuration

This nginx-proxy has a predefined configuration:

- Increase client_max_body_size to 64M ([nginx documentation](http://nginx.org/en/docs/http/ngx_http_core_module.html#client_max_body_size))
- Set server_tokens to off ([nginx documentation](http://nginx.org/en/docs/http/ngx_http_core_module.html#server_tokens))

## Redirection

If you are using this proxy on your local machine, you maybe have to add your domains to the vhost file.

Read more here: [How to Edit Your Hosts File on Windows, Mac, or Linux (Christopher Welker, How-To-Geek)](https://www.howtogeek.com/howto/27350/beginner-geek-how-to-edit-your-hosts-file/)

## SSl-Certifications

Add you certification-files to the directory `certs`. If you added a new cert-file, you have to restart the container.

For your local environment you can use this tool to [create your own certificates](https://github.com/erkenes/ssl-certs-local)
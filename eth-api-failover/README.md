# Example of failover strategy for those who need to call ETH API

## Install nginx

`sudo apt update`

`sudo apt install nginx`

## Configure nginx

copy content of the `default` file to the `/etc/nginx/sites-enabled/default`

restart nginx `service nginx restart`

## Test call

`curl -H "Content-Type: application/json" --data '{"jsonrpc":"2.0", "method":"eth_getBalance", "params":["0xcAFEfeF5B02608FC18c99B0995f71D408Ae22720", "latest"], "id":1}' http://127.0.0.1:7777`

You are good to go. Now you could use `http://127.0.0.1:7777` as a general entry point for the several eth API.

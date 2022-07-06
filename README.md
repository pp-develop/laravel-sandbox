## laravel-sandbox
## Usage
run your containers
```
$ docker-compose up -d
```
start local development server
```
$ docker exec -it laravel_sandbox_php bash
$ php artisan serve --host=0.0.0.0 --port=8000
```

## Features
### xdebug setting for VSCode

install [PHP Debug](https://marketplace.visualstudio.com/items?itemName=xdebug.php-debug)

/.vscode/launch.json
```
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Listen for Xdebug",
            "type": "php",
            "request": "launch",
            "port": 9003,
            "pathMappings": {
                "/var/www/html/": "${workspaceRoot}/"
            }
        },
    ]
}
```
Referens  
launch.json attribute  
https://code.visualstudio.com/docs/editor/debugging#_launchjson-attributes  
about pathMappings  
https://marketplace.visualstudio.com/items?itemName=xdebug.php-debug  

/php.ini  
https://xdebug.org/docs/all_settings
#### Usage
1. Ctrl+Shift+D
2. ▶︎(RUN) 「Listen for Xdebug」 selection
3. Set a breakpoint on any line
4. Shift+F5 debag start

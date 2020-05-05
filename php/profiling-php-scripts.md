# Profiling PHP Script

Run a PHP script with profiler enabled

```
php -d xdebug.profiler_enable=1 -d xdebug.profiler_output_dir=/tmp my-script.php
```

Use [Webgrind](https://github.com/jokkedk/webgrind) for analyzing the output files. In my case:

```
cd ~/apps/webgrind
php -S localhost:8080 index.php
```
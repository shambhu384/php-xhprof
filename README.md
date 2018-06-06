# php-xhprof

$ git clone https://github.com/tideways/php-profiler-extension.git

$ cd php-profiler-extension

$ phpize

$ ./configure

$ make

$ sudo make install

$ mkdir /tmp/xhprof

$ sudo chmod -R 0777 /tmp/xhprof


// enable xhprof in you app
tideways_xhprof_enable();

// load your application


$data = tideways_xhprof_disable();
file_put_contents(
    sys_get_temp_dir() . "/xhprof" . time() . ".yourapp.xhprof",
    serialize($data)
);

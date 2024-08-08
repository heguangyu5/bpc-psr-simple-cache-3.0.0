libpsr-simplecache.so:
	rm -rf SimpleCache
	mkdir SimpleCache
	phptobpc ../src/CacheException.php > SimpleCache/CacheException.php
	phptobpc ../src/CacheInterface.php > SimpleCache/CacheInterface.php
	phptobpc ../src/InvalidArgumentException.php > SimpleCache/InvalidArgumentException.php
	bpc -v \
		-c bpc.conf  \
		-l psr-simplecache \
		placeholder-simplecache.php \
		SimpleCache/CacheException.php \
		SimpleCache/CacheInterface.php \
		SimpleCache/InvalidArgumentException.php

install-libpsr-simplecache:
	bpc -l psr-simplecache --install

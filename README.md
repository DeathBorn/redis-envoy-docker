docker-compose pull

docker-compose up


redis-cli -h 127.0.0.1 -p 1999 set foo foo
# OK
redis-cli -h 127.0.0.1 -p 1999 set bar bar
# OK
redis-cli -h 127.0.0.1 -p 1999 get foo
# "foo"
redis-cli -h 127.0.0.1 -p 1999 get bar
# "bar"




# OK

# OK
redis-cli -h 127.0.0.1 -p 1999 get foo
# "foo"
redis-cli -h 127.0.0.1 -p 1999 get bar
# "bar"

redis-cli -h 127.0.0.1 -p 1999 set foo foo
redis-cli -h 127.0.0.1 -p 6379 get foo
redis-cli -h 127.0.0.1 -p 6380 get foo
redis-cli -h 127.0.0.1 -p 6381 get foo


redis-cli -h 127.0.0.1 -p 1999 set bar bar
redis-cli -h 127.0.0.1 -p 6379 get bar
redis-cli -h 127.0.0.1 -p 6380 get bar
redis-cli -h 127.0.0.1 -p 6381 get bar



needs optimizations
sysctls:
      net.core.somaxconn: 1024


huge pages directory on host
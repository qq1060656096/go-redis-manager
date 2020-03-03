# go-redis-driver

```go
import "github.com/qq1060656096/go-redis-driver"

redisDriver := NewDriver()
redisDriver.Add("test1", &redis.Options{
	Addr:     "localhost:6379",
	Password: "123456", // no password set
	DB:       1,        // use default DB
})
redisDriver.Add("test2", &redis.Options{
	Addr:     "localhost:6379",
	Password: "123456", // no password set
	DB:       2,        // use default DB
})

redisClient := redisDriver.Get("test1").GetRedisClient().Set("test1.key1", "test1.value1", 0).Err()
```
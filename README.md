# rosgotest
Experiments with rosgo (golang ROS client)
https://github.com/akio/rosgo

To regenerate msg: 
```
~/go/src/rosgotest$ go generate
```

Do not forget to start master: 
```
$ roscore
```

### Test Subscriber

Run subscriber: 
```
~/go/src/rosgotest$ go run subscriber.go

```
And try to publish something:
```
$ rostopic pub -r 2 /chatter std_msgs/String "data: 'test msg2'"
```

### Test Publisher
Run publisher: 
```
~/go/src/rosgotest$ go run publisher.go

```
And try to listen:
```
$ rostopic echo /chatter
```

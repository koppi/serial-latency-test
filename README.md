[![Build Status](https://travis-ci.org/koppi/serial-latency-test.png?branch=master)](https://travis-ci.org/koppi/serial-latency-test)

serial-latency-test measures the roundtrip time of packets sent over
the serial port. It calculates the worst case roundtrip time of all
sent packets and displays a histogram of the rountrip time jitter.

### demo

[![youtube](http://img.youtube.com/vi/2HOwFQcZfV4/0.jpg)](http://www.youtube.com/watch?v=2HOwFQcZfV4)

### usage

```
$ serial-latency-test -h
Usage: serial-latency-test -p <port> ...

  -p, --port=port    serial port to run tests on
  -b, --baud=baud    baud rate (default: 9600)
  -R, --realtime     use realtime scheduling (default: no)
  -P, --priority=n   scheduling priority, use with -R
                     (default: 99)

  -S, --samples=n    to take for the measurement (default: 10000)
  -c, --count=n      number of bytes to send per sample (default: 1)
  -w, --wait=ms      time interval between measurements (default: 0)
  -r, --random-wait  use random interval between wait and 2*wait

  -a, --async        set ASYNC_LOW_LATENCY flag (default: no)
  -x  --xmit=n       set xmit_fifo_size to given number (default: 0)
  -o, --output=file  write the output to file

  -h, --help         this help
  -V, --version      print current version
```

### related utilities

* https://github.com/cbrake/linux-serial-test


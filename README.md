# Simple test sample

The code in hello.go intentionally does not return the expected value for the test in order for it to fail.

## Usage

1. Clone this repository

``` bash
$ git clone https://github.com/jeastman19/golang-simple-test-sample.git
```

2. Enter the project folder

``` bash
$ cd golang-simple-test-sample
```

3. Run the test

``` bash
$ go test
    hello_test.go:9: Response from getName is unexpected value
FAIL
exit status 1
FAIL    _<path to project>/golang-simple-test-sample 0.003s
```

4. Modify the getName () function in the hello.go file, which should now appear as follows:

``` go
func getName () string {
    return "World"
}
```

to appear like this

``` go
func getName () string {
    return "World!"
}
```

note that the question mark was added at the end of the word World on the line

``` go
    return "World"
```

5. Now, run the test again, this time the test must pass

``` bash
$ go test
PASS
ok      _<path to project>/golang-simple-test-sample        0.002s
```

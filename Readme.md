





























# Letterbox.

A tiny Go program to batch-process letter-boxing of photographs.

## Installation

From [gobinaries.com](https://gobinaries.com):

```sh
$ curl -sf https://gobinaries.com/drylikov/Letterbox/cmd/Letterbox | sh
```

From source:

```
$ go get github.com/drylikov/Letterbox/cmd/Letterbox
```

## Usage

```
Usage of Letterbox:
  -aspect string
    	Output aspect ratio (default "16:9")
  -concurrency int
    	Concurrency of image processing (default 8)
  -force
    	Force image reprocess when it exists
  -output string
    	Image output directory (default "processed")
  -padding int
    	Output image padding in percentage
  -quality int
    	Output jpeg quality (default 90)
  -white
    	Output a white Letterbox
```

## Examples

Example of 1:1

```
$ Letterbox -aspect 1:1
```

![](https://apex-software.imgix.net/github/drylikov/Letterbox/1-1.jpg?w=500&dpr=2)

Example of 4:3

```
$ Letterbox -aspect 4:3
```

![](https://apex-software.imgix.net/github/drylikov/Letterbox/4-3.jpg?w=500&dpr=2)

Example of 16:9 (the default)

```
$ Letterbox -aspect 16:9
```

![](https://apex-software.imgix.net/github/drylikov/Letterbox/16-9.jpg?w=500&dpr=2)

Example of explicitly listing images:

```
$ Letterbox DSCF6719.jpg DSCF6718.jpg
```

![](https://apex-software.imgix.net/github/drylikov/Letterbox/16-9.jpg?w=500&dpr=2)

Example of 1:1 with a white background and 6% padding:

```
$ Letterbox -white -aspect 1:1 -padding 6
```

# GREP(Globally search a Regular Expression and Print) Examples

## regular expression

```sh
# 'bee'로 시작하는 bug들을 찾음
$ grep ^bee bugs
bees
beetles
# 세번째 글자가 'a'인 bug들을 찾음
$ grep ^..a bugs
roaches
grasshoppers
# 4개 숫자로 시작하는 모든 라인을 찾음
$ grep ^[0-9][0-9][0-9][0-9] textfile
2010
2013 is turning out to be a better year
12345 Taylor Avenue
# 위와 동일함. 다만 extended regexp(-E)를 사용함
$ grep -E "^[0-9]{4}" textfile
```

## output options

```sh
# print only the part of your pattern (--only-matching)
$ grep -o bee bugs
bee
bee
# pattern에 맞는 부분과 그 전과 후의 최고 40개의 문자만 프린트함
$ egrep -Rso '.{0,40}segmentation.{0,40}' instances_minival2014.json
# pattern에 맞는 부분과 그 이후 100개의 문자만 프린트함
$ egrep -Rso 'segmentation.{0,100}' instances_minival2014.json
```


## REF
- [](https://www.networkworld.com/article/2706756/big-data/groping-through-big-data-with-grep.html)

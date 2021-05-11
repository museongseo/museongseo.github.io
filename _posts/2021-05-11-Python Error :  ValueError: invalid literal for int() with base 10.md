---
layout: post
title: Python Error - ValueError : invalid literal for int() with base 10
tags: [error, python, jupyter]
image: 
---

# ValueError: invalid literal for int() with base 10: ''
------
오류 : Jupyter Notebook 에서 빠른 입출력을 위해 sys.stdin.readline() 구문을 사용했을 때, ValueError: invalid literal for int() with base 10: '' 와 같은 오류 발생.
해결법 : Jupyter Notebook 에서는 stdin/stdout 이 제대로 구성되어 있지 않다. 따라서 stdin.readline() 을 실행하면 입력을 받지 못하고 빈 문자열이 반환되기 때문에 int() 를 통해 10진수로 변환할 수 없다. stdin.readline() 대신 input() 을 사용해서 문제를 해결하고, 채점을 할 때만 빠른 수행 속도를 위해 stdin.readline() 으로 바꾸는 식으로 사용해야 할 것이다.

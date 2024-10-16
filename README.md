# SWE_2021_41_2024_2_week_6

---

## Week 4 Assignment
* ### [link of my repository](https://github.com/yunnniverse/SWE_2021_41_2024_2_week_4)

* ### my code
```python
def isHappy(n):
    arr = [False] * 2593  # 배열 초기화
    sum = 0

    while True:
        while n > 0:
            digit = n % 10  # 자리수 구하기
            sum += digit ** 2  # 자리수 제곱 더하기
            n //= 10  # n을 10으로 나눈 몫으로 갱신

        if sum == 1:  # 해피 넘버
            return True
        elif arr[sum] == True:  # 무한 루프 방지
            return False
        else:
            arr[sum] = True  # 체크된 수 저장

        n = sum  # n을 새로 구한 sum으로 갱신
        sum = 0  # sum 초기화

 n = int(input("Enter a number: "))  # 사용자로부터 숫자를 입력받음

# isHappy 함수 실행
if isHappy(n):
    print("True")
else:
    print("False")
 ```
* ### Explanation
 1. Repeatedly calculates the sum of the squares of the digits of the number.
 2. If the result is 1, it returns True, indicating the number is a happy number.
 3. If a previously encountered result reappears, it returns False to prevent an infinite loop.
 4. An array is used to store the calculated values, and if a value reappears, the loop stops.

---

## Week 5 Assignment

> ```bash
> docker exec aaa cat /etc/os-release
> ```
> * Checks the OS information inside the container aaa.
> * My output : "Ubuntu 24.04.1 LTS" ...

> ```bash
> docker exec aaa git --version
> ```
> * Checks the Git version inside the container aaa.
> * My output : git version 2.43.0

> ```bash
> docker exec aaa python3 --version
> ```
> * Checks the Python3 version inside the container aaa.
> * My output : Python 3.12.3

> ```bash
> docker inspect --format="{{ •HostConfig.Binds }}" aaa
> ```
> * Displays the host-to-container volume binding information for the container aaa.
> * My output : [/Users/yunni/ossp_hostdir:/mnt/ossp_container dir]

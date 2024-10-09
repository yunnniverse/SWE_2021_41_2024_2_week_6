# SWE_2021_41_2024_2_week_6

---

## Week 4 Assignment
> #### link of my repository
> https://github.com/yunnniverse/SWE_2021_41_2024_2_week_4


> ### my code
> ```python
>def isHappy(n):
>    arr = [False] * 2593  # 배열 초기화
>    sum = 0
>
>    while True:
>        while n > 0:
>            digit = n % 10  # 자리수 구하기
>            sum += digit ** 2  # 자리수 제곱 더하기
>            n //= 10  # n을 10으로 나눈 몫으로 갱신
>
>        if sum == 1:  # 해피 넘버
>            return True
>        elif arr[sum] == True:  # 무한 루프 방지
>            return False
>        else:
>            arr[sum] = True  # 체크된 수 저장
>
>        n = sum  # n을 새로 구한 sum으로 갱신
>        sum = 0  # sum 초기화
>
> n = int(input("Enter a number: "))  # 사용자로부터 숫자를 입력받음
>
># isHappy 함수 실행
>if isHappy(n):
>    print("True")
>else:
>    print("False")
> ```


---

## Week 5 Assignment


# 예제 5-1
```
#include <stdio.h>
int main(void)
{
	int x = 5;
	printf("x의 초기값은 %d이다.\n", x);

	x + 2;
	printf("문장 x+2는 문법에는 이상이 없으나 의미 없는 문장으로 경고가 발생한다.\n");

	// x + 3 = 5; // 오류발생 문장

	x = x + 2;
	printf("문장 x = x + 2; 이후의 x값은 %d이다.", x);

	printf("대입문도 평가값은 변수에 대입되는 값을 말하며\n");
	printf("x = x + 10의 평가값은 %d이다.\n", x = x + 10);
}
```

- 실행 결과
```
x의 초기값은 5이다.
문장 x+2는 문법에는 이상이 없으나 의미 없는 문장으로 경고가 발생한다.
문장 x = x + 2; 이후의 x값은 7이다.대입문도 평가값은 변수에 대입되는 값을 말하며
x = x + 10의 평가값은 17이다.
```

# 예제 5-2
```
#include <stdio.h>
int main(void)
{
	int x, y;

	printf("정수 1 입력> ");
	scanf_s("%d", &x);
	printf("정수 2 입력> ");
	scanf_s("%d", &y);
	printf("\n");

	printf("%d + %d는 %d입니다.\n", x, y, x + y);
	printf("%d - %d는 %d입니다.\n", x, y, x - y);
	printf("%d * %d는 %d입니다\n", x, y, x * y);
	printf("%d / %d는 %d입니다.\n", x, y, x / y);
	printf("%d %% %d는 %d입니다.\n", x, y, x % y);

	return 0;
}
```

- 실행 결
```
정수 1 입력> 59
정수 2 입력> 7

59 + 7는 66입니다.
59 - 7는 52입니다.
59 * 7는 413입니다
59 / 7는 8입니다.
59 % 7는 3입니다.
```

# 예제 5-3
```
#include <stdio.h>

int main(void)
{
	int m, n;
	printf("두 정수를 입력하세요. ");
	scanf_s("%d %d", &m, &n);

	printf("입력한 두 정수 %d, %d를비교하면 \n", m, n);
	printf("\t(%d > %d) 의 관계 연산 결과는 %d입니다\n", m, n, m>n);
	printf("\t(%d < %d) 의 관계 연산 결과는 %d입니다\n", m, n, m < n);
	printf("\t(%d >= %d)의 관계 연산 결과는 %d입니다\n", m, n, m >= n);
	printf("\t(%d <= %d)의 관계 연산 결과는 %d입니다\n", m, n, m <= n);
	printf("\t(%d == %d)의 관계 연산 결과는 %d입니다\n", m, n, m == n);
	printf("\t(%d != %d)의 관계 연산 결과는 %d입니다\n", m, n, m != n);

	return 0;
}
```

- 실행 결과
```
두 정수를 입력하세요. 38 4
입력한 두 정수 38, 4를비교하면
        (38 > 4) 의 관계 연산 결과는 1입니다
        (38 < 4) 의 관계 연산 결과는 0입니다
        (38 >= 4)의 관계 연산 결과는 1입니다
        (38 <= 4)의 관계 연산 결과는 0입니다
        (38 == 4)의 관계 연산 결과는 0입니다
        (38 != 4)의 관계 연산 결과는 1입니다
```

# 예제 5-4
```
#include <stdio.h>

int main(void)
{
	int a = 10;
	a++; // a = a+1
	printf("%d\n", a);

	a = 10;
	++a; // a = a+1;
	printf("%d\n\n", a);

	a = 10;
	printf("%d\n", a++);
	printf("%d\n", a);

	a = 10;
	printf("%d\n", ++a);
	printf("%d\n", a);


	return 0;
}
```

- 실행 결과과
```
11
11

10
11
11
11
```

# 예제 5-5
```
#include <stdio.h>
int main(void)
{
	int a = 5, b = 10, c = 15;

	printf("a = %d, b = %d, c = %d\n", a, b, c);
	printf("\t a + b++ - --c의 결과 = %5d\n\n", a + b++ - --c);

	printf("a = %d, b = %d, c = %d\n", a, b, c);
	printf("\t --a + ++b %% 3의 결과 = %5d\n\n", --a + ++b % 3);
	printf("a = %d, b = %d, c = %d\n", a, b, c);

	return 0;
}
```

- 실행 결과
```
a = 5, b = 10, c = 15
         a + b++ - --c의 결과 =     1

a = 5, b = 11, c = 14
         --a + ++b % 3의 결과 =     4

a = 4, b = 12, c = 14
```

# 예제 5-6

```
#include <stdio.h>
int main(void)
{
	printf("연산자 &&의 이용\n");
	printf("논리 연산 0 && 1 결과값은 %d\n", 0 && 1);
	printf("논리 연산 1.1 && 34.5 결과값은 %d\n", 1, 1 && 34.5);

	printf("연산자 ||의 이용\n");
	printf("논리 연산 0 || 1 결과값은 %d\n", 0 || 1);
	printf("논리 연산 0.3 || 0.2 결과값은 %d\n", 0.3 || 0.2);

	printf("연산자 !의 이용\n");
	printf("논리 연산 !NULL의 결과값은 %d\n", !NULL);
	printf("논리 연산 !3.4의 결과값은 %d\n", !3.4);
}
```

- 실행 결과
```
연산자 &&의 이용
논리 연산 0 && 1 결과값은 0
논리 연산 1.1 && 34.5 결과값은 1
연산자 ||의 이용
논리 연산 0 || 1 결과값은 1
논리 연산 0.3 || 0.2 결과값은 1
연산자 !의 이용
논리 연산 !NULL의 결과값은 1
논리 연산 !3.4의 결과값은 0
```


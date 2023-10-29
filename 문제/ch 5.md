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

# 예제 5-7
```
#include <stdio.h>
int main(void)
{
	int a = 10, b = 20, c = 3;
	printf("a = %d, b = %d, c = %d\n\n", a, b, c);
	// a = 10, b = 20, c = 3

	c = (a++ == 11) && (b++ == 20);
	printf("a = %d, b = %d, c = %d\n", a, b, c);
	// a = 11, b = 20, c = 0

	c = (a++ == 11) && (b++ == 21);
	printf("a = %d, b = %d, c = %d\n", a, b, c);
	// a = 12, b = 21, c = 0

	c = (a++ == 12) || (b++ == 21);
	printf("a = %d, b = %d, c = %d\n", a, b, c);
	// a = 13, b = 21, c = 1

	c = (a++ == 12) || (b++ == 22);
	printf("a = %d, b = %d, c = %d\n", a, b, c);
	// a = 14, b = 22, c = 0

	return 0;
}
```

- 실행 결과
```
a = 10, b = 20, c = 3

a = 11, b = 20, c = 0
a = 12, b = 21, c = 0
a = 13, b = 21, c = 1
a = 14, b = 22, c = 0
```

(1) && (2) -> (1)이 True 여야 (2) 실행. 그렇지 않으면 (1)만 실행 후 멈춤

(1) || (2) -> (1)이 True면 멈춤. 그렇지 않으면 (1) 실행 후 (2) 실행

(1) && (2) -> (1) True, (2) True : 1 / (1) False : 0

(1) || (2) -> (1) True : 1 / (1) False : 0


# 프로그래밍 실습 과제

1. 다음 식을 참고로 화씨 온도를 입력받아서 섭씨 온도로 변환하여 출력하는 프로그램을 작성하시오.
```
#include <stdio.h>
int main(void)
{
	double f;
	printf("화씨 온도를 입력하세요. ");
	scanf_s("%lf", &f);
	double c = 5 / 9. * (f - 32);
	printf("섭씨 온도는 %lf입니다.", c);
	return 0;
}
```
- 실행 결과
```
화씨 온도를 입력하세요. 100
섭씨 온도는 37.777778입니다.
```

2. 두 정수를 입력받아서 합과 평균을 구하여 출력하는 프로그램을 작성하시오. 단 평균은 실수로 출력되도록 한다.
```
#include <stdio.h>
int main(void)
{
	int a, b;
	printf("두 정수를 입력하시오. ");
	scanf_s("%d%d", &a, &b);
	double avg = (a + b) / 2.;
	printf("평균은 %lf입니다.", avg);
}
```

- 실행 결과
```
두 정수를 입력하시오. 1 2
평균은 1.500000입니다.
```

3. 표준입력으로 두 정수를 입력받아 큰 수를 작은 수로 나눈 몫과 나머지를 각각 출력하는 프로그램을 작성하시오.

```
#include <stdio.h>
int main(void)
{
	int a, b, remainder;
	printf("두 정수를 입력하시오. ");
	scanf_s("%d%d", &a, &b);
	if (a > b)
	{
		remainder = a % b;
	}
	else
	{
		remainder = b % a;
	}
	printf("%d", remainder);
	return 0;
}
```

- 실행 결과
```
두 정수를 입력하시오. 8 5
3
```

4. 원의 반지름 r을 입력받아 원의 면적과 둘레의 길이를 구하는 프로그램을 작성하시오.

```
#include <stdio.h>
int main(void)
{
	double r;
	printf("원의 반지름을 입력하시오. ");
	scanf_s("%lf", &r);

	double area = 3.14 * r * r;
	double circumference = 2 * 3.14 * r;
	
	printf("원의 둘레는 %lf, 원의 면적은 %lf입니다.", circumference, area);
}
```

- 실행 결과
```
원의 반지름을 입력하시오. 5.5
원의 둘레는 34.540000, 원의 면적은 94.985000입니다.
```

5. 무게의 단위인 킬로그램(kg)을 소수로 입력받아 파운드(pound)로 계산하여 소수점 3자리까지 출력하는 프로그램을 작성하시오.
```
#include <stdio.h>
int main(void)
{
	double kg;
	printf("킬로그램(kg)를 입력하시오. ");
	scanf_s("%lf", &kg);

	double pound = kg / 0.453592;

	printf("%lf킬로그램은 %.3lf파운드입니다.\n", kg, pound);
	return  0;
}
```

- 실행 결과과
```
킬로그램(kg)를 입력하시오. 60
60.000000킬로그램은 132.277파운드입니다.
```


6. 길이의 단위인 센티미터(cm)를 소수로 입력받아 피트(feet)로 계산하여 소수점 3자리까지 출력하는 프로그램을 작성하시오.
```
#include <stdio.h>
int main(void)
{
	double cm;
	printf("센티미터(cm)를 입력하시오. ");
	scanf_s("%lf", &cm);

	double feet = cm / 30.48;

	printf("%lfcm는 %.3lffeet입니다.\n", cm, feet);
	return  0;
}
```

- 실행 결과
```
센티미터(cm)를 입력하시오. 56
56.000000cm는 1.837feet입니다.
```

7. 정수 천만 이하의 하나의 수를 입력받아 우리가 사용한느 단위인 만, 천, 백, 십, 일 단위로 출력하는 프로그램을 작성하시오.

```
#include <stdio.h>
int main(void)
{
	int num, remainder;
	printf("천 만 이하 정수를 입력하시오 ");
	scanf_s("%d", &num);
	int million = num / 10000;
	remainder = num % 10000;

	int thousand = remainder / 1000;
	remainder = num % 1000;

	int hundred = remainder / 100;
	remainder = num % 100;

	int ten = remainder / 10;
	remainder = num % 10;

	printf("%d만 %d천 %d백 %d십 %d입니다.\n", million, thousand, hundred, ten, remainder);

	return 0;
}
```

- 실행 결과
```
천 만 이하 정수를 입력하시오 2347653
234만 7천 6백 5십 3입니다.
```

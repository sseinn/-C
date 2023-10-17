## 내용 점검 문제

4번

A.

```
#define CUBE (x) x*x*x
int main(void)
{
	int result = CUBE(2 + 3);
	return 0;
}
```

매크로를 정의하는 경우 기호상수 이름 다음 ()를 쓸 때 띄어쓰기를 하면 안된다.


- 수정
```
#define CUBE(x) x*x*x
int main(void)
{
	int result = CUBE(2 + 3);
	return 0;
}
```

- 만약 CUBE(x)의 값이 125를 원한다면 다음과 같이 수정해야한다. 
```
#define CUBE(x) (x)*(x)*(x)
int main(void)
{
	int result = CUBE(2+3);
	return 0;
}
```

B.
```
#include <stdio.h>
{
	int salary = 0;
	printf("월급을 입력 => ");
	scanf_s("%d", salary);
	return 0;
}
```

int main() 함수를 작성하지 않았다

- 수정
```
#include <stdio.h>
int main(void)
{
	int salary = 0;
	printf("월급을 입력 => ");
	scanf_s("%d", salary);
	return 0;
}
```

C.
```
#include "stdio.h"
int main(void)
{
	float degree = 0;
	printf("현재 온도를 입력(소수로)==> ");
	scanf_s("%lf", &degree);
	printf("현재의 온도는 %d입니다.\n", degree);
	return 0;
}
```

printf()에서 degree는 실수인데 정수형 서식문자 %d를 사용해서 출력하고 있다.

- 수정 : float 형 서식문자 %f로 바꿔서 출력한다.
```
#include "stdio.h"
int main(void)
{
	float degree = 0;
	printf("현재 온도를 입력(소수로)==> ");
	scanf_s("%f", &degree);
	printf("현재의 온도는 %f입니다.\n", degree);
	return 0;
}
```

D.
```
#include <stdio.h>
int main(void)
{
	int age = 20;
	printf("현재 나이는 %d 입니다.\n", age);
	return 0;
}
```

오류가 없다. 


## 프로그래밍 실습 과제

1. 정수 87을 적당한 변수에 저장하여 8진수와 십진수, 16진수로 출력하는 프로그램을 작성하시오.
```
#include <stdio.h>
int main(void)
{
	int a = 87;
	printf("%x %d %o", a, a, a);
}
```



- 실행 결과
```
57 87 127
```

2. 하나의 정수를 입력 받아 적당한 변수에 저장하여 8진수와 십진수, 16진수로 출력하는 프로그램을 작성하시오.

```
#include <stdio.h>
int main(void)
{
	int a;
	scanf_s("%d", &a);
	printf("%x %d %o", a, a, a);
}
```

- 실행 결과
```
65
41 65 101
```


3. 하나의 정수를 8진수로 인식하여 입력 받아(%o를 이용) 적당한 변수에 저장하여 8진수와 십진수, 16진수로 출력하는 프로그램을 작성하시오.

```
#include <stdio.h>
int main(void)
{
	int a;
	scanf_s("%o", &a);
	printf("%x %d %o", a, a, a);
}
```

- 실행 결과
```
10
8 8 10
```

4. 0부터 15까지 8진수, 십진수, 16진수로 다음과 같이 출력하는 프로그램을 작성하시오.

```
#include <stdio.h>
int main(void)
{
	int i;
	printf("\t8진수\t10진수\t16진수\n");

	for (i = 0; i < 16; i++)
		printf("\t%o\t%d\t%x\n", i, i, i);
}
```

- 실행 결과
```
        8진수   10진수  16진수
        0       0       0
        1       1       1
        2       2       2
        3       3       3
        4       4       4
        5       5       5
        6       6       6
        7       7       7
        10      8       8
        11      9       9
        12      10      a
        13      11      b
        14      12      c
        15      13      d
        16      14      e
        17      15      f
```

5. 표준 입력으로 두 개의 정수를 16진수(%x를 이용)로 입력 받아 두 수의 합을 다시 십진수로 출력하는 프로그램을 작성하시오.

```
#include <stdio.h>
int main(void)
{
	int a, b;
	scanf_s("%x %x", &a, &b);
	printf("%d", a + b);
}
```

- 실행 결과
```
13 15
40
```


6. 표준 입력으로 두 개의 정수를 16진수(%x를 이용)로 입력 받아 두 수의 합을 다시 십진수로 출력하는 프로그램을 작성하시오.
```
#include <stdio.h>
int main(void)
{
	int a, b;
	scanf_s("%x %x", &a, &b);
	printf("%d", a * b);
}
```


- 실행 결과
```
13 15
399
```

7. 두 수를 나누는 매크로 DIV(x, y)를 적당히 정의하여 표준 입력으로 두 개의 실수를 입력 받아 나누기의 결과를 출력하는 프로그램을 작성하시오.

```
#include <stdio.h>
#define DIV(x, y) ((x) / (y))
int main(void)
{
	int a, b;
	scanf_s("%d %d", &a, &b);
	printf("%d", DIV((a), (b)));
}
```

- 실행 결과
```
4 2
2
```

8. 다음과 같이 자료형 double인 원의 반지름을 입력 받아, 원의 둘레와 원의 면적을 구하는 프로그램을 다음 조건에 맞도록 작성하시오.


- 헤더파일 circle.h는 매크로와 출력을 위한 시스템 헤더 파일을 첨가하는 소스로 구성한다.

  1) 원주율 3.14를 PHI 정의하자
 
  2) 매크로 CIRCUM(x)는 인자 x가 반지름인 원에서 원의 둘레를 구하는 매크로를 정의한다.
 
  3) 매크로 AREA(x)는 인자 x가 반지름인 원에서 원의 면적을 구하는 매크로를 정의한다.
 
- 소스파일 circle.h에서는 double형 반지름을 표준 입력으로 입력 받아 위의 결과를 출력한다.

  4) 반지름은 표준입력으로 저장한다.
 
  5) 반지름과 원의 둘레(매크로 CIRCUM(x) 이용)를 출력한다.
 
  6) 반지름과 원의 면적(매크로 AREA(x) 이용)을 출력한다.

```
#define PHI 3.14
#define CIRCUM(x) (2 * PHI * (x))
#define AREA(x) (2 * PHI * (x) * (x))
```

```
#include <stdio.h>
#include "circle.h"
int main(void)
{
	double r;
	printf("반지름을 입력하시오 : ");
	scanf_s("%lf", &r);
	printf("원의 둘레 : %lf\n", CIRCUM(r));
	printf("원의 면적 : %lf\n", AREA(r));

	return 0;
}
```


- 실행 결과
```
반지름을 입력하시오 : 2.4
원의 둘레 : 15.072000
원의 면적 : 36.172800
```





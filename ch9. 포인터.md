# p.236 예제

```
#include <stdio.h>

int main(void)
{
	int a;
	double b;
	char c;

	printf("int형 변수의 주소 : %u\n", &a); //주소 연산자로 주소 계산
	printf("double형 변수의 주소 : %u\n", &b);
	printf("char형 변수의 주소 %u", &c);

	return 0;
}
```


- 출력 결과
```
  int형 변수의 주소 : 13630532
  double형 변수의 주소 : 13630568
  char형 변수의 주소 13630596
```

# p.238 예제

```
#include <stdio.h>

int main(void)
{
	int a;
	int *pa;

	pa = & a;
	*pa = 10;

	printf("포인터로 a 값 출력 : %d\n", *pa);
	printf("변수명으로 a 값 출력 : %d\n", a);

	return 0;
}
```


- 출력 결과
  
```
  포인터로 a 값 출력 : 10
  변수명으로 a 값 출력 : 10
```

# p.241 예제

```
#include <stdio.h>

int main(void)
{
	int a = 10, b = 15, total;
	double avg;
	int* pa, * pb;
	int* pt = &total;
	double* pg = &avg;

	pa = &a;
	pb = &b;

	*pt = *pa + *pb;
	*pg = *pt / 2.0;

	printf("두 정수의 값 : %d, %d\n", *pa, *pb);
	printf("두 정수의 합 : %d\n", *pt);
	printf("두 정수의 평균 : %.1lf\n", *pg);
	return 0;
}
```


- 출력 결과

```
두 정수의 값 : 10, 15
두 정수의 합 : 25
두 정수의 평균 : 12.5
```

# p.244 예제

```
#include <stdio.h>

int main(void)
{
	int a = 10, b = 20;
	const int* pa = &a;

	printf("변수 a 값 : %d\n", *pa);
	pa = &b;
	printf("변수 b 값 : %d\n", *pa);
	pa = &a;
	a = 20;
	printf("변수 a 값 : %d\n", *pa);

	return 0;
}
```


- 출력 결과

```
  변수 a 값 : 10
  변수 b 값 : 20
  변수 a 값 : 20
```

# 요약


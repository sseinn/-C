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

```
- 출력 결과

  int형 변수의 주소 : 13630532

  double형 변수의 주소 : 13630568

  char형 변수의 주소 13630596
```

# p.238 예

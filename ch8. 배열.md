# p.209 예제  

```
#include <stdio.h>

int main(void)
{
	int ary[5];

	ary[0] = 10;
	ary[1] = 20;
	ary[2] = ary[0] + ary[1];
	scanf_s("%d", &ary[3]);

	printf("%d\n", ary[2]);
	printf("%d\n", ary[3]);
	printf("%d\n", ary[4]); // 마지막 배열 요소는 쓰레기 

	return 0;
}
```

```
- 출력 결과

  50
  30
  50
  -858993460
```

# p. 215 예제 

```
#include <stdio.h>

int main(void)
{
	int score[5];
	int i;
	int total = 0;
	double avg;

	for (i = 0; i < 5; i++)
	{
		scanf_s("%d", &score[i]);
	}

	for (i = 0; i < 5; i++)
	{
		total += score[i];
	}
	avg = total / 5.0;
	}
```

```
- 출력 결과

80 95 77 84 100
   80   95   77   84  100
평균 : 87.2
```

# p.216 예제 

```
#include <stdio.h>

int main(void)
{
	int score[5];
	int i;
	int total = 0;
	double avg;
	int count;

	count = sizeof(score) / sizeof(score[0]); // 배열 요소의 개수 계산

	for (i = 0; i < count; i++)
	{
		scanf_s("%d", &score[i]);
	}
	
	for (i = 0; i < count; i++)
	{
		total += score[i];
	}
	avg = total / (double)count;

	for (i = 0; i < count; i++)
	{
		printf("%5d", score[i]);
	}
	printf("\n");

	printf("평균 : %.1lf\n", avg);

	return 0;
}
```

```
- 출력 결과

80 95 77 84 100
   80   95   77   84  100
평균 : 87.2
```

# p.219 3번 문제

```
#include <stdio.h>

int main(void)
{
	int A[3] = { 1, 2, 3 };
	int B[10];
	int i;

	for (i = 0; i < 10; i++)
	{
		B[i] = A[i%3];
	}
	
	for (i = 0; i < 10; i++)
	{
		printf("%5d ", B[i]);
	}
}
```

```
- 출력 결과

      1     2     3     1     2     3     1     2     3     1
```



# 요약

- 배열을 선언하면 많은 변수를 한 번에 선언하는 효과를 볼 수 있다.

- 배열을 초기화할 때는 중괄호{}를 사용한다.

- 배열은 주로 반복문으로 처리한다.

- 배열 전체의 크기를 구할 때 sizeof 연산자를 사용한다

- sizeof 연산자를 활용한 배열 처리

  **sizeof(배열명) / sizeof(배열 요소)**

  **p.216 예제**에서

  ```
  count = sizeof(score) / sizeof(score[0]);
  ```

  count : 배열 요소의 개수(5)

  sizeof(score) : 배열 전체 크기(20바이트) (int형 count 4바이트 X int형 배열 score 5개 = 20)

  sizeof(score[0]) : 배열 요소 하나의 크기(4바이트)

  

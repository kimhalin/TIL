## 1. 데이터 조회 방법

Pandas에서는 `loc` 또는 `iloc` 을 이용해 데이터를 조회한다. 아래와 같이 다양한 방법으로 행 또는 열 데이터에 접근할 수 있다.

![loc&iloc](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0678bdef-7ab0-469c-8fca-324eeb9977c1/Untitled.png)

### - 조건으로 조회

In

```python
df['디스플레이'] > 5
df.loc[df['디스플레이'] > 5]
```

Out

```python
iPhone 7    False
iPhone 8     True
...
iPhone X     True
```

Input에서 윗줄 코드를 실행시키면, 이렇게 ‘디스플레이’에 해당되는 값이 5보다 큰지 작은지를 판단해 각 행마다 `True` 또는 `False` 를 반환해준다. 

그래서 `df.loc[df['디스플레이'] > 5]` 을 실행시키면, 이 코드는 즉, df.loc[디스플레이 > 5가 True인 행] 이므로 `True` 가 나왔던 행들을 전체 출력해준다.

# Pandas

- [데이터 조회 방법](#데이터-조회-방법)
[조건으로-조회](#--조건으로-조회)

- [데이터 시각화하기](#데이터-시각화하기)


## 데이터 조회 방법

Pandas에서는 `loc` 또는 `iloc` 을 이용해 데이터를 조회한다. 아래와 같이 다양한 방법으로 행 또는 열 데이터에 접근할 수 있다.

![image](https://user-images.githubusercontent.com/75435113/157443952-127bc988-ce7b-43a8-a3de-1acd360a162d.png)

![image](https://user-images.githubusercontent.com/75435113/157444075-8f63be82-4ea1-4eb0-b60c-3f4703cdf5c9.png)

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

## 데이터 시각화하기

### Plot

`plot` 은 Pandas의 시리즈나 데이터프레임이 가지고 있는 메서드이다. `matplotlib` 를 내부에서 임포트하여 사용한다.

```python
시리즈 또는 데이터프레임.plot(kind='원하는 그래프 종류')
시리즈 또는 데이터프레임.plot(kind='원하는 그래프 종류', x='가로축', y='세로축')
```

위와 같은 코드를 사용해 데이터를 그래프로 시각화할 수 있다. 그래프 종류로는 ‘bar’, ‘pie’, ‘hist’, ‘kde’, ‘box’, ‘scatter’, ‘area’ 가 있다.

x와 y에 원하는 가로축과 세로축 데이터를 설정할 수 있다.

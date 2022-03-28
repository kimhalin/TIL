## 브라우저의 내용과 크롤링의 내용이 다를 때

Python으로 웹 스크래퍼를 클론 코딩하던 중, 검색 결과의 페이지 수를 알아내는 코드를 작성하고 결과를 확인하고 있었는데, 내 코드의 결과가 강의와 다르게 나왔다. 

> 분명 사이트에서는 3페이지까지 있었는데.. 갑자기 17페이지??? 왜 브라우저에서 응답받는 값과 request 모듈로 응답받는 값이 다르지?
> 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/475b4929-9799-4f59-aefb-6bd60554de9d/Untitled.png)

이렇게 나와야 할 것을 page 1 of 17, page 2 of 17, page 17 of 17.. 이렇게 순서도 뒤죽박죽 나왔다. 

강의의 Q&A를 살펴보니, 

자신이 쓰는 브라우저의 정보를 전달해주어야 지금 현재 보고 있는 것처럼 정보를 얻을 수 있다는 것!!

### 해결: requests get 함수에 인자로, headers 넘겨주기(User-Agent)

```python
result = requests.get(URL, headers=HEADER)
```

위처럼 get함수를 호출할 때, URL과 함께 headers 값을 따로 전달해주어야 한다. 그랬더니 문제 해결!

참고로 이 사이트를 통해 자신의 User-Agent를 알 수 있다. [https://www.whatismybrowser.com/detect/what-is-my-user-agent](https://www.whatismybrowser.com/detect/what-is-my-user-agent)

## A

저번주부터 감을 잡는데에 오랜 시간을 보냈다.

두줄이면 충분한데 거의 한시간을 고민한 것 같다.

numpy로 구현해서 pandas로 옮기는 과정에서 열 이름이 아래로 내려가서

처음부터 pandas로 구현하니 드디어 할수 있었다.

---
## B

여기도 거의 한 시간을 쓴 것 같다.

datetime 함수를 제대로 쓰는 방법을 몰라서 숫자형 데이터에도 함수를 적용해서

오류를 고치는 데에 시간을 많이 보냈다.

`df['Date'] = pd.to_datetime(df['Date'])`

`df['Date'] = pd.to_datetime(df['Close'])`

두번째는 해서는 안되는 함수였는데 해야 하는 것처럼 생각해서 계속 고민하다가

나중에 이미 숫자형 데이터에 datetime을 쓸 필요가 없다는 것을 알고 지웠다.

함수 쓰는 법을 다시 배우고 부등호로 원하는 시간대의 데이터만 뽑아서

그래프를 구현하니 별 문제 없이 되었다.

---
## C

여기부터는 그렇게 오랜 시간을 쓰지는 않았다.

감을 잡은 것 같다.

B에서 뽑은 데이터에 min, max 함수를 적용해 

원하는 데이터를 잘 뽑아냈다.

---
## D

그룹화 하는 과정이 생소해서 시간을 좀더 썼다.

구글링을 통해서 나에게 필요한 함수를 긁어와서 썼다.

`df_after_2021_views = df_after_2021.groupby(df_after_2021['Date'].dt.strftime('%Y-%m')).mean()`

워낙 길어서 알아보기 쉽지는 않았지만 중요한 것은 strftime은 시간 데이터에서 원하는 부분을 가져와 쓸수 있다는 것. 

그래프 구현은 B에서 했던 것처럼 하면 그렇게 어렵지 않았다.

---
## E

지금까지 해온 것들을 종합하면 그리 어렵지 않게 구현할 수 있었다.

2022년 이후의 데이터를 뽑아내서

그래프를 구현할 때 선을 3개로 만들면 되는 간단한 작업이었다.


## Djnago Project

#### Model 구현

```python
models.Model
```

- 클래스를 상속받아 Django Framework에서 사용할 모델 클래스를 구현 할 수 있다.
- 멤버 변수를 이용해 테이블으 ㅣ컬럼의 정의할 수 있다.

---

```python
models.Charfield
```

- 문자열 형태의 필드를 만들 때 사용
- max_length 는 문자열의 최대 길이를 의미하며 verbose_name 은 추후 admin 페이지에서 보여줄 문자열을 지정한다.

```python
models.DataTimeFeild
```

- 년,월,일,시간을 나타낼 때 사용

```
auto_now_add
```

- 따로 시간과 관련된 데이터가 추가되지 않으면 현재 시간 데이터가 추가되게끔 하는 옵션

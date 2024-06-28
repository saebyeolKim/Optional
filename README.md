# Optional&lt;T>

Optional&lt;T> 란 NullPointException 가 발생하지 않도록, 또한 null 일 수도 있는 값을 다루기 위한 다양한 메소드를 제공하는 Wrapper 클래스 </br></br>
기본사용법 </br>
```ruby
//변수가 null 일 경우 NPE(NullPointException) 예외 발생. 반드시 값이 있어야 하는 경우에 사용
Optional<String> optional = Optional.of(value);
```
```ruby
//변수가 null 일 수 있음. null 인 경우 Optional.empty() 리턴
Optional<String> optional = Optional.ofNullable(value);
```
```ruby
//빈 Optional 객체 생성
Optional<String> optional = Optional.empty();
```

Optional&lt;T> 개념 및 사용법 </br>
참고 </br>
https://hbase.tistory.com/212 </br>
https://jeongkyun-it.tistory.com/168 </br>
https://mangkyu.tistory.com/203 </br>
optional orelse orelseget 차이 ?




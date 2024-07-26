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
Optional&lt;T> 사용합수
```ruby
//Optional 안의 object가 null 인지 아닌지 체크하고 null 이 아닐 시 true 반환
public boolean isPresent()

//Optional 안의 값을 추출하고 null 이라면 에러를 반환
public T get()

//Optional이 null 이 아니라면 Optional 안의 값을 반환하고, null 이라면 other 로 공급된 값을 반환
public T ofElse(T other)

//Optional이 null이 아니라면 Optional 안의 값을 반환, null 이라면 supplier로 공급되는 값을 반환
public T orElseGet(Supplier<? extends T> supplier)

//Optional이 null이 아니라면 Optional 안의 값을 반환, null 이라면 exceptionSupplier로 공급되는 exception을 반환
public <X extends Throwable> T orElseThrow(
        Supplier<? extends X> exceptionSupplier) throws X
```

Optional&lt;T> 기본함수
```ruby
//Optional이 null 아니라면 actiona을 실행
public void ifPresent(Consumer<? super T> action)

//Optional이 null이 아니면 map에서 지정한 값 반환
public <U> Optional<U> map(Function<? super T, ? extends U> mapper)
```

📌 List<> 는 Optional 을 해줄 필요가 없다. return 값이 null 이 아니라 size() == 0 으로 오기 때문에
null 을 처리할 수 없기 때문이다.</br>
참고 </br>
https://hbase.tistory.com/212 </br>
https://jeongkyun-it.tistory.com/168 </br>
https://mangkyu.tistory.com/203 </br>
optional orelse orelseget 차이 ?




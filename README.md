##### ConversionService

+ 등록과 사용 분리
> 컨버터를 등록할 때는 StringToIntegerConverter 같은 타입 컨버터를 명확하게 알아야 한다.<br/>
  반면에 컨버터를 사용하는 입장에서는 타입 컨버터를 전혀 몰라도 된다.<br/>
  타입 컨버터들은 모두 컨버전 서비스 내부에 숨어서 제공된다.<br/>
   따라서 타입을 변환을 원하는 사용자는 컨버전 서비스 인터페이스에만 의존하면된다.<br/>
   물론 컨버전 서비스를 등록하는 부분과 사용하는 부분을 분리하고 의존관계 주입을 사용해야 한다.
   
+ 인터페이스 분리 원칙 (ISP)
  +  DefaultConversionService 는 다음 두 인터페이스를 구현했다.
      + ConversionService : 컨버터 사용에 초점
      + ConverterRegistry : 컨버터 등록에 초점

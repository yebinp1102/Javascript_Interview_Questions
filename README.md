<div align="center">
  <h2> [ 자바스크립트 면접 기출 문제 정리 ] </h2>
  <p style="color:gray">문제 클릭시 답변이 등장 합니다.</p>
</div>
<hr/>

<details>
  <summary>
    1. 이벤트 위임(event delegation)이란?
  </summary>
  <br/>
  <div>
    이벤트 위임은 주로 비슷한 방식으로 여러 요소에 이벤트를 할당하거나 핸들링 할 때 사용 됩니다. 이벤트 위임을 사용하면 요소마다 핸들러를 할당하지 않는 대신 요소의 공통 조상에만 이벤트 핸들러를 할당해도 여러 요소들을 핸들링 할 수 있습니다. 여러 요소에 이벤트를 할당하게 되면 메모리 점유율이 높아져 페이지 성능이 낮아진다는 단점이 있는데, 이벤트 핸들링을 이벤트 위임으로 구현하게 되면 문제를 해소할 수 있다는 장점이 있습니다.
  </div>
</details>
<br/>
<details>
  <summary>
    2. this 키워드에 대해 설명하시오.
  </summary>
  <br/>
  <div>
    객체의 메서드는 자신이 속한 객체의 프로퍼티를 참조하고 변경할 수 있어야 하는데, 이때 this를 통해 자신이 속한 객체 또는 자신이 생성할 인스턴스의 프로퍼티나 메서드를 참조할 수 있습니다. 구체적으로 this란 자신이 속한 객체 또는 자신이 생성할 인스턴스를 가리키는 자기 참조 변수 이며, this가 가리키는 값, 즉 this 바인딩은 함수 호출 방식에 의해 동적으로 결정 됩니다. <br/><br/>
    1. 객체 리터럴로 생성된 객체의 내부 this : 메서드를 호출한 객체가 바인딩 됩니다. <br/><br/>
    2. 생성자 함수로 생성된 객체 내부 this : 생성자 함수가 생성할 인스턴스가 바인딩 됩니다. <br/><br/>
    3. 전역에서 this와 일반 함수 내부의 this에는 window가 디폴트로 바인딩 되며, use strict 모드에서는 undefined가 바인딩 됩니다. <br/><br/>
    4. Function.prototype.apply/call 메서드에 의한 간접 호출시 this : apply와 call 메서드의 본질적인 기능은 함수를 호출하면서 인수로 전달한 객체를 해당 함수의 this에 바인딩 하므로, this에는 메서드의 인수로 전달한 특정 객체가 바인딩 됩니다. <br/><br/>
    5. Function.prototype.bind 메서드에 의한 간접 호출시 this : bind 메서드는 apply와 call 메서드와 달리 함수를 호출하지 않고 this로 사용할 객체만 전달하기 때문에 this에는 인수로 전달한 객체가 바인딩 됩니다.
    <br/><br/>
    <p>요약</p>
    <table border="1">
      <tr bgcolor="salmon">
        <td>함수 호출 방식</td>
        <td>this 바인딩</td>
      </tr>
      <tr>
        <td>일반 함수 호출</td>
        <td>전역 객체 window</td>
      </tr>
      <tr>
        <td>메서드 호출</td>
        <td>메서드를 호출 한 객체</td>
      </tr>
      <tr>
        <td>생성자 함수 호출</td>
        <td>생성자 함수가 미래에 생성할 인스턴스</td>
      </tr>
      <tr>
        <td>Function.prototype.apply/call/bind 메서드에 의한 간접 호출</td>
        <td>메서드의 첫번째 인수로 전달한 객체</td>
      </tr>
    </table>
  </div>
</details>
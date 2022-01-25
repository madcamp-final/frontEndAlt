<template>
  <div>
    <br/><br/><br/><br/><br/>
    <p class="title">첫충전시10만원무료지급</p>
    <button @click="bill()">충전 ㄱ?</button>
  </div>
</template>
<script>
export default {
  data() {
    return {
    };
  },
  methods: {
      bill(){
          var IMP  = window.IMP;
          IMP.init('imp49785554');
          var money = 10000;
          IMP.request_pay({
              pg: 'kakao',
              merchant_uid: 'merchant_' + new Date().getTime(),
              name: '정승네트워크',
              amount: money,
              buyer_email: 'awwsb41@gmail.com', 
              buyer_name: 'anan',
              buyer_tel: '010-0000-0000',
              buyer_addr: '대전광역시 유성구',
              buyer_postcode: '21667'
          }, function(rsp){
              console.log(rsp);
              if (rsp.success) {
                    alert("오");
                    var msg = '결제가 완료되었습니다.'; 
                    msg += '고유ID : ' + rsp.imp_uid;
                    msg += '상점 거래ID : ' + rsp.merchant_uid;
                    msg += '결제 금액 : ' + rsp.paid_amount;
                    msg += '카드 승인번호 : ' + rsp.apply_num;
                    $.ajax({
                        type: "GET", 
                        url: "http://54.180.160.3:8080/user/confirm-payments", //충전 금액값을 보낼 url 설정
                        data : {
                            'imp_uid': rsp.imp_uid,
                            'uid': "hell11o@gmail.com", //uid 쿠키에 저장 필요함!
                            'value': money
                        }
                    }).then((res)=>{
                        console.log(res);
                    });
              } else {
                  var msg = '결제에 실패하였습니다.';
                  msg += rsp.error_msg;
              }
              alert(msg);
          });
      },
  },
};
</script>
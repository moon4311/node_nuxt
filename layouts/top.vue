<template>
  <div>
    
<header>
		<!-- 공통영역 ::: Top -->
		<div class="_wrap">
      <div class="utilWrap">
        <div class="login_state">
          <div class="login_state_text">
            <strong>{userNm}님</strong>이 로그인 하셨습니다.
          </div>
        </div>

        <ul class="utilList">
          <li><a href="/vst/main.do">home</a></li>
          <li><a href="/cms/logout.do">logout</a></li>
          <li><a href="/cms/">admin</a></li>
        </ul>
      </div>
    </div>

  <div class="popAlert noticePop" style="display:none;">
    <h2>공지사항 알림</h2>
    <h3 id="popTitle" style="text-align: center; font-weight: bold;"></h3>
    <div id="popTime" class="popupArea">새로운 공지사항이 등록되었습니다</div>
    <div class="btnWrap">
      <input type="button" class="_btn _blue" onclick="goNotice()" value="확인">
      <input type="button" class="_btn _grey pop-close" value="닫기">
    </div>
    <a class="pop-close" href="#none">닫기</a>
  </div>
</header>
    <nuxt/>
  </div>
</template>
<script>
export default{
  
}
</script>
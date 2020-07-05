<template>
  <div>
		<!-- 공통영역 ::: Top -->
		<el-container>
  <el-header>
    <header>
        <div class="_wrap">
          <div class="utilWrap">
            <div class="login_state">
              <div class="login_state_text">
                <strong>{{userNm}}님</strong>이 로그인 하셨습니다.
              </div>
            </div>

            <ul class="utilList">
              <li><nuxt-link to="/vst/main.do">home</nuxt-link></li>
              <li><nuxt-link to="/cms/logout.do">logout</nuxt-link></li>
              <li><nuxt-link to="/cms/">admin</nuxt-link></li>
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

  </el-header>
  <el-container>
    <el-aside width="200px">
      <el-menu :default-openeds="['1', '2']" router>
        <el-submenu index="1">
          <template slot="title"><i class="el-icon-message"></i>회원관리</template>
            <el-menu-item index="1-1" route="mbr">회원관리</el-menu-item>
            <el-menu-item index="1-2" route="mbrtype">그룹관리</el-menu-item>
            <el-menu-item index="1-3" route="mbrtype/typeMenuMng">그룹별권한관리</el-menu-item>
          <!-- <el-submenu index="1-4">
            <template slot="title">Option4</template>
            <el-menu-item index="1-4-1">Option 4-1</el-menu-item>
          </el-submenu> -->
        </el-submenu>
        <el-submenu index="2">
          <template slot="title"><i class="el-icon-setting"></i>컴포넌트관리</template>
            <el-menu-item index="2-1">게시판 관리</el-menu-item>
            <el-menu-item index="2-2">배너관리</el-menu-item>
            <el-menu-item index="2-3">팝업관리</el-menu-item>
        </el-submenu>
        <el-submenu index="3">
          <template slot="title"><i class="el-icon-message"></i>메뉴관리</template>
            <el-menu-item index="3-1">회원관리</el-menu-item>
            <el-menu-item index="3-2">그룹관리</el-menu-item>
            <el-menu-item index="3-3">그룹별권한관리</el-menu-item>
        </el-submenu>
        <el-submenu index="4">
          <template slot="title"><i class="el-icon-message"></i>코드관리</template>
            <el-menu-item index="4-1">대분류관리</el-menu-item>
            <el-menu-item index="4-2">중분류관리</el-menu-item>
            <el-menu-item index="4-3">소분류관리</el-menu-item>
        </el-submenu>
      </el-menu>
    </el-aside>
    <el-main>
      <div class="content">
        <nuxt />
      </div>
    </el-main>
  </el-container>
</el-container>

  </div>
</template>
<script>
export default{
 layout: 'top',
 data (){
    return {userNm: 'ADMIN'}
  }
}
</script>
<style>
  .el-header, .el-footer {
    background-color: #B3C0D1;
    color: #333;
    text-align: center;
    line-height: 60px;
  }
  
  .el-aside {
    background-color: #D3DCE6;
    color: #333;
    text-align: center;
    line-height: 200px;
  }
  
  .el-main {
    background-color: #E9EEF3;
    color: #333;
    text-align: center;
    line-height: 160px;
  }
  
  body > .el-container {
    margin-bottom: 40px;
  }
  
  .el-container:nth-child(5) .el-aside,
  .el-container:nth-child(6) .el-aside {
    line-height: 260px;
  }
  
  .el-container:nth-child(7) .el-aside {
    line-height: 320px;
  }
</style>
# trjy17
web trjy17.com

<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html b:css='false' b:defaultwidgetversion='2' b:layoutsVersion='3' b:responsive='true' b:templateUrl='indie.xml' b:templateVersion='1.3.0' expr:dir='data:blog.languageDirection' expr:lang='data:blog.locale.language' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr'>
  <b:attr name='xmlns' value=''/>
  <b:attr name='xmlns:b' value=''/>
  <b:attr name='xmlns:expr' value=''/>
  <b:attr name='xmlns:data' value=''/>
  <b:attr cond='data:view.url == data:view.url params { amp: &quot;1&quot; }' name='amp' value='amp'/>
  

    
  <!--[ <head> Open ]-->
  &lt;head&gt;

  <b:if cond='data:view.isMultipleItems'>
    <b:if cond='data:view.isHomepage'>
      <!--[ Homepage title ]-->
      <title><data:blog.title.escaped/></title>
      <b:elseif cond='data:view.search.query'/>
      <!--[ Search title ]-->
      <title><data:messages.search/>: <data:view.search.query/></title>
      <b:elseif cond='data:view.search.label'/>
      <!--[ Label title ]-->
      <title><data:blog.pageName.escaped/> - <data:blog.title.escaped/></title>
      <b:elseif cond='data:view.isArchive'/>
      <!--[ Archive title ]-->
      <title>Blog archive in: <data:blog.pageName.escaped/></title>
      <b:else/>
      <title>Blog: <data:blog.title.escaped/></title>
    </b:if>
    <b:elseif cond='data:view.isError'/>
    <!--[ Error title ]-->
    <title>Error 404: Not Found</title>
    <b:else/>
    <!--[ SingleItem title ]-->
    <title><data:blog.pageName.escaped/> - <data:blog.title.escaped/></title>
  </b:if>

  <!--[ Meta for browser ]-->
  <meta charset='UTF-8'/>
  <meta content='width=device-width, initial-scale=1, user-scalable=1, minimum-scale=1, maximum-scale=5' name='viewport'/>
  <meta content='IE=edge' http-equiv='X-UA-Compatible'/>
  <meta content='max-image-preview:large' name='robots'/>

  <!-- Link Canonical -->
  <link expr:href='data:blog.url.canonical' rel='canonical'/>
  <!--<b:if cond='data:view.url == data:view.url params { amp: &quot;1&quot; }'>
    <link expr:href='data:view.url' rel='alternate'/>
    <b:else/>
    <link expr:href='data:view.url + &quot;?m=1&quot;' rel='alternate'/>
    <link expr:href='data:view.url params { amp: &quot;1&quot; }' rel='amphtml'/>
  </b:if>-->

  <b:if cond='!data:view.isError'>
    <!--[ Browser data, description and keyword ]-->
    <b:if cond='data:blog.metaDescription'>
      <meta expr:content='data:blog.metaDescription.escaped' name='description'/>
      <b:elseif cond='data:view.isSingleItem'/>
      <meta expr:content='data:post.snippet.escaped snippet { length: 147, links: false, linebreaks: false, ellipsis: false }' name='description'/>
      <b:else/>
      <meta expr:content='data:blog.pageName.escaped ? data:blog.pageName.escaped : data:blog.title' name='description'/>
    </b:if>
    <meta expr:content='data:blog.title.escaped + &quot;, &quot; + data:blog.pageName.escaped + &quot;, Keyword_1, Keyword_2, Keyword_3 &quot;' name='keywords'/>
    <b:tag cond='data:view.isPost' expr:href='resizeImage(data:blog.postImageUrl, 0)' name='link' rel='image_src'/>
  
    <!--[ Generator and rrs ]-->
    <meta content='blogger' name='generator'/>
    <link expr:href='data:blog.homepageUrl.canonical + &quot;feeds/posts/default&quot;' expr:title='data:blog.title + &quot; - Atom&quot;' rel='alternate' type='application/atom+xml'/>
    <link expr:href='data:blog.homepageUrl.canonical + &quot;feeds/posts/default?alt=rss&quot;' expr:title='data:blog.title + &quot; - Feed&quot;' rel='alternate' type='application/rss+xml'/>
    <link expr:href='data:blog.homepageUrl.canonical + &quot;feeds/comments/default?alt=rss&quot;' expr:title='data:blog.title + &quot; - Comments Feed&quot;' rel='alternate' type='application/rss+xml'/>
  
    <!--[ Theme Color ]-->
    <meta expr:content='data:skin.vars.themeColor' name='theme-color'/>
    <meta expr:content='data:skin.vars.themeColor' name='msapplication-navbutton-color'/>
    <meta expr:content='data:skin.vars.themeColor' name='apple-mobile-web-app-status-bar-style'/>
    <meta expr:content='yes' name='apple-mobile-web-app-capable'/>
  
    <!--[ Favicon ]-->
    <link expr:href='data:blog.blogspotFaviconUrl' rel='apple-touch-icon' sizes='120x120'/>
    <link expr:href='data:blog.blogspotFaviconUrl' rel='apple-touch-icon' sizes='152x152'/>
    <link expr:href='data:blog.blogspotFaviconUrl' rel='icon' type='image/x-icon'/>
    <link expr:href='data:blog.blogspotFaviconUrl' rel='shortcut icon' type='image/x-icon'/>
    
    <!--[ Open graph ]-->
    <meta expr:content='data:blog.pageName.escaped ? data:blog.pageName.escaped : data:blog.title.escaped' property='og:title'/>
    <meta expr:content='data:blog.canonicalUrl' property='og:url'/>
    <meta expr:content='data:blog.title.escaped' property='og:site_name'/>
    <b:if cond='data:view.isMultipleItems'>
      <meta content='website' property='og:type'/>
      <b:if cond='data:blog.metaDescription'>
        <meta expr:content='data:blog.metaDescription.escaped' property='og:description'/>         
        <b:else/>
        <meta expr:content='data:blog.pageName.escaped ? data:blog.pageName.escaped : data:blog.title' property='og:description'/>
      </b:if>
      <b:else/>
      <meta content='article' property='og:type'/>
      <b:if cond='data:blog.metaDescription'>
        <meta expr:content='data:blog.metaDescription.escaped' property='og:description'/>            
        <b:else/>
        <meta expr:content='data:post.snippet.escaped snippet { length: 147, links: false, linebreaks: false, ellipsis: false }' property='og:description'/>
      </b:if>
    </b:if>
    <meta expr:content='data:blog.pageName.escaped ? data:blog.pageName.escaped : data:blog.title.escaped' property='og:image:alt'/>
    <b:if cond='data:blog.postImageUrl'>
      <meta expr:content='resizeImage(data:blog.postImageUrl, 0)' property='og:image'/>
      <b:else/>
      <meta content='#' property='og:image'/>
    </b:if>
    
    <!--[ Twitter Card ]-->
    <meta expr:content='data:blog.pageName.escaped ? data:blog.pageName.escaped : data:blog.title.escaped' name='twitter:title'/>
    <meta expr:content='data:blog.canonicalUrl' name='twitter:url'/>
    <b:if cond='data:view.isMultipleItems'>
      <b:if cond='data:blog.metaDescription'>
        <meta expr:content='data:blog.metaDescription.escaped' name='twitter:description'/>         
        <b:else/>
        <meta expr:content='data:blog.pageName.escaped ? data:blog.pageName.escaped : data:blog.title' name='twitter:description'/>
      </b:if>
      <b:else/>
      <b:if cond='data:blog.metaDescription'>
        <meta expr:content='data:blog.metaDescription.escaped' name='twitter:description'/>            
        <b:else/>
        <meta expr:content='data:post.snippet.escaped snippet { length: 147, links: false, linebreaks: false, ellipsis: false }' name='twitter:description'/>
      </b:if>
    </b:if>
    <meta content='summary_large_image' name='twitter:card'/>
    <meta expr:content='data:blog.pageName.escaped ? data:blog.pageName.escaped : data:blog.title.escaped' name='twitter:image:alt'/>
    <b:if cond='data:blog.postImageUrl'>
      <meta expr:content='resizeImage(data:blog.postImageUrl, 0)' name='twitter:image:src'/>
      <b:else/>
      <meta content='#' name='twitter:image:src'/>
    </b:if>
  
    <!-- Sife Verification -->
    <meta content='' name='msvalidate.01'/>
    
  </b:if>
  
  <b:if cond='data:view.isLayoutMode'>
    <!--[ CSS Layout ]-->
    <b:template-skin><![CDATA[ body#layout::before{content:'Fletro Pro v6.1 Updated(October 25, 2021)';position:absolute;top:15px;right:15px;font-size:.8rem;font-family:Roboto, sans-serif;color:rgba(0,0,0,0.52)} body#layout{width:1025px;margin:0 !important;padding:60px 0 0 !important;border:0 !important;text-align:left !important;position:relative} body#layout div.layout-widget-description{font-size:12px !important;line-height:1.6em} body#layout div.layout-title{font-size:15px !important} body#layout div.section{border-radius:2px} body#layout .section h4{font-size:15px !important;margin-left:0!important} body#layout .add_widget a{font-size:13px !important} body#layout .Blog .widget-content{height:auto!important} body#layout #anchor-ad, body#layout #notif-widget .widget-content, body#layout #side-sticky, body#layout #HTML91 .widget-content, body#layout #HTML92 .widget-content, body#layout #HTML93 .widget-content, body#layout #HTML01 .widget-content, body#layout #HTML02 .widget-content, body#layout #HTML94 .widget-content{background:#f0f8ff !important} body#layout .mainIn{padding-bottom:30px} body#layout .headIn, body#layout .blogM, body#layout .fotIn{display:flex} body#layout .headL{width:30%} body#layout .headR, body#layout .headM{width:35%} body#layout .mainbar{width:55%} body#layout .sidebar{width:45%} body#layout header, body#layout .mainIn, body#layout footer, body#layout .erroP{border-top:1px solid #e5e5e5;padding:30px 0 30px;position:relative} body#layout header::before, body#layout .mainIn::before, body#layout footer::before, body#layout .erroP::before{content:'Header';position:absolute;top:-14px;left:20px;padding:5px 20px;border:1px solid #e5e5e5;border-radius:20px;font-size:.8rem;font-family:Roboto,sans-serif;color:rgba(0,0,0,0.52);background:#f1f1f1} body#layout #notif-widget{padding:0!important; margin-bottom:30px!important} body#layout #notif-widget .widget{margin-top:0!important} body#layout #notif-widget h4, body#layout #notif-widget .layout-widget-description{display:none !important} body#layout .mainIn, body#layout .erroP{margin-top:40px;padding-bottom:0} body#layout .mainIn::before{content:'Main Content'} body#layout footer::before{content:'Footer'} body#layout .erroP::before{content:'Custom Error Page'} ]]></b:template-skin>
  </b:if>

  <!--[ CSS stylesheet ]-->
  &lt;style&gt;&lt;!-- /* <b:skin version='1.3.0'><![CDATA[
/*
<Group description="Theme Color">
<Variable name="themeColor" description="Address bar color" type="color" default="#2e51a2" value="#2c7ef4"/>
</Group>

<Group description="Basic colors and Background">
<Variable name="head.color" description="Heading colors" type="color" default="#262d3d" value="#08102b"/>
<Variable name="body.color" description="Body colors" type="color" default="#48525c" value="#08102b"/>
<Variable name="body.colorAlt" description="Alternative body colors" type="color" default="#767676" value="#767676"/>
<Variable name="body.bgColor" description="Main page bakground color" type="color" default="#fffdfc" value="#fffdfc"/>
<Variable name="link.color" description="Link colors" type="color" default="#204ecf" value="#2c7ef4"/>
<Variable name="link.bgColor" description="Button link colors" type="color" default="#204ecf" value="#2c7ef4"/>
</Group>

<Group description="Icon colors">
<Variable name="icon.color" description="Icon colors" type="color" default="#48525c" value="#08102b"/>
<Variable name="icon.colorAlt" description="Alternative icon colors" type="color" default="#767676" value="#08102b"/>
<Variable name="icon.colorSec" description="Secondary icon colors" type="color" default="#767676" value="#767676"/>
</Group>

<Group description="Notification">
<Variable name="notif.height" description="Notification max height" type="length" max="60px" default="45px" value="53px"/>
<Variable name="notif.bg" description="Notification background color" type="color" default="#e1f5fe" value="#e8f0fe"/>
<Variable name="notif.color" description="Notification text color" type="color" default="#08102b" value="#3c4043"/>
<Variable name="notif.link" description="Notification link color" type="color" default="#204ecf" value="#2c7ef4"/>
</Group>

<Group description="Header colors, background and height">
<Variable name="header.height" description="Header height" type="length" max="80px" default="60px" value="72px"/>
<Variable name="header.heightM" description="Header height(mobile)" type="length" max="80px" default="60px" value="60px"/>
<Variable name="header.titleSize" description="Header title font size" type="length" max="20px" default="16px" value="16px"/>
<Variable name="header.text" description="Header text colors" type="color" default="#48525c" value="#08102b"/>
<Variable name="header.icon" description="Header icon colors" type="color" default="#262d3d" value="#08102b"/>
<Variable name="header.bgColor" description="Header background color" type="color" default="#fffdfc" value="#fffdfc"/>
<Variable name="header.border" description="Header border" type="length" max="1px" default="0px" value="1px"/>
</Group>

<Group description="Scroll menu background">
<Variable name="nav.bg" description="Navbar background color" type="color" default="#fffdfc" value="#fffdfc"/>
</Group>

<Group description="Searchbar colors">
<Variable name="search.icon" description="Searchbar icon color" type="color" default="#48525c" value="#08102b"/>
<Variable name="search.bg" description="Searchbar background color" type="color" default="#fffdfc" value="#fffdfc"/>
</Group>

<Group description="Content background">
<Variable name="content.bg" description="Content background color" type="color" default="#fffdfc" value="#fffdfc"/>
<Variable name="content.border" description="Content border color" type="color" default="#eceff1" value="#e6e6e6"/>
</Group>

<Group description="Content max width">
<Variable name="content.maxWidth" description="Max width of main content" type="length" max="1440px" default="1024px" value="1200px"/>
<Variable name="sidebar.maxWidth" description="Max width of sidebar" type="length" max="360px" default="300px" value="300px"/>
<Variable name="post.maxContent" description="Post max width" type="length" max="900px" default="720px" value="780px"/>
<Variable name="page.maxContent" description="Static page max width" type="length" max="900px" default="780px" value="780px"/>
</Group>

<Group description="Post font size">
<Variable name="post.titleSize" description="Post title font size" type="length" max="42px" default="28px" value="36px"/>
<Variable name="post.titleSizeMobile" description="Post title size (onMobile)" type="length" max="38px" default="22px" value="28px"/>
<Variable name="post.fontSize" description="Post font size (Default)" type="length" max="18px" default="16px" value="16px"/>
<Variable name="post.fontSizeMobile" description="Post font size (Default onMobile)" type="length" max="18px" default="16px" value="15px"/>
<Variable name="post.fontSizeS" description="Post font size (Small)" type="length" max="16px" default="14px" value="15px"/>
<Variable name="post.fontSizeSMobile" description="Post font size (Small onMobile)" type="length" max="16px" default="14px" value="14px"/>
<Variable name="post.fontSizeL" description="Post font size (Large)" type="length" max="20px" default="18px" value="17px"/>
<Variable name="post.fontSizeLMobile" description="Post font size (Large onMobile)" type="length" max="20px" default="18px" value="16px"/>
</Group>

<Group description="Widget title font size">
<Variable name="widget.titleSize" description="Widget title font size" type="length" max="18px" default="14px" value="15px"/>
<Variable name="widget.titleAfter" description="Widget title border" type="length" max="40px" default="25px" value="25px"/>
<Variable name="widget.titleAfterC" description="Widget title border color" type="color" default="#989b9f" value="#989b9f"/>
</Group>

<Group description="Mobile menu colors">
<Variable name="mob.border" description="Mobile menu border" type="length" max="2px" default="0px" value="0px"/>
<Variable name="mob.borderR" description="Mobile corder radius" type="length" max="20px" default="0px" value="0px"/>
<Variable name="mob.text" description="Mobile text colors" type="color" default="#48525c" value="#48525c"/>
<Variable name="mob.bg" description="Mobile background color" type="color" default="#fffdfc" value="#fffdfc"/>
<Variable name="mob.hovBg" description="Mobile hover background color" type="color" default="#f6f6f6" value="#f6f6f6"/>
</Group>

<Group description="Footer colors">
<Variable name="foot.border" description="Footer border" type="length" max="2px" default="0px" value="0px"/>
<Variable name="foot.text" description="Footer text colors" type="color" default="#48525c" value="#08102b"/>
<Variable name="foot.bg" description="Footer background color" type="color" default="#fffdfc" value="#f7f7f7"/>
</Group>

<Group description="Dark mode colors and background">
<Variable name="dark.text" description="Dark mode text color" type="color" default="#fffdfc" value="#fffdfc"/>
<Variable name="dark.textAlt" description="Alternative text colors" type="color" default="#989b9f" value="#989b9f"/>
<Variable name="dark.link" description="Dark mode link colors" type="color" default="#005af0" value="#2c7ef4"/>
<Variable name="dark.bg" description="Dark mode background color" type="color" default="#1e1e1e" value="#1e1e1e"/>
<Variable name="dark.bgAlt" description="Alternative background color" type="color" default="#2d2d30" value="#2d2d30"/>
<Variable name="dark.bgSec" description="Secondary background color" type="color" default="#252526" value="#252526"/>
</Group>

<Group description="(Do not edit) New Blogger comment required">
<Variable name="body.background" description="Background" color="#505050" type="background" default="$(color) none repeat scroll center center"  value="#505050 url() no-repeat scroll center center"/>
<Variable name="body.text.font" description="Font Blogger comment" type="font" default="&#39;Roboto&#39;, sans-serif" value="400 14px &#39;Roboto&#39;, sans-serif"/>
<Variable name="body.text.color" description="Color" type="color" default="#505050"  value="#505050"/>
<Variable name="body.link.color" description="Link color" type="color" default="#262d3d"  value="#989b9f"/>
<Variable name="posts.title.color" description="Post title color" type="color" default="#262d3d"  value="#989b9f"/>
<Variable name="posts.text.color" description="Post text color" type="color" default="#48525c"  value="#989b9f"/>
<Variable name="posts.icons.color" description="Post info color" type="color" default="#262d3d" value="#989b9f"/>
<Variable name="posts.background.color" description="Post background color" type="color" default="#f7f7fc"  value="transparent"/>
<Variable name="tabs.font" description="Font" type="font" default="&#39;Roboto&#39;, sans-serif" value="400 14px &#39;Roboto&#39;, sans-serif"/>
<Variable name="tabs.color" description="Text color" type="color" default="#4d4d4d"  value="#08102b"/>
<Variable name="tabs.selected.color" description="Selected color" type="color" default="#fff"  value="#fffdfc"/>
<Variable name="tabs.overflow.background.color" description="Popup background color" type="color" default="$(posts.background.color)"  value="#fffdfc"/>
<Variable name="tabs.overflow.color" description="Popup text color" type="color" default="#48525c"  value="#08102b"/>
<Variable name="tabs.overflow.selected.color" description="Popup selected color" type="color" default="#262d3d"  value="#989b9f"/>
<Variable name="labels.background.color" description="Labels background color" type="color" default="#fff" value="#fffdfc"/>
<Variable name="blog.title.font" description="Blog title font" type="font" default="&#39;Roboto&#39;, sans-serif" value="400 14px &#39;Roboto&#39;, sans-serif"/>
<Variable name="blog.title.color" description="Blog title color" type="color" default="#fff" value="#fffdfc"/>
</Group>
*/

/* Variable color */
:root{
--headC: $(head.color) ;
--bodyC: $(body.color) ;
--bodyCa: $(body.colorAlt) ;
--bodyB: $(body.bgColor) ;
--linkC: $(link.color) ;
--linkB: $(link.bgColor) ;

--iconC: $(icon.color) ;
--iconCa: $(icon.colorAlt) ;
--iconCs: $(icon.colorSec) ;

--headerC: $(header.text) ;
--headerT: $(header.titleSize) ;
--headerW: 700 ; /* write 400(normal) or 700(bold) */
--headerB: $(header.bgColor) ;
--headerL: $(header.border) ;
--headerI: $(header.icon) ;
--headerH: $(header.height) ;
--headerHi: -$(header.height) ;
--headerHm: $(header.heightM) ;

--notifH: $(notif.height) ;
--notifU: $(notif.bg) ;
--notifC: $(notif.color) ;
--notifL: $(notif.link) ;

--contentB: $(content.bg) ;
--contentL: $(content.border) ;
--contentW: $(content.maxWidth) ;
--sideW: $(sidebar.maxWidth) ;
--transB: rgba(0,0,0,.05);

--pageW: $(page.maxContent) ;
--postW: $(post.maxContent) ;
--postT: $(post.titleSize) ;
--postTm: $(post.titleSizeMobile) ;
--postF: $(post.fontSize) ;
--postFm: $(post.fontSizeMobile) ;
--postFS: $(post.fontSizeS) ;
--postFSm: $(post.fontSizeSMobile) ;
--postFL: $(post.fontSizeL) ;
--postFLm: $(post.fontSizeLMobile) ;

--widgetT: $(widget.titleSize) ;
--widgetTw: 700 ; /* write 400(normal) or 700(bold) */
--widgetTa: $(widget.titleAfter) ;
--widgetTac: $(widget.titleAfterC);

--navB: $(nav.bg) ;

--srchI: $(search.icon) ;
--srchB: $(search.bg) ;

--mobT: $(mob.text) ;
--mobHv: $(mob.hovBg) ;
--mobB: $(mob.bg) ;
--mobL: $(mob.border) ;
--mobBr: $(mob.borderR) ;

--fotT: $(foot.text) ;
--fotB: $(foot.bg) ;
--fotL: $(foot.border) ;

--fontH: 'Noto Sans', sans-serif ;
--fontB: 'Noto Sans', sans-serif ;
--fontBa: 'Noto Sans', sans-serif ;
--fontC: 'Fira Mono', monospace ;

--trans-1: all .1s ease ;
--trans-2: all .2s ease ;
--trans-4: all .4s ease ;

--synxBg: #f6f6f6 ;
--synxC: #2f3337 ;
--synxOrange: #b75501 ;
--synxBlue: #015692 ;
--synxGreen: #54790d ;
--synxRed: #f15a5a ;
--synxGray: #656e77 ;

--darkT: $(dark.text) ;
--darkTa: $(dark.textAlt) ;
--darkU: $(dark.link) ;
--darkB: $(dark.bg) ;
--darkBa: $(dark.bgAlt) ;
--darkBs: $(dark.bgSec) ;
}

/* ubah warna cari kode #f89000 dan %23f89000 */
.postTextRelated{position:relative;margin:42px 0;padding:1.5em 0;border:1px solid #eceff1;border-left:0;border-right:0; font-size:14px;line-height:1.8em;display:none}
.postTextRelated a{-webkit-tap-highlight-color:rgba(0,0,0,0);-webkit-tap-highlight-color:transparent}
.postTextRelated a:hover{opacity:.8}
.postTextRelated b{font-size:13px;font-weight:400;margin:0;padding:2px 14px;background-color:#fefefe;border:1px solid #e6e6e6;border-radius:15px; position:absolute;top:-15.5px;left:20px}
.postTextRelated ul{margin:8px 0 0;padding-left:20px}
.postTextRelated li:hover{margin-left:5px}
.postTextRelated li{background:url("data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24'><g transform='translate(12.000000, 12.000000) rotate(-90.000000) translate(-12.000000, -12.000000) translate(6.500000, 3.000000)'><line fill='none' stroke='%232c7ef4' x1='5.3939' y1='9.7001' x2='5.3939' y2='0.7501'></line><path fill='none' stroke='%232c7ef4' d='M5.3998,17.3539 C6.6558,17.3539 10.6708,10.9899 9.9488,10.2679 C9.2268,9.5459 1.6418,9.4769 0.8508,10.2679 C0.0598,11.0599 4.1448,17.3539 5.3998,17.3539 Z'></path></g></svg>") left / 20px no-repeat;list-style-type:none;padding:0 25px;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;color:#2c7ef4;transition:all .4s ease}

/* css darkmode sesuaikan class (.drK) */
.drK .postTextRelated b{background-color:#1e1e1e;}
.drK .postTextRelated,.drK .postTextRelated b{border-color:rgba(255,255,255,.15)}


.Blog .post { -webkit-touch-callout:none; -webkit-user-select:none; -khtml-user-select:none; -ms-user-select:none; -moz-user-select:none; }/*mematikan fungsi seleksi*/
.Blog .post blockquote,.post pre,.post code,h1 ,.note,.sp { -webkit-touch-callout:text; -webkit-user-select:text; -khtml-user-select:text; -ms-user-select:text; -moz-user-select:text; }/*mengecualikan class atau id tertentu*/

]]></b:skin>

<style>/*<![CDATA[*/
/* Font Body and Heading */ @font-face{font-family: 'Noto Sans';font-style: italic;font-weight: 400;font-display: swap;src: url(https://fonts.gstatic.com/s/notosans/v11/o-0OIpQlx3QUlC5A4PNr4ARMQ_m87A.woff2) format('woff2'), url(https://fonts.gstatic.com/s/notosans/v11/o-0OIpQlx3QUlC5A4PNr4DRG.woff) format('woff')} @font-face{font-family: 'Noto Sans';font-style: italic;font-weight: 700;font-display: swap;src: url(https://fonts.gstatic.com/s/notosans/v11/o-0TIpQlx3QUlC5A4PNr4Az5ZuyDzW0.woff2) format('woff2'), url(https://fonts.gstatic.com/s/notosans/v11/o-0TIpQlx3QUlC5A4PNr4Az5ZtyH.woff) format('woff')} @font-face{font-family: 'Noto Sans';font-style: normal;font-weight: 400;font-display: swap;src: url(https://fonts.gstatic.com/s/notosans/v11/o-0IIpQlx3QUlC5A4PNr5TRA.woff2) format('woff2'), url(https://fonts.gstatic.com/s/notosans/v11/o-0IIpQlx3QUlC5A4PNb4Q.woff) format('woff')} @font-face{font-family: 'Noto Sans';font-style: normal;font-weight: 700;font-display: swap;src: url(https://fonts.gstatic.com/s/notosans/v11/o-0NIpQlx3QUlC5A4PNjXhFVZNyB.woff2) format('woff2'), url(https://fonts.gstatic.com/s/notosans/v11/o-0NIpQlx3QUlC5A4PNjXhFlYA.woff) format('woff')}

/* Source Code Font */ @font-face {font-family: 'Fira Mono';font-style: normal;font-weight: 400;font-display: swap;src: local('Fira Mono Regular'), local('FiraMono-Regular'), url(https://fonts.gstatic.com/s/firamono/v9/N0bX2SlFPv1weGeLZDtQIg.woff) format('woff'), url(https://fonts.gstatic.com/s/firamono/v9/N0bX2SlFPv1weGeLZDtgJv7S.woff2) format('woff2')}

/* Standar CSS */ ::selection{color:#fff;background:var(--linkC)} *, ::after, ::before{-webkit-box-sizing:border-box;box-sizing:border-box} h1, h2, h3, h4, h5, h6{margin:0;font-weight:700;font-family:var(--fontH);color:var(--headC)} h1{font-size:1.9rem} h2{font-size:1.7rem} h3{font-size:1.5rem} h4{font-size:1.4rem} h5{font-size:1.3rem} h6{font-size:1.2rem} a{color:var(--linkC);text-decoration:none} a:hover{opacity:.9;transition:opacity .1s} table{border-spacing:0} iframe{max-width:100%;border:0;margin-left:auto;margin-right:auto} input, button, select, textarea{font:inherit;font-size:100%;color:inherit;line-height:normal} input::placeholder{color:rgba(0,0,0,.5)} img{display:block;position:relative;max-width:100%;height:auto} svg{width:22px;height:22px;fill:var(--iconC)} svg.line, svg .line{fill:none!important;stroke:var(--iconC);stroke-linecap:round;stroke-linejoin:round; stroke-width:1} svg.c-1{fill:var(--iconCa)} svg.c-2{fill:var(--iconCs); opacity:.4} .hidden{display:none} .invisible{visibility:hidden} .clear{width:100%;display:block;margin:0;padding:0;float:none;clear:both} .fCls{display:block;position:fixed;top:0;left:0;right:0;bottom:0;z-index:1;transition:var(--trans-1);background:transparent;opacity:0;visibility:hidden} .free::after, .new::after{display:inline-block;content:'Free!';color:var(--linkC);font-size:12px;font-weight:400;margin:0 5px} .new::after{content:'New!'}

/* Main Element */ html{scroll-behavior:smooth;overflow-x:hidden} body{position:relative;margin:0;padding:0!important;width:100%;font-family:var(--fontB);font-size:14px;color:var(--bodyC);background:var(--bodyB);-webkit-font-smoothing: antialiased;} .secIn{margin:0 auto;padding-left:20px;padding-right:20px;max-width:var(--contentW)}

/* Notif Section */ .ntfC{display:flex;align-items:center;position:relative;min-height:var(--notifH); background:var(--notifU);color:var(--notifC); padding:10px 25px; font-size:13px; transition:var(--trans-1);overflow:hidden} .ntfC .secIn{width:100%; position:relative} .ntfC .c{display:flex;align-items:center} .ntfT{width:100%; padding-right: 15px; text-align:center} .ntfT a{color:var(--notifL); font-weight:700} .ntfI:checked ~ .ntfC{height:0;min-height:0; padding:0; opacity:0;visibility:hidden} .ntfA{display:inline-flex;align-items:center;justify-content:center;text-align:initial} .ntfA >a{flex-shrink:0;white-space:nowrap;display:inline-block; margin:0 10px;padding:8px 12px;border-radius:3px; background:var(--notifL);color:#fffdfc; font-size:12px;font-weight:400; box-shadow:0 10px 8px -8px rgb(0 0 0 / 12%);text-decoration:none}

/* Fixed/Pop-up Element */ .fixL{display:flex;align-items:center;position:fixed;left:0;right:0;bottom:0;margin-bottom:-100%;z-index:20;transition:var(--trans-1);width:100%;height:100%;opacity:0;visibility:hidden} .fixLi, .fixL .cmBri{width:100%;max-width:680px;max-height:calc(100% - 60px);border-radius:12px;transition:inherit;z-index:3;display:flex;overflow:hidden;position:relative;margin:0 auto;box-shadow:0 5px 30px 0 rgba(0,0,0,.05)} .fixLs{padding:60px 20px 20px;overflow-y:scroll;overflow-x:hidden;width:100%;background:var(--contentB)} .fixH, .mnH, .srhB .BlogSearch{display:flex;background:inherit;position:absolute;top:0;left:0;right:0;padding:0 10px;z-index:2} .fixH .cl, .srhB .c{padding:0 10px;display:flex;align-items:center;justify-content:flex-end;position:relative;flex-shrink:0;min-width:40px} .fixH .c::after, .ntfC .c::after, .mnH .c::before, .srhB .c::after{content:'\2715';line-height:18px;font-size:14px} .fixT::before{content:attr(data-text);flex-grow:1;padding:16px 10px;font-size:90%;opacity:.7} .fixT .c::before, .mnH .c::after{content:attr(aria-label);font-size:11px;margin:0 8px;opacity:.6} .fixi:checked ~ .fixL, #comment:target .fixL{margin-bottom:0;opacity:1;visibility:visible} .fixi:checked ~ .fixL .fCls, #comment:target .fixL .fCls{opacity:1;visibility:visible;background:rgba(0,0,0,.2); -webkit-backdrop-filter:saturate(180%) blur(10px); backdrop-filter:saturate(180%) blur(10px)} .shBri, .tmBr{max-width:520px} .fnBr{max-width:480px}

/* Display Flex */ .bIc{display:flex;align-items:center}

/* Header */ header{width:100%;z-index:10; position:-webkit-sticky;position:sticky;top:0; border-bottom:var(--headerL) solid var(--contentL)} header a{color:inherit} header svg{width:20px;height:20px;fill:var(--headerI); opacity:.8} header svg.line{fill:none;stroke:var(--headerI)} .headCn{position:relative;height:var(--headerH);color:var(--headerC);background:var(--headerB)} .headIn{display:flex;justify-content:space-between;height:100%} .headL{display:flex;align-items:center;min-width:200px;max-width: 300px ; /* change this to increase header title width */} .headL .headIc{flex:0 0 35px;padding-right:5px} .headI .headP{display:flex;justify-content:flex-end;align-items:center;position:relative;height:100%} .headI{height:100%; position:relative;width:calc(100% + 15px);left:-7.5px;right:-7.5px} .headI >*{margin:0 7.5px} .headIc{font-size:11px;display:flex;list-style:none;margin:0;padding:0} .headIc >*{position:relative} .headIc svg{z-index:1} ul.headIc{position:relative;width:calc(100% + 14px);left:-7px;right:-7px;justify-content:flex-end} ul.headIc li{margin:0 2px} /* Header Widget */ .Header{background-repeat:no-repeat;background-size:100%;background-position:center} .Header img{max-width:160px;max-height:45px} .Header .headH{display:block;color:inherit;font-size:var(--headerT); font-weight:var(--headerW)} .Header .headH.hasSub{display:flex;align-items:baseline} .Header .headTtl{overflow:hidden;white-space:nowrap;text-overflow:ellipsis; display:block} .Header .headSub{margin:0 5px;font:400 11px var(--fontB); white-space:nowrap;text-overflow:ellipsis;overflow:hidden;max-width:60px;opacity:.6} .Header .headSub::before{content:attr(data-text)} /* Header Icon */ .tIc{width:30px;height:30px;justify-content:center} .tIc::after{content:'';background:var(--transB);border-radius:12px;position:absolute;left:0;right:0;top:0;bottom:0;transition:var(--trans-1);opacity:0;visibility:hidden} .tIc:hover::after{opacity:1;visibility:visible;transform:scale(1.3,1.3)} .tDL .d2, .drK .tDL .d1, .grD .tGr .s3{display:none} 

/* Scroll Menu */ .navI{background-color:var(--navB); overflow-y:hidden;overflow-x:scroll;scroll-behavior:smooth;scroll-snap-type:x mandatory; -ms-overflow-style:none;-webkit-overflow-scrolling:touch; display:flex;padding:0} .navI ul{display:flex;list-style:none;margin:0;padding:0;white-space:nowrap} .navI li{margin:0 15px;padding:10px 0;position:relative; scroll-snap-align: start} .navI li:first-child{margin-left:auto} .navI li:last-child{margin-right:auto} .navI .l{display:block;color:inherit;padding:8px 0} .navI .l::before{content:attr(data-text)} .navI .l::after{content:'';height:1px;border-radius:2px 2px 0 0;background:var(--linkC);position:absolute;bottom:0;left:0;right:0;opacity:0} .navI span.l{opacity:.7} .navI a.l:hover, .navI .l.a{color:var(--linkC)}

/* mainNav */ .mnBr ul{list-style:none;margin:0;padding:0} .mnMn svg{flex-shrink:0} .mnMn svg.d{width:14px;height:14px}

/* mainIn Section */ .blogCont{flex-grow:1;padding:20px 0 0;position:relative;transition:var(--trans-1)} .blogCont .section:not(.no-items), .blogCont .widget:not(:first-child){margin-top:40px} .blogCont .section:first-child, .blogCont footer .widget:not(:first-child){margin-top:0} .blogAd .section:not(.no-items){margin-bottom:40px} .blogM{flex-wrap:wrap;justify-content:center;padding-bottom:40px} .sidebar{max-width:500px;margin:50px auto 0} .sideSticky{position:-webkit-sticky;position:sticky;top:calc(var(--headerH) + 10px)} .onPs .mainbar, .onHm .mainbar{max-width:var(--postW)} .onPg .mainbar, .onMl:not(.grD) .mainbar{max-width:var(--pageW)} .onMl.grD .mainbar{max-width:100%}

/* Footer */ footer{font-size:97%;line-height:1.8em; padding:30px 0; border-top:var(--fotL) solid var(--contentL); color:var(--fotT); background:var(--fotB)} footer .LinkList a, footer .sL li >*{display:inline-block;color:inherit;line-height:20px} footer .LinkList a:hover{text-decoration:underline} footer .LinkList ul:not(.sL) li::before{content:'\2013'; opacity:.3} footer .sL{display:flex;flex-wrap:wrap;align-items:baseline;font-size:13px;opacity:.8} footer .sL li{display:inline-flex;align-items:baseline} footer .sL li:not(:first-child)::before{content:'/';margin:0 5px} footer .sL li >*::before{content:attr(data-text)} .fotIn ul{list-style:none;margin:0;padding:0} .fotIn{display:flex;flex-wrap:wrap;position:relative;width:calc(100% + 30px);left:-15px;right:-15px} .fotIn >*{width:calc(21.666% - 30px);margin:0 15px} .fotIn >*:first-child{width:calc(35% - 30px)} .fotIn .widget{margin-bottom:30px} .fotIn .widget .title{color:inherit;margin-bottom:12px;font-weight:700;font-size:14px} .abtU{max-width:calc(100% - 25px)} .abtU::before{content:attr(data-text);font-size:13px; opacity:.6;display:block;margin-bottom:3px} .abtT .tl{color:inherit; font-size:1.3rem} .abtD{line-height:1.6em;margin:20px 0 0} /* Footer Credit and Backtop */ .cdtIn{display:flex;align-items:baseline;justify-content:space-between; position:relative;width:calc(100% + 20px);left:-10px;right:-10px} .cdtIn >*{margin:0 10px} .cdtIn .HTML{overflow:hidden;white-space:nowrap;text-overflow:ellipsis} .fotCd{display:inline-flex} .fotCd .creator{opacity:0} .tTop svg{width:20px;height:20px;stroke:var(--fotT)} .toTop{display:flex;align-items:center; white-space:nowrap} .toTop::before{content:attr(data-text); opacity:.7;margin:0 5px} .toTopF{display:flex;align-items:center;justify-content:center;width:45px;height:45px;border-radius:50%;background:var(--linkB);position:fixed;bottom:20px;right:20px} .toTopF svg{stroke:#fffdfc;stroke-width:2}

/* Article*/ .onId:not(.grD) .ntry, .itemFt .itm{display:flex;flex-wrap:wrap;align-items:center;position:relative; margin-bottom:20px;padding: 10px 0px 10px;border-radius: 8px;border: 1px solid var(--contentL);border-radius:8px;box-shadow:0px 5px 35px rgb(0 0 0 / 10%); width:calc(100% + 0px);left:-0px;right:-0px} .onId:not(.grD) .ntry >*, .itemFt .itm >*{flex:0 0 calc(50% - 22px);width:calc(50% - 22px); margin-bottom:0;margin-left:11px;margin-right:11px} .onId:not(.grD) .ntry >*:last-child, .itemFt .itm >*:last-child{flex-grow:1} .onId:not(.grD) div.ntry >*{flex:0 0 calc(100% - 25px);width:calc(100% - 25px)} .onId .ntry{margin-bottom:40px; position:relative} .onId .blogPts.mty{display:block;width:100%;left:0;right:0} .onId .blogPts.mty .noPosts{width:100%;margin:0} .blogPts .ntry.noAd .widget, .Blog ~ .HTML{display:none}

/* Gridmode */ .tGr::before{content:attr(data-grid);position:absolute;right:32px;opacity:.8} .grD .tGr::before{content:attr(data-list)} .grD .blogPts{display:flex;flex-wrap:wrap;position:relative; width:calc(100% + 22px);left:-11px;right:-11px} .grD .pCntn{margin:0px 11px} .grD .ntry{width:calc(50% - 22px);margin-left:11px;margin-right:11px;margin-bottom:20px;padding: 0px 0px 45px;border-radius: 8px;border: 1px solid var(--contentL);border-radius:8px;box-shadow:0px 5px 35px rgb(0 0 0 / 10%); position:relative} .grD div.ntry{padding-bottom:0} .grD .ntry .pInf{position:absolute;bottom:10px;left:0px;right:0px} @media screen and (min-width:897px){.onMl.grD .ntry{width:calc(33.33% - 22px)}} @media screen and (max-width:1100px) and (min-width: 897px){.grD .ntry .pTtl{font-size:1.1rem}} @media screen and (max-width:500px){.grD:not(.oGrd) .ntry .pSnpt, .grD:not(.oGrd) .ntry .pHdr .aIm{display:none} .grD .blogPts{width:calc(100% + 15px);left:-7.5px;right:-7.5px} .grD .ntry{width:calc(50% - 15px);margin-left:7.5px;margin-right:7.5px} .grD div.ntry{width:calc(100% - 15px)}}

/* Blog title */ .blogTtl{font-size:14px; margin:0 0 22px;width:calc(100% + 16px);display:flex;align-items:center;justify-content:space-between;position:relative;left:-8px;right:-8px} .blogTtl .t, .blogTtl.hm .title{margin:0 8px;flex-grow:1} .blogTtl .t span{font-weight:400;font-size:90%; opacity:.7} .blogTtl .t span::before{content:attr(data-text)} .blogTtl .t span::after{content:''; margin:0 4px} .blogTtl .t span.hm::after{content:'/'; margin:0 8px} .blogTtl .g{position:relative;flex-shrink:0;margin:0 2px;font-size:12px} .blogTtl .g svg{width:20px;height:20px} /* Thumbnail */ .pThmb{flex:0 0 calc(50% - 12.5px);overflow:hidden;position:relative;border-radius:3px; margin-bottom:20px; background:var(--transB)} .pThmb .thmb{display:block;position:relative;padding-top:52.335%; color:inherit; transition:var(--trans-1)} .pThmb .thmb amp-img{position:absolute;top:50%;left:50%;min-width:100%;min-height:100%;max-height:108%;text-align:center;transform:translate(-50%, -50%)} .pThmb div.thmb span::before{content:attr(data-text); opacity:.7; white-space:nowrap} .pThmb:not(.nul)::before{position:absolute;top:0;right:0;bottom:0;left:0; transform:translateX(-100%); background-image:linear-gradient(90deg, rgba(255,255,255,0) 0, rgba(255,255,255,.3) 20%, rgba(255,255,255,.6) 60%, rgba(255,255,255, 0)); animation:shimmer 2s infinite;content:''} .pThmb.iyt:not(.nul) .thmb::after{content:'';position:absolute;top:0;left:0;right:0;bottom:0; background:rgba(0,0,0,.4) url("data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='%23fff' stroke-width='1.5' stroke-linecap='round' stroke-linejoin='round'><path d='M4 11.9999V8.43989C4 4.01989 7.13 2.2099 10.96 4.4199L14.05 6.1999L17.14 7.9799C20.97 10.1899 20.97 13.8099 17.14 16.0199L14.05 17.7999L10.96 19.5799C7.13 21.7899 4 19.9799 4 15.5599V11.9999Z'/></svg>") center / 35px no-repeat; opacity:0;transition:var(--trans-1)} .pThmb.iyt:not(.nul):hover .thmb::after{opacity:1} /* Sponsored */ .iFxd{display:flex;justify-content:flex-end;position:absolute;top:0;left:0;right:0;padding:10px 6px;font-size:13px;line-height:16px} .iFxd >*{display:flex;align-items:center;margin:0 5px;padding:5px 2.5px;border-radius:8px;background:var(--contentB);color:inherit;box-shadow:0 8px 25px 0 rgba(0,0,0,.1)} .iFxd >* svg{width:16px;height:16px;stroke-width:1.5;margin:0 2.5px;opacity:.7} .iFxd .cmnt{padding:5px;color:var(--bodyC)} .iFxd .cmnt::after{content:attr(data-text);margin:0 2.5px;opacity:.7} .drK .iFxd >* svg.line{stroke:var(--iconC)} /* Label */ .pLbls::before, .pLbls >*::before{content:attr(data-text)} .pLbls::before{opacity:.7} .pLbls a:hover{text-decoration:underline} .pLbls >*{color:inherit;display:inline} .pLbls >*:not(:last-child)::after{content:'/'} /* Profile Images and Name */ .im{width:35px;height:35px;border-radius:16px; background-color:var(--transB);background-size:100%;background-position:center;background-repeat:no-repeat;display:flex;align-items:center;justify-content:center} .im svg{width:18px;height:18px;opacity:.4} .nm::after{content:attr(data-text)} /* Title and Entry */ .pTtl{font-size:1.2rem;line-height:1.5em} .pTtl.itm{font-size:var(--postT);font-family:var(--fontBa);font-weight:900; line-height:1.3em} .pTtl.itm.nSpr{margin-bottom:30px} .aTtl a:hover{color:var(--linkC)} .aTtl a, .pSnpt{color:inherit; display:-webkit-box;-webkit-line-clamp:3;-webkit-box-orient:vertical;overflow:hidden} .pEnt{margin-top:30px; font-size:var(--postF);font-family:var(--fontBa); line-height:1.8em} /* Snippet, Description, Headers and Info */ .pHdr.nHdr{margin:0} .pHdr{width:calc(100% + 8px);position:relative;left:-4px;right:-4px;margin-bottom:8px; display:flex;align-items:center} .pHdr .aIm{flex-shrink:0;margin:0 4px} .pHdr .aIm .im{width:18px; height:18px} .pHdr .aNm{flex-grow:1; opacity:.8;margin:0 2px; display:inline-flex;flex-wrap:wrap;max-width:calc(100% - 30px)} .pHdr .nm, .pHdr .pLbls{white-space:nowrap;text-overflow:ellipsis;overflow:hidden;margin:0 2px} .pHdr .pLbls{opacity:.8} .pSml{font-size:93%} .pSnpt{-webkit-line-clamp:2;margin:12px 0 0;font-family:var(--fontBa);font-size:14px;line-height:1.5em; opacity:.8} .pSnpt.nTag{color:var(--linkC);opacity:1} .pDesc{font-size:16px;line-height:1.5em;margin:8px 0 25px;opacity:.7} .pInf{display:flex;align-items:center;justify-content:space-evenly; margin-top:15px} .pInf.nTm{margin:0} .pInf.nSpr .pJmp{opacity:1} .pInf.nSpr .pJmp::before{content:attr(aria-label)} .pInf.ps{justify-content:flex-start;align-items:center; margin-top:25px; position:relative;left:-4px;right:-4px;width:calc(100% + 8px)} .pInf.ps .pTtmp{opacity:1} .pInf.ps .pTtmp::before{content:attr(data-date) ' '} .pInf.ps .pTtmp::after{display:inline} .pInf.ps.nul{display:none} .pInf .pIm{flex-shrink:0; margin:0 4px} .pInf .pNm{flex-grow:1;width:calc(100% - 108px);display:inline-flex;flex-wrap:wrap;align-items:baseline} .pInf .pNm.l{display:none} .pInf .pCm{flex-shrink:0;max-width:24px;margin:0 2px} .pInf .pCm.l{max-width:58px} .pInf .pIc{display:inline-flex;justify-content:flex-end;position:relative;width:calc(100% + 10px);left:-5px;right:-5px} .pInf .pIc >*{display:flex;align-items:center;position:relative;margin:0 2px;color:inherit} .pInf .pIc svg{width:20px;height:20px;opacity:.8;z-index:1} .pInf .pIc .cmnt::before{content:attr(data-text);font-size:11px;line-height:18px;padding:0 5px;border-radius:10px;background:#e6e6e6;color:var(--bodyC);position:absolute;top:-5px;right:0;z-index:2} .pInf .pIc .cmnt svg{height:18px} .pInf .pDr{opacity:.7;display:inline-block;margin:0 4px;white-space:nowrap;text-overflow:ellipsis;overflow:hidden;max-width:100%} .pInf .pDr svg{position:relative;margin:0px 0px -3px 0px} .pInf .pDr >*:not(:first-child)::before{content:'\00B7';margin-inline:2px 5px} .pInf .pIn{display:inline} .pInf .nm{margin:0 4px} .pInf .n .nm::before, .pHdr .n .nm::before{content:attr(data-write) ' ';opacity:.7} .pInf .im{width:28px;height:28px} .aTtmp{opacity:.8} .aTtmp, .pJmp{overflow:hidden} .pTtmp::after, .pJmp::before, .iTtmp::before{content:attr(data-text); display:block;line-height:18px; white-space:nowrap;text-overflow:ellipsis;overflow:hidden} .pJmp{display:contents;align-items:center; opacity:0; transition:var(--trans-2)} .pJmp::before{content:attr(aria-label)} .pJmp svg{height:18px;width:18px;stroke:var(--linkC); flex-shrink:0} .ntry:hover .pJmp, .itm:hover .pJmp{opacity:1} /* Blog pager */ .blogPg{display:flex;flex-wrap:wrap;justify-content:space-between; font-size:90%;font-family:var(--fontB);line-height:20px; color:#fffdfc; margin:30px 0 50px; max-width:100%} .blogPg >*{display:flex;align-items:center; padding:10px 13px;margin-bottom:10px; color:inherit;background:var(--linkB); border-radius:3px} .blogPg >* svg{width:18px;height:18px; stroke:var(--darkT); stroke-width:1.5} .blogPg >*::before{content:attr(data-text)} .blogPg .jsLd{margin-left:auto;margin-right:auto} .blogPg .nwLnk::before, .blogPg .jsLd::before{display:none} .blogPg .nwLnk::after, .blogPg .jsLd::after{content:attr(data-text); margin:0 8px} .blogPg .olLnk::before{margin:0 8px} .blogPg .nPst, .blogPg .current{background:var(--contentL); color:var(--bodyCa)} .blogPg .nPst.jsLd svg{fill:var(--darkTa);stroke:var(--darkTa)} .blogPg .nPst svg.line{stroke:var(--darkTa)} /* Breadcrumb */ .brdCmb{margin-bottom:5px;overflow:hidden;text-overflow:ellipsis;white-space:nowrap} .brdCmb a{color:inherit} .brdCmb >*:not(:last-child)::after{content:'/'; margin:0 4px;font-size:90%;opacity:.6} .brdCmb >*{display:inline} .brdCmb .tl::before{content:attr(data-text)} .brdCmb .hm a{font-size:90%;opacity:.7}

/* Article Style */ .pS h1, .pS h2, .pS h3, .pS h4, .pS h5, .pS h6{margin:1.5em 0 18px; font-family:var(--fontBa);font-weight:900; line-height:1.5em} .pS h1:target, .pS h2:target, .pS h3:target, .pS h4:target, .pS h5:target, .pS h6:target{padding-top:var(--headerH);margin-top:0} /* Paragraph */ .pS p{margin:1.7em 0} .pIndent{text-indent:2.5rem} .onIt:not(.Rtl) .dropCap{float:left;margin:4px 8px 0 0; font-size:55px;line-height:45px;opacity:.8} .pS hr{margin:3em 0; border:0} .pS hr::before{content:'\2027 \2027 \2027'; display:block;text-align:center; font-size:24px;letter-spacing:0.6em;text-indent:0.6em;opacity:.8;clear:both} .pRef{display:block;font-size:14px;line-height:1.5em; opacity:.7; word-break:break-word} /* Img and Ad */ .pS img{display:inline-block;border-radius:3px;height:auto !important} .pS img.full{display:block !important; margin-bottom:10px; position:relative; width:100%;max-width:none} .pS .widget, .ps .pAd >*{margin:40px 0} /* Note */ .note{position:relative;padding:16px 20px 16px 50px; background:#e1f5fe;color:#3c4043; font-size:.85rem;font-family:var(--fontB);line-height:1.6em;border-radius:10px;overflow:hidden} .note::before{content:'';width:60px;height:60px;background:#81b4dc;display:block;border-radius:50%;position:absolute;top:-12px;left:-12px;opacity:.1} .note::after{content:'\002A';position:absolute;left:18px;top:16px; font-size:20px; min-width:15px;text-align:center} .note.wr{background:#ffdfdf;color:#48525c} .note.wr::before{background:#e65151} .note.wr::after{content:'\0021'} /* Ext link */ .extL::after{content:''; width:14px;height:14px; display:inline-block;margin:0 5px; background: url("data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='%23989b9f' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'><path d='M13 11L21.2 2.80005'/><path d='M22 6.8V2H17.2'/><path d='M11 2H9C4 2 2 4 2 9V15C2 20 4 22 9 22H15C20 22 22 20 22 15V13'/></svg>") center / 14px no-repeat} /* Scroll img */ .psImg{display:flex;flex-wrap:wrap;align-items:flex-start;justify-content:center; margin:2em 0; position:relative;left:-7px;right:-7px; width:calc(100% + 14px)} .psImg >*{width:calc(50% - 14px); margin:0 7px 14px; position:relative} .psImg img{display:block} .scImg >*{width:calc(33.3% - 14px); margin:0 7px} .btImg label{position:absolute;top:0;left:0;right:0;bottom:0; border-radius:3px; display:flex;align-items:center;justify-content:center; background:rgba(0,0,0,.6); transition:var(--trans-1); -webkit-backdrop-filter:saturate(180%) blur(10px); backdrop-filter:saturate(180%) blur(10px); color:var(--darkT); font-size:13px;font-family:var(--fontB)} .hdImg .shImg{width:100%;margin:0; left:0;right:0; transition:var(--trans-1); max-height:0;opacity:0;visibility:hidden} .inImg:checked ~ .hdImg .shImg{max-height:1000vh;opacity:1;visibility:visible} .inImg:checked ~ .hdImg .btImg label{opacity:0;visibility:hidden} /* Post related */ .pRelate{margin:40px 0;padding:20px 0; border:1px solid #989b9f;border-left:0;border-right:0; font-size:14px;line-height:1.8em} .pRelate b{font-weight:400; margin:0;opacity:.8} .pRelate ul, .pRelate ol{margin:8px 0 0;padding:0 20px} /* Blockquote */ blockquote, .cmC i[rel=quote]{position:relative;font-size:.97rem; opacity:.8;line-height:1.6em;margin-left:0;margin-right:0;padding:5px 20px;border-left:2px solid var(--contentL)} blockquote.s-1, details.sp{font-size:.93rem; padding:25px 25px 25px 45px; border:1px solid #989b9f;border-left:0;border-right:0;line-height:1.7em} blockquote.s-1::before{content:'\201D';position:absolute;top:10px;left:0; font-size:60px;line-height:normal;opacity:.5} /* Table */ .ps table{margin:0 auto; font-size:14px;font-family:var(--fontB)} .ps table:not(.tr-caption-container){min-width:90%;border:1px solid var(--contentL);border-radius:3px;overflow:hidden} .ps table:not(.tr-caption-container) td{padding:16px} .ps table:not(.tr-caption-container) tr:not(:last-child) td{border-bottom:1px solid var(--contentL)} .ps table:not(.tr-caption-container) tr:nth-child(2n+1) td{background:rgba(0,0,0,.01)} .ps table th{padding:16px; text-align:inherit; border-bottom:1px solid var(--contentL)} .ps .table{display:block; overflow-y:hidden;overflow-x:auto;scroll-behavior:smooth} /* Img caption */ figure{margin-left:0;margin-right:0} .ps .tr-caption, .psCaption, figcaption{display:block; font-size:14px;line-height:1.6em; font-family:var(--fontB);opacity:.7} /* Syntax */ .pre{background:var(--synxBg);color:var(--synxC); direction: ltr} .pre:not(.tb){position:relative;border-radius:3px;overflow:hidden;margin:1.7em auto;font-family:var(--fontC)} .pre pre{margin:0;color:inherit;background:inherit} .pre:not(.tb)::before, .cmC i[rel=pre]::before{content:'</>';display:flex;justify-content:flex-end;position:absolute;right:0;top:0;width:100%;background:inherit;color:var(--synxGray);font-size:10px;padding:0 10px;z-index:2;line-height:30px} .pre:not(.tb).html::before{content:'.html'} .pre:not(.tb).css::before{content:'.css'} .pre:not(.tb).js::before{content:'.js'} pre, .cmC i[rel=pre]{display:block;position:relative;font-family:var(--fontC);font-size:13px;line-height:1.6em;border-radius:3px;background:var(--synxBg);color:var(--synxC);padding:30px 20px 20px;margin:1.7em auto; -moz-tab-size:2;tab-size:2;-webkit-hyphens:none;-moz-hyphens:none;-ms-hyphens:none;hyphens:none; overflow:auto;direction:ltr;white-space:pre} pre i{color:var(--synxBlue);font-style:normal} pre i.block{color:#fff;background:var(--synxBlue)} pre i.green{color:var(--synxGreen)} pre i.gray{color:var(--synxGray)} pre i.red{color:var(--synxOrange)} pre i.blue{color:var(--synxBlue)} code{display:inline;padding:5px;font-size:14px;border-radius:3px;line-height:inherit;color:var(--synxC);background:#f2f3f5;font-family:var(--fontC)} /* Multi syntax */ .pre.tb{border-radius:5px} .pre.tb pre{margin:0;background:inherit} .pre.tb .preH{font-size:13px;border-color:rgba(0,0,0,.05);margin:0} .pre.tb .preH >*{padding:13px 20px} .pre.tb .preH::after{content:'</>';font-size:10px;font-family:var(--fontC);color:var(--synxGray);padding:15px;margin-left:auto} .pre.tb >:not(.preH){display:none} .pS input[id*="1"]:checked ~ div[class*="C-1"], .pS input[id*="2"]:checked ~ div[class*="C-2"], .pS input[id*="3"]:checked ~ div[class*="C-3"], .pS input[id*="4"]:checked ~ div[class*="C-4"]{display:block} /* ToC */ .pS details summary{list-style:none;outline:none} .pS details summary::-webkit-details-marker{display:none} details.sp{padding:20px 15px} details.sp summary{display:flex;justify-content:space-between;align-items:baseline} details.sp summary::after{content:attr(data-show);font-size:12px; opacity:.7;cursor:pointer} details.sp[open] summary::after{content:attr(data-hide)} details.toc a:hover{text-decoration:underline} details.toc a{display:-webkit-box;-webkit-line-clamp:3;-webkit-box-orient:vertical;overflow:hidden; color:inherit} details.toc ol{list-style:none;padding:0;margin:0; line-height:1.6em; counter-reset:toc-count} details.toc ol ol ol ol{display:none} details.toc ol ol, .tocIn li:not(:last-child){margin-bottom:5px} details.toc li li:first-child{margin-top:5px} details.toc li{display:flex;flex-wrap:wrap; justify-content:flex-end} details.toc li::before{flex:0 0 23px; content:counters(toc-count,'.')'. ';counter-increment:toc-count} details.toc li a{flex:1 0 calc(100% - 23px)} details.toc li li::before{flex:0 0 28px; content:counters(toc-count,'.')} details.toc li li a{flex:1 0 calc(100% - 28px)} details.toc li li li::before{flex:0 0 45px} details.toc li li li a{flex:1 0 calc(100% - 45px)} details.toc .toC >ol{margin-top:1em} details.toc .toC >ol >li >ol{flex:0 0 calc(100% - 23px)} details.toc .toC >ol >li >ol ol{flex:0 0 calc(100% - 45px)} details.toc .toC >ol >li >ol ol ol{flex:0 0 calc(100% - 35px)} /* Accordion */ .showH{margin:1.7em 0;font-size:.93rem;font-family:var(--fontB);line-height:1.7em} details.ac{padding:18px 0;border-bottom:1px solid var(--contentL)} details.ac:first-child{border-top:1px solid var(--contentL)} details.ac summary{font-weight:700;cursor:default; display:flex;align-items:baseline; transition:var(--trans-1)} details.ac summary::before{content:'\203A'; flex:0 0 25px;display:flex;align-items:center;justify-content:flex-start;padding:0 5px; font-weight:400;font-size:1.33rem;color:inherit} details.ac[open] summary{color:var(--linkC)} details.ac:not(.alt)[open] summary::before{transform:rotate(90deg);padding:0 0 0 5px;justify-content:center} details.ac.alt summary::before{content:'\002B'; padding:0 2px} details.ac.alt[open] summary::before{content:'\2212'} details.ac .aC{padding:0 25px;opacity:.9} /* Tabs */ .tbHd{display:flex; border-bottom:1px solid var(--contentL);margin-bottom:30px;font-size:14px;font-family:var(--fontB);line-height:1.6em; overflow-x:scroll;overflow-y:hidden;scroll-behavior:smooth;scroll-snap-type:x mandatory; -ms-overflow-style:none;-webkit-overflow-scrolling:touch} .tbHd >*{padding:12px 15px; border-bottom:1px solid transparent; transition:var(--trans-1);opacity:.6;white-space:nowrap; scroll-snap-align:start} .tbHd >*::before{content:attr(data-text)} .tbCn >*{display:none;width:100%} .tbCn >* p:first-child{margin-top:0} .pS input[id*="1"]:checked ~ .tbHd label[for*="1"], .pS input[id*="2"]:checked ~ .tbHd label[for*="2"], .pS input[id*="3"]:checked ~ .tbHd label[for*="3"], .pS input[id*="4"]:checked ~ .tbHd label[for*="4"]{border-color:var(--linkB);opacity:1} .pS input[id*="1"]:checked ~ .tbCn div[class*="Text-1"], .pS input[id*="2"]:checked ~ .tbCn div[class*="Text-2"], .pS input[id*="3"]:checked ~ .tbCn div[class*="Text-3"], .pS input[id*="4"]:checked ~ .tbCn div[class*="Text-4"]{display:block} .tbHd.stick{position:-webkit-sticky;position:sticky;top:var(--headerH);background:var(--bodyB)} /* Split */ .ps .blogPg{font-size:13px; justify-content:center; position:relative;width:calc(100% + 8px);left:-4px;right:-4px} .ps .blogPg >*{padding:8px 15px;margin:0 4px 8px} /* Youtube fullpage */ .videoYt{position:relative;padding-bottom:56.25%; overflow:hidden;border-radius:5px} .videoYt iframe{position:absolute;width:100%;height:100%;left:0;right:0} /* Lazy Youtube */ .lazyYt{background:var(--synxBg);position:relative;overflow:hidden;padding-top:56.25%;border-radius:5px} .lazyYt img{width:100%;top:-16.84%;left:0;opacity:.95} .lazyYt img, .lazyYt iframe, .lazyYt .play{position:absolute} .lazyYt iframe{width:100%;height:100%;bottom:0;right:0} .lazyYt .play{top:50%;left:50%; transform:translate3d(-50%,-50%,0); transition:all .5s ease;display:block;width:70px;height:70px;z-index:1} .lazyYt .play svg{width:inherit;height:inherit; fill:none;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:10;stroke-width:8} .lazyYt .play .c{stroke:rgba(255,255,255,.85);stroke-dasharray:650;stroke-dashoffset:650; transition:all .4s ease-in-out; opacity:.3} .lazyYt .play .t{stroke:rgba(255,255,255,.75);stroke-dasharray:240;stroke-dashoffset:480; transition:all .6s ease-in-out; transform:translateY(0)} .lazyYt .play:hover .t{animation:nudge .6s ease-in-out;-webkit-animation:nudge .6s ease-in-out} .lazyYt .play:hover .t, .lazyYt .play:hover .c{stroke-dashoffset:0; opacity:.7;stroke:#FF0000} .nAmp .lazyYt{display:none} /* Button */ .button{display:inline-flex;align-items:center; margin:10px 0;padding:12px 15px;outline:0;border:0; border-radius:3px;line-height:20px; color:#fffdfc; background:var(--linkB); font-size:14px;font-family:var(--fontB); white-space:nowrap;overflow:hidden;max-width:320px} .button.ln{color:inherit;background:transparent; border:1px solid var(--bodyCa)} .button.ln:hover{border-color:var(--linkB);box-shadow:0 0 0 1px var(--linkB) inset} .btnF{display:flex;justify-content:center; margin:10px 0;width:calc(100% + 12px);left:-6px;right:-6px;position:relative} .btnF >*{margin:0 6px} /* Download btn */ .dlBox{max-width:500px;background:#f1f1f0;border-radius:10px;padding:12px;margin:1.7em 0; display:flex;align-items:center; font-size:14px} .dlBox .fT{flex-shrink:0;display:flex;align-items:center;justify-content:center; width:45px;height:45px; padding:10px; background:rgba(0,0,0,.1);border-radius:5px} .dlBox .fT::before{content:attr(data-text);opacity:.7} .dlBox a{flex-shrink:0;margin:0;padding:10px 12px;border-radius:5px;font-size:13px} .dlBox a::after{content:attr(aria-label)} .dlBox .fN{flex-grow:1; width:calc(100% - 200px);padding:0 15px} .dlBox .fN >*{display:block;white-space:nowrap;overflow:hidden;text-overflow:ellipsis} .dlBox .fS{line-height:16px;font-size:12px;opacity:.8} /* Icon btn */ .icon{flex-shrink:0;display:inline-flex} .icon::before{content:'';width:18px;height:18px;background-size:18px;background-repeat:no-repeat;background-position:center} .icon::after{content:'';padding:0 6px} .icon.dl::before, .drK .button.ln .icon.dl::before{background-image:url("data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='%23fefefe' stroke-linecap='round' stroke-linejoin='round' stroke-width='1.5'><polyline points='8 17 12 21 16 17'/><line x1='12' y1='12' x2='12' y2='21'/><path d='M20.88 18.09A5 5 0 0 0 18 9h-1.26A8 8 0 1 0 3 16.29'/></svg>")} .icon.demo::before{background-image:url("data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='%23fefefe' stroke-linecap='round' stroke-linejoin='round' stroke-width='1.5'><path d='M7.39999 6.32003L15.89 3.49003C19.7 2.22003 21.77 4.30003 20.51 8.11003L17.68 16.6C15.78 22.31 12.66 22.31 10.76 16.6L9.91999 14.08L7.39999 13.24C1.68999 11.34 1.68999 8.23003 7.39999 6.32003Z'/><path d='M10.11 13.6501L13.69 10.0601'/></svg>")} .button.ln .icon.dl::before{background-image:url("data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='%2308102b' stroke-linecap='round' stroke-linejoin='round' stroke-width='1.5'><polyline points='8 17 12 21 16 17'/><line x1='12' y1='12' x2='12' y2='21'/><path d='M20.88 18.09A5 5 0 0 0 18 9h-1.26A8 8 0 1 0 3 16.29'/></svg>")} /* Lightbox image */ .zmImg.s{position:fixed;top:0;left:0;bottom:0;right:0;width:100%;margin:0;background:rgba(0,0,0,.75); display:flex;align-items:center;justify-content:center;z-index:999; -webkit-backdrop-filter:saturate(180%) blur(15px); backdrop-filter:saturate(180%) blur(15px)} .zmImg.s img{display:block;max-width:92%;max-height:92%;width:auto;margin:auto;border-radius:10px;box-shadow:0 5px 30px 0 rgba(0,0,0,.05)} .zmImg.s img.full{left:auto;right:auto;border-radius:10px;width:auto} .zmImg::after{content:'\2715';line-height:16px;font-size:14px;color:#fffdfc;background:var(--linkB); position:fixed;bottom:-20px;right:-20px; display:flex;align-items:center;justify-content:center;width:45px;height:45px;border-radius:50%; transition:var(--trans-1);opacity:0;visibility:hidden} .zmImg.s::after{bottom:20px;right:20px;opacity:1;visibility:visible;cursor:pointer} /* kontak */ .contact-form-widget{border: 1px solid var(--contentL);border-radius: 8px;box-shadow: 0px 5px 35px rgb(0 0 0 / 10%);padding: 10px 10px;}

/* Article Style Responsive */ @media screen and (max-width: 640px){.pS img.full{width:calc(100% + 40px);left:-20px;right:-20px; border-radius:0} .note{font-size:13px} .scImg{flex-wrap:nowrap;justify-content:flex-start;position:relative;width:calc(100% + 40px);left:-20px;right:-20px;padding:0 13px; overflow-y:hidden;overflow-x:scroll;scroll-behavior:smooth;scroll-snap-type:x mandatory; -ms-overflow-style:none;-webkit-overflow-scrolling:touch} .scImg >*{flex:0 0 80%;scroll-snap-align:center} .ps .table{position:relative; width:calc(100% + 40px);left:-20px;right:-20px;padding:0 20px; display:flex}} @media screen and (max-width:500px){.hdImg{width:100%;left:0;right:0} .hdImg >*, .shImg >*{width:100%;margin:0 0 16px} .ps .tr-caption, .psCaption, figcaption{font-size:13px} .btnF >*{flex-grow:1;justify-content:center}.btnF >*:first-child{flex:0 0 auto} .dlBox a{width:42px;height:42px;justify-content:center} .dlBox a::after, .dlBox .icon::after{display:none} .pS .separator a{display:block!important;margin:0!important}} .separator a,.separator img{margin:auto 0!important} .separator .zmImg img{margin:auto!important}

/* Author profile */ .admPs{display:flex; max-width:480px;margin:30px 0; padding:12px 12px 15px; background:var(--contentB);border-radius:8px; box-shadow:0 10px 25px -3px rgba(0,0,0,.1)} .admIm{flex-shrink:0; padding:5px 0 0} .admIm .im{width:34px;height:34px} .admI{flex-grow:1; width:calc(100% - 34px);padding:0 12px} .admN::before{content:attr(data-write) ' '; opacity:.7;font-size:90%} .admN::after{content:attr(data-text)} .admA{margin:5px 0 0; font-size:90%; opacity:.9;line-height:1.5em; /*display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden*/} /* Share btn */ .pSh{margin:15px 0;padding:18px 0;border:1px solid rgba(0,0,0,.05);border-left:0;border-right:0} .pShc{display:flex;align-items:center;flex-wrap:wrap; position:relative;width:calc(100% + 18px);left:-9px;right:-9px;font-size:13px;opacity:.8} .pShc::before{content:attr(data-text);margin:0 9px;flex-shrink:0} .pShc >*{margin:0 5px; display:flex;align-items:center; color:inherit} .pShc a::after{content:attr(data-text);margin:0 3px} .pShc svg, .cpL svg{width:18px;height:18px; margin:0 3px} .shL{position:relative;width:calc(100% + 20px);left:-10px;right:-10px;margin-bottom:20px;display:flex;flex-wrap:wrap;justify-content:center} .shL >*{margin:0 10px 20px;text-align:center} .shL >*::after{content:attr(data-text);font-size:90%;opacity:.7;display:block} .shL a{display:flex;align-items:center;justify-content:center;flex-wrap:wrap; width:65px;height:65px; color:inherit;margin:0 auto 5px;padding:8px;border-radius:26px;background:#f1f1f0} .shL svg{opacity:.8} .cpL{padding-bottom:15px} .cpL::before{content:attr(data-text);display:block;margin:0 0 15px;opacity:.8} .cpL svg{margin:0 4px;opacity:.7} .cpL input{border:0;outline:0; background:transparent;color:rgba(8,16,43,.4); padding:18px 8px;flex-grow:1} .cpL label{color:var(--linkC);display:flex;align-items:center;align-self:stretch; flex-shrink:0;padding:0 8px} .cpLb{display:flex;align-items:center;position:relative;background:#f1f1f0;border-radius:4px 4px 0 0;border-bottom:1px solid rgba(0,0,0,.25); padding:0 8px} .cpLb:hover{border-color:rgba(0,0,0,.42);background:#ececec} .cpLn span{display:block;padding:5px 14px 0;font-size:90%;color:#2e7b32; transition:var(--trans-1);animation:fadein 2s ease forwards; opacity:0;height:22px} /* Entry font */ .fnIn:checked ~ .fnB .fCls{-webkit-backdrop-filter:none;backdrop-filter:none} .fnC{display:flex;list-style:none;margin:0;padding:0} .fnC li{flex:0 0 33.33%;display:flex;justify-content:center;align-items:baseline;padding-bottom:17px;position:relative} .fnC li:nth-child(1) label::before{font-size:25px;line-height:38px} .fnC li:nth-child(1) label::after{content:'Small'} .fnC li:nth-child(3) label::before{font-size:40px;line-height:27px} .fnC li:nth-child(3) label::after{content:'Large'} .fnC label{display:inline-flex;flex-direction:column;align-items:center;opacity:.6} .fnC label:hover{opacity:1} .fnC label::before{content:'A';font-size:32px;font-weight:700;line-height:34px} .fnC label::after{content:'Default';font-size:12px;position:absolute;bottom:0} .fontS1:checked ~ .fnB .fnt1, .fontS2:checked ~ .fnB .fnt2, .fontS3:checked ~ .fnB .fnt3{opacity:1} .fontS1:checked ~ .pInr .pEnt{font-size:var(--postFS)} .fontS3:checked ~ .pInr .pEnt{font-size:var(--postFL)} @media screen and (max-width:500px){.fontS1:checked ~ .pInr .pEnt{font-size:var(--postFSm)} .fontS3:checked ~ .pInr .pEnt{font-size:var(--postFLm)}} /* Post bMenu */ .bMenu{display:none !important;position:fixed;left:0;right:0;bottom:0;display:flex;align-items:center;justify-content:center;padding:25px 15px 20px;z-index:2;background-image:linear-gradient(0deg, rgba(255,255,255,.9) 25%, rgba(255,255,255,.75) 50%, rgba(255,255,255,.35) 75%, rgba(255,255,255,.01) 95%)} .bMenu >*{position:relative;margin:0 5px;border-radius:10px;box-shadow:0 10px 20px -10px rgba(0,0,0,.25)} .bMenu >*:not(.bCmt){width:42px;height:42px;justify-content:center;background:#fffdfc} .bMenu .bCmt{justify-content:center;padding:0 10px;height:42px;flex-grow:1;background:var(--linkB);color:var(--darkT)} @media screen and (min-width:501px){.bMenu{display:none}} /* Comments */ .pCmnts{margin-top:50px} .cmDis{text-align:center;margin-top:20px;opacity:.7} .cmMs{margin-bottom:20px} .cm iframe{width:100%} .cm:not(.cmBr) .cmBrs{background:transparent;position:relative;padding:60px 20px 0;width:calc(100% + 40px);left:-20px;right:-20px} .cmH h3.title{margin:0;flex-grow:1;padding:16px 10px} .cmH .s{margin:0 14px} .cmH .s::before{content:attr(data-text);margin:0 6px;opacity:.7;font-size:90%} .cmH .s::after{content:'\296E';line-height:18px;font-size:17px} .cmAv{flex-shrink:0;padding:0 6px;width:47px} .cmAv .im{width:35px;height:35px;border-radius:50%;position:relative} .cmIn{flex-grow:1;padding:0 6px;width:calc(100% - 47px);position:relative} .cmBd.del .cmCo{font-style:italic;font-size:90%;line-height:normal;border:1px dashed rgba(0,0,0,.2);border-radius:3px;margin:.5em 0;padding:15px;opacity:.7; overflow:hidden;text-overflow:ellipsis;white-space:nowrap} .cmHr{line-height:24px; overflow:hidden;text-overflow:ellipsis;white-space:nowrap} .cmHr .d{font-size:90%;opacity:.7} .cmHr .d::before{content:'\00B7';margin:0 4px} .cmHr.a .n{display:inline-flex;align-items:center} .cmHr.a .n::after{content:'\2714';display:flex;align-items:center;justify-content:center;width:14px;height:14px;font-size:8px;background:#519bd6;color:#fefefe;border-radius:50%;margin-left:3px} .cmCo{line-height:1.6em;opacity:.9} .cmC i[rel=image]{font-size:90%; display:block;position:relative; min-height:50px; overflow:hidden;text-overflow:ellipsis;white-space:nowrap; margin:1em auto} .cmC i[rel=image]::before{content:'This feature isn\0027t available!';border:1px dashed rgba(0,0,0,.2);border-radius:3px;padding:10px;display:flex;align-items:center;justify-content:center;position:absolute;top:0;left:0;bottom:0;right:0;background:var(--contentB)} .cmC i[rel=pre], .cmC i[rel=quote]{margin-top:1em;margin-bottom:1em; font-style:normal;line-height:inherit;padding:20px} .cmC i[rel=pre]::before{display:block;width:auto} .cmC i[rel=pre]{text-align:left} .cmC i[rel=quote]{display:block;font-style:italic;font-size:inherit;padding:5px 15px} .cmCo img{margin-top:1em;margin-bottom:1em} .cmAc{margin-top:10px} .cmAc a{font-size:90%;color:inherit;opacity:.7;display:inline-flex} .cmAc a::before{content:'\2934';line-height:18px;font-size:16px;transform:rotate(90deg)} .cmAc a::after{content:attr(data-text);margin:0 6px} .cmR{margin:10px 0 0} .cmRp ~ .cmAc, .cmBd.del ~ .cmAc, .onIt:not(.Rtl) .cmHr .date{display:none} .cmRi:checked ~ .cmRp .thTg{margin-bottom:0} .cmRi:checked ~ .cmRp .thTg::before{content:attr(aria-label)} .cmRi:checked ~ .cmRp .thCh, .cmRi:checked ~ .cmRp .cmR{display:none} .cmAl:checked ~ .cm .cmH .s::before{content:attr(data-new)} .cmAl:checked ~ .cm .cmCn >ol{flex-direction:column-reverse} .thTg{display:inline-flex;align-items:center;margin:15px 0 18px;font-size:90%} .thTg::after{content:'';width:20px;border-bottom:1px solid var(--widgetTac);opacity:.5;margin:0 10px} .thTg::before{content:attr(data-text);opacity:.7} .cmCn ol{list-style:none;margin:0;padding:0;display:flex;flex-direction:column} .cmCn li{display:flex;flex-wrap:wrap;padding-bottom:20px;position:relative;width:calc(100% + 12px);left:-6px;right:-6px} .cmCn li .cmRbox{margin-top:20px;padding:0 6px;flex-grow:1} .cmCn li li{padding-bottom:15px;display:block;width:100%;left:0;right:0} .cmCn li li:last-child{padding-bottom:0} .cmCn li li .cmAv{width:20px;margin:2px 0;padding:0;position:absolute} .cmCn li li .cmAv .im{width:20px;height:20px} .cmCn li li .cmIn{width:100%;padding:0} .cmCn li li .cmHr{padding:0 0 0 26px} .cmHl >li >.cmIn::before{content:'';border-left:1px solid var(--contentL);position:absolute;left:-24px;top:40px;height:calc(100% - 25px)} /* Comments Show/Hide */ #comment:target{margin:0;padding-top:60px} .cmSh:checked ~ .cmShw, .cmShw ~ .cm:not(.cmBr), #comment:target .cmShw, #comment:target .cmSh:checked ~ .cm:not(.cmBr){display:none} .cmSh:checked ~ .cm:not(.cmBr), #comment:target .cm:not(.cmBr), #comment:target .cmSh:checked ~ .cmShw{display:block} .cmBtn{display:block;padding:20px;text-align:center;max-width:100%} .cmBtn.ln:hover{color:var(--linkB)} /* Comments Pop-up */ #comment:target .cmSh:checked ~ .cm.cmBr{bottom:-100%;opacity:0;visibility:hidden} #comment:target .cmSh:checked ~ .cm.cmBr .fCls{opacity:0;visibility:hidden}

/* Widget Style */ .widget .imgThm{display:block;position:absolute;top:50%;left:50%;max-width:none;max-height:108%; font-size:12px;text-align:center; transform:translate(-50%, -50%)} .widget .title{margin:0 0 25px; font-size:var(--widgetT);font-weight:var(--widgetTw);position:relative} .widget .title::after{content:'';display:inline-block;vertical-align:middle; width:var(--widgetTa); margin:0 10px;border-bottom:1px solid var(--widgetTac); opacity:.5} .widget input[type=text], .widget input[type=email], .widget textarea{display:block;width:100%;outline:0;border:0;border-bottom:1px solid rgba(0,0,0,.25);border-radius:4px 4px 0 0;background:#f3f3f4; padding:25px 16px 8px 16px; line-height:1.6em; transition:var(--trans-1)} .widget input[type=text]:hover, .widget input[type=email]:hover, .widget textarea:hover{border-color:rgba(0,0,0,.42);background:#ececec} .widget input[type=text]:focus, .widget input[type=email]:focus, .widget textarea:focus, .widget input[data-text=fl], .widget textarea[data-text=fl]{border-color:var(--linkB);background:#ececec} .widget input[type=button], .widget input[type=submit]{display:inline-flex;align-items:center; padding:12px 30px; outline:0;border:0;border-radius:4px; color:#fffdfc; background:var(--linkB); font-size:14px; white-space:nowrap;overflow:hidden;max-width:100%} .widget input[type=button]:hover, .widget input[type=submit]:hover{opacity:.7}

/* Widget BlogSearch */ .srhB .c{border-left:1px solid var(--contentL);padding:0 20px} .srhB .BlogSearch{padding:0} .srhB .BlogSearch:last-child{border:0} .srhB .Label{padding:20px 0} .srhBs{padding-bottom:0} .BlogSearch{border-bottom:1px solid var(--contentL)} .BlogSearch form{position:relative;flex-grow:1} .BlogSearch input{position:relative;display:block;background:var(--srchB);border:0;outline:0;padding:10px 55px;width:100%;height:60px;transition:var(--trans-1);z-index:2} .BlogSearch input[type=search]::-ms-clear,.BlogSearch input[type=search]::-ms-reveal{display:none;appearance:none;width:0;height:0} .BlogSearch input[type=search]::-webkit-search-decoration, .BlogSearch input[type=search]::-webkit-search-cancel-button, .BlogSearch input[type=search]::-webkit-search-results-button, .BlogSearch input[type=search]::-webkit-search-results-decoration{display:none;-webkit-appearance:none;appearance:none} .BlogSearch input:focus ~ button.sb{opacity:.7} .BlogSearch .sb{position:absolute;left:0;top:0;display:flex;align-items:center;padding:0 20px;z-index:3;opacity:.7;height:100%;background:transparent;border:0;outline:0} .BlogSearch .sb svg{width:18px;height:18px;stroke:var(--srchI)} .BlogSearch button.sb{left:auto;right:0;opacity:0;font-size:12px;padding:0 15px} .BlogSearch button.sb::before{content:attr(data-text)}

/* Widget Profile */ .wPrf.sl{position: relative;width: calc(100% + 0px);left: 0px;right: 0px;display: flex;padding: 10px 10px 10px 10px;border-radius: 8px;border:1px solid var(--contentL);box-shadow: 0px 5px 35px rgb(0 0 0 / 10%)} .wPrf.sl .sIm{margin:0 8px;flex-shrink:0} .wPrf.sl .im{width:58px;height:58px;border-radius:26px;margin:0 auto} .wPrf.tm{display:flex;position:relative;width:calc(100% + 4px);left:-2px;right:-2px} .wPrf.tm .sIm{padding:2px;background:var(--contentB);position:relative;border-radius:50%} .wPrf.tm .sIm:not(:first-child){margin-left:-10px} .wPrf.tm .sIm .im, .wPrf.tm .am{width:42px;height:42px;flex-shrink:0;border-radius:50%} .wPrf.tm .sIm::after{content:attr(data-text);position:absolute;bottom:-23px;left:50%;transform:translate(-50%, 0);white-space:nowrap;text-overflow:ellipsis;overflow:hidden;max-width:120px;background:#696969;color:#ebeced;font-size:12px;padding:3px 10px;border-radius:3px;opacity:0;visibility:hidden} .wPrf.tm .sIm:hover::after{opacity:.9;visibility:visible} .wPrf.tm .mIm{display:flex;padding:2px 0} .wPrf.tm .mIm::before{content:'';border-left:1px solid var(--contentL);margin:5px 10px;flex-shrink:0} .wPrf.tm .am{display:flex;align-items:center;justify-content:center;background:var(--transB)} .wPrf.tm .am::before{content:attr(data-text);font-size:12px;opacity:.8} .tmC{display:flex} .prfL{border-radius:8px;padding:8px;transition:var(--trans-1);text-align:center} .prfL::after{content:attr(data-text);font-size:13px;white-space:nowrap;text-overflow:ellipsis;overflow:hidden;max-width:100px;display:block} .prfL .im{width:55px;height:55px;border-radius:50%;margin:0 auto 5px} .sInf{margin:0 8px;flex-grow:1} .sInf .sDt .l{display:inline-flex;align-items:center;color:inherit} .sInf .sTxt{margin:5px auto 0;max-width:320px;font-size:93%;opacity:.9;line-height:1.5em} .sInf .sTxt a{text-decoration:underline} .sInf .lc{display:flex;margin:10px 0 0;opacity:.8;font-size:90%} .sInf .lc svg{width:16px;height:16px} .sInf .lc::after{content:attr(data-text);margin:0 4px}

/* Widget PopularPosts */ .itemPp{counter-reset:p-cnt;border: 0px solid var(--contentL);border-radius: 8px;box-shadow: 0px 5px 35px rgb(0 0 0 / 10%);} .itemPp .iCtnt{display:flex;margin: 0px 10px;padding: 0px 0px 10px 0px;} .itemPp >*{border: 1px solid var(--contentL);border-radius: 8px;box-shadow: 0px 1px 0px rgb(0 0 0 / 7%);margin-bottom:0px} .itemPp .iCtnt::before{flex-shrink:0;content:'0' counter(p-cnt);counter-increment:p-cnt;width:25px;opacity:.9;font-size:120%;color:#2c7ef4;font-weight:bold;line-height:1.4em} .iInr{flex:1 0;width:calc(100% - 25px)} .iTtl{font-size:.95rem;font-weight:700;line-height:1.5em} .iTtmp{display:inline-flex} .iTtmp::after{content:'\2014';margin:0 5px; color:var(--widgetTac);opacity:.7} .iInf{margin:0 25px 8px; overflow:hidden;white-space:nowrap;text-overflow:ellipsis;opacity:.8;margin: 0px 35px;padding: 0px 0px 0px 0px;} .iInf .pLbls{display:inline;opacity:.8}

/* Widget Label */ /* List Label */ div.wL.pSml.bg.ls{border: 1px solid var(--contentL);border-radius: 8px;box-shadow: 0px 5px 35px rgb(0 0 0 / 10%);padding: 10px 10px} .wL ul{display:flex;flex-wrap:wrap; list-style:none;margin:0;padding:0; position:relative;width:calc(100% + 30px);left:-15px;right:-15px; font-size:13px} .wL li{width:calc(50% - 10px); margin:0 5px} .wL li >*{box-shadow: 0 2px 8px 0 rgb(209 208 208);display:flex;align-items:baseline;justify-content:space-between; color:inherit;width:100%; padding:8px 10px;border-radius:4px;line-height:20px} .wL li >* svg{width:18px;height:18px;opacity:.8} .wL li >*:hover svg, .wL li >div svg{/*fill:var(--linkC) !important;*/fill:var(--linkC) !important} .wL li >*:hover .lbC, .wL li >div .lbC{color:var(--linkC)} .wL .lbR{display:inline-flex;align-items:center} .wL .lbR .lbC{margin:0 5px} .wL .lbAl{max-height:0; overflow:hidden; transition:var(--trans-4)} .wL .lbM{display:inline-block; margin-top:10px;line-height:20px; color:var(--linkC)} .wL .lbM::before{content:attr(data-show)} .wL .lbM::after, .wL .lbC::after{content:attr(data-text)} .wL .lbM::after{margin:0 8px} .wL .lbT{overflow:hidden;text-overflow:ellipsis;white-space:nowrap;opacity:.7} .wL .lbC, .wL .lbM::after{flex-shrink:0;font-size:12px;opacity:.7} .lbIn:checked ~ .lbAl{max-height:1000vh} .lbIn:checked ~ .lbM::before{content:attr(data-hide)} .lbIn:checked ~ .lbM::after{visibility:hidden} .wL.bg ul{width:calc(100% + 10px);left:-5px;right:-5px} .wL.bg li{margin-bottom:10px} .wL.bg li >*{background:#ffffff} /* Cloud Label */ .wL.cl{display:flex;flex-wrap:wrap} .wL.cl >*, .wL.cl .lbAl >*{display:block;max-width:100%} .wL.cl .lbAl{display:flex;flex-wrap:wrap} .wL.cl .lbC::before{content:'';margin:0 4px;flex:0 0} .wL.cl .lbN{display:flex;justify-content:space-between; margin:0 0 8px;padding:9px 13px; border:1px solid var(--contentL);border-radius:3px; color:inherit;line-height:20px} .wL.cl .lbN:hover .lbC, .wL.cl div.lbN .lbC{color:var(--linkB); opacity:1} .wL.cl .lbN:not(div):hover, .wL.cl div.lbN{border-color:var(--linkB)} .wL.cl .lbSz{display:flex} .wL.cl .lbSz::after{content:'';margin:0 4px;flex:0 0}

/* Widget ContactForm */ .ContactForm{max-width:500px; font-family:var(--fontB);font-size:14px} .cArea:not(:last-child){margin-bottom:25px} .cArea label{display:block;position:relative} .cArea label .n{display:block;position:absolute;left:0;right:0;top:0; color:rgba(8,16,43,.4);line-height:1.6em;padding:15px 16px 0;border-radius:4px 4px 0 0;transition:var(--trans-1)} .cArea label .n.req::after{content:'*';font-size:85%} .cArea textarea{height:100px} .cArea textarea:focus, .cArea textarea[data-text=fl]{height:200px} .cArea input:focus ~ .n, .cArea textarea:focus ~ .n, .cArea input[data-text=fl] ~ .n, .cArea textarea[data-text=fl] ~ .n{padding-top:5px;color:rgba(8,16,43,.7);font-size:90%;background:#ececec} .cArea .h{display:block;font-size:90%;padding:5px 16px 0;opacity:.7;line-height:normal} .nArea .contact-form-error-message-with-border{color:#d32f2f} .nArea .contact-form-success-message-with-border{color:#2e7b32} 

/* Widget Sliders */ .sldO{position:relative;display:flex;overflow-y:hidden;overflow-x:scroll; scroll-behavior:smooth;scroll-snap-type:x mandatory;list-style:none;margin:0;padding:0; -ms-overflow-style: none} .sldO.no-items{display:none} .sldO.no-items + .section{margin-top:0} .sldO .widget:not(:first-child){margin-top:0} .sldO .widget{position:relative;flex:0 0 100%;width:100%;background:transparent; outline:0;border:0} .sldC{position:relative} .sldS{position:absolute;top:0;left:0;width:100%;height:100%;scroll-snap-align:center;z-index:-1} .sldIm{background-repeat:no-repeat;background-size:cover;background-position:center;background-color:var(--transB);display:block;padding-top:40%;border-radius:3px;color:#fffdfc;font-size:13px} .sldT{position:absolute;bottom:0;left:0;right:0;display:block;padding:20px; background:linear-gradient(0deg, rgba(30,30,30,.1) 0%, rgba(30,30,30,.05) 60%, rgba(30,30,30,0) 100%); border-radius:0 0 3px 3px} .sldS{animation-name:tonext, snap;animation-timing-function:ease;animation-duration:4s;animation-iteration-count:infinite} .sldO .widget:last-child .sldS{animation-name:tostart, snap} .Rtl .sldS{animation-name:tonext-rev, snap} .Rtl .sldO .widget:last-child .sldS{animation-name:tostart-rev, snap} .sldO:hover .widget .sldS, .Rtl .sldO:hover .widget .sldS, .sldO:focus-within .widget .sldS, .Rtl .sldO:focus-within .widget .sldS{animation-name:none} @media (prefers-reduced-motion:reduce){.sldS, .Rtl .sldS{animation-name:none}} @media screen and (max-width:640px){.sldO{width:calc(100% + 40px);left:-20px;right:-20px;padding:0 12.5px 10px} .sldO .widget{flex:0 0 90%;width:90%;margin:0 7.5px; box-shadow:0 10px 8px -8px rgb(0 0 0 / 12%)} .sldT{padding:10px 15px} .sldIm{font-size:12px}}

/* Sticky Ad */ .ancrA{position:fixed;bottom:0;left:0;right:0;min-height:70px;max-height:200px;padding:5px;box-shadow:0 -6px 18px 0 rgba(9,32,76,.1); transition:var(--trans-1);display:flex;align-items:center;justify-content:center;background:#fffdfc;z-index:50;border-top:1px solid var(--contentL)} .ancrC{width:40px;height:30px;display:flex;align-items:center;justify-content:center;border-radius:12px 0 0;border:1px solid var(--contentL);border-bottom:0;border-right:0;position:absolute;right:0;top:-30px;background:inherit} .ancrC::after{content:'\2715';line-height:18px;font-size:14px} .ancrCn{flex-grow:1;overflow:hidden;display:block;position:relative} .ancrI:checked ~ .ancrA{padding:0;min-height:0} .ancrI:checked ~ .ancrA .ancrCn{display:none}

/* Error Page */ .erroP{display:flex;align-items:center;justify-content:center;height:100vh;text-align:center;padding:0} .erroC{width:calc(100% - 40px);max-width:450px;margin:auto;font-family:var(--fontBa)} .erroC h3{font-size:1.414rem;font-family:inherit} .erroC h3 span{display:block;font-size:140px;line-height:.8;margin-bottom:-1rem;color:#ebebf0} .erroC p{margin:30px 5%;line-height:1.6em;opacity:.7} .erroC .button{margin:0;padding-left:2em;padding-right:2em;font-size:14px}

/* Responsive */
@media screen and (min-width:897px){/* Header */ .headL .headN{width:100%} .headL, .headR{z-index:1} .headM .HTML + .PageList, .headL .headIc{display:none} .headM{display:flex;align-items:center;justify-content:center;max-width:calc(100% - 350px);height:100%;position:absolute;left:0;right:0;margin:0 auto} /* mainIn */ .mainIn, .blogM{display:flex} .blogCont{padding-top:30px;padding-bottom:30px} .mainbar{flex:1 0 calc(100% - var(--sideW) - 50px);width:calc(100% - var(--sideW) - 50px); transition:var(--trans-2)} .sidebar{display:flex;flex:0 0 calc(var(--sideW) + 50px);width:calc(var(--sideW) + 50px); margin:0} .sidebar::before{content:'';flex:0 0 50px} .sidebar .sideIn{width:calc(100% - 50px)} /* mainNav */ .mnH{display:none} .mnMob, .mnMn svg:not(.d){display:none} .mnMn{display:block;position:relative;width:calc(100% + 25px);left:-12.5px;right:-12.5px} .mnMn >li{display:inline-flex; align-items:center;margin:0 12.5px;position:relative;white-space:nowrap;height:var(--headerH)} .mnMn >li:hover ul{max-height:100vh; opacity:1;visibility:visible} .mnMn >li:last-child ul{left:auto;border-radius:16px 5px 16px 16px} .mnMn ul{display:block; position:absolute;top:calc(var(--headerH) - 15px);left:-15px;right:-15px; min-width:180px; max-height:0vh; background:var(--contentB); box-shadow:0 10px 20px -10px rgba(0,0,0,.1); border-radius:5px 16px 16px 16px; transition:var(--trans-1); opacity:0;visibility:hidden;z-index:1; overflow:hidden} .mnMn ul li >*{display:block;padding:10px 15px} .mnMn ul li >*:hover{background:var(--transB)} .mnMn .a{display:inline-flex;align-items:center} .mnMn .a:hover{color:var(--linkC)} .mnMn .a:hover::after{opacity:1} .mnMn .a::after{content:'';border-bottom:1px solid var(--linkC);position:absolute;bottom:-1px;left:0;right:0;opacity:0} .mnMn .drp .n::after{content:'';padding:0 3px;flex:0 0}}
@media screen and (min-width:768px){::-webkit-scrollbar{-webkit-appearance:none;width:4px;height:5px}::-webkit-scrollbar-track{background:transparent}::-webkit-scrollbar-thumb{background:rgba(0,0,0,.15);border-radius:10px}::-webkit-scrollbar-thumb:hover{background:rgba(0,0,0,.35)}::-webkit-scrollbar-thumb:active{background:rgba(0,0,0,.35)}}
@media screen and (max-width:1100px) and (min-width: 897px){/* mainIn */ .mainbar{flex:1 0 calc(100% - var(--sideW) - 25px);width:calc(100% - var(--sideW) - 25px)} .sidebar{flex:0 0 calc(var(--sideW) + 25px);width:calc(var(--sideW) + 25px)} .sidebar::before{content:'';flex:0 0 25px} .sidebar .sideIn{width:calc(100% - 25px)}}
@media screen and (max-width:896px){/* mainIn */ .mainbar{margin:0 auto} /* Header */ .ntfC{padding-left:20px;padding-right:20px} .headIn, .navI .secIn{padding:0} .headL{padding:0 0 0 15px;flex-grow:1;width:50%;max-width:none} .headR{padding:0 20px 0 0;flex-grow:0} .headIc .isSrh{display:block} .headL .headN{width:calc(100% - 40px)} /* Scroll Menu */ .navI li{margin:0;padding:8px 0;display:flex} .navI li::before{content:'';padding:10px} .navI ul::after{content:'';display:block;padding:10px;scroll-snap-align:start} .navI .l{position:relative} .navI .l::after{bottom:-8px} .navI a.l:hover::after, .navI .l.a::after{opacity:1} /* mainNav */ .headM{display:flex;justify-content:flex-start;position:fixed;left:0;top:0;bottom:0;margin-left:-100%;z-index:20;transition:var(--trans-1);width:100%;height:100%} .mnBr{margin:15px 15px;width:85%;max-width:480px;height:auto;border-radius:12px 12px 12px 12px;transition:inherit;z-index:3;overflow:hidden;position:relative;box-shadow:0 5px 30px 0 rgba(0,0,0,.05)} .mnBrs{padding:60px 0 0;overflow-y:scroll;overflow-x:hidden;width:100%;height:100%; background:var(--contentB)} .mnH{padding:0 15px} .mnH label{padding:15px 10px} .mnH .c::after{margin:0 13px} .navi:checked ~ .mainWrp .headM{margin-left:0} .navi:checked ~ .mainWrp .headM .fCls{opacity:1;visibility:visible;background:rgba(0,0,0,.2); -webkit-backdrop-filter:saturate(180%) blur(10px); backdrop-filter:saturate(180%) blur(10px)} .mnMob{font-size: 12px;text-align:center;border-top: 1px solid var(--contentL);justify-content:center;align-self:flex-end;position:absolute;left:0;right:0;bottom:0;background:inherit;padding:15px 20px 20px;z-index:1} .mnMob .mSoc{justify-content: center;display:flex;position:relative;width:calc(100% + 14px);left:-7px;right:-7px;margin-top:5px} .mnMob:not(.no-items) + .mnMen{padding-bottom:100px} .mnBr .mMenu{margin-bottom:5px} .mnMen{padding:0 15px 20px} .mMenu >*{display:inline} .mMenu >*:not(:last-child)::after{content:'\00B7';font-size:90%;opacity:.6} .mMenu a:hover{text-decoration:underline} .mSoc >*{position:relative} .mSoc svg{z-index:1} .mSoc svg, .mnMn svg{width:20px;height:20px;opacity:.8} .mSoc span, .mMenu span{opacity:.7} .mnMn >li{position:relative} .mnMn >li.br::after{content:'';display:block;border-bottom:1px solid var(--contentL);margin:12px 5px} .mnMn li:not(.mr) .a:hover, .mnMn ul li >*:hover{background:var(--transB)} .mnMn li:not(.mr) .a:hover, .mnMn ul li a:hover{color:var(--linkC)} .mnMn li:not(.mr) ul{padding-left:30px} .mnMn li ul{display:none;opacity:0;visibility:hidden} .mnMn ul li >*, .mnMn .a{display:flex;align-items:center;padding:10px 5px;position:relative;width:calc(100% + 10px);left:-5px;right:-5px;border-radius:8px;transition:var(--trans-1)} .mnMn ul li >*{padding:10px} .mnMn .a >*{margin:0 5px} .mnMn .a:hover svg:not(.d){fill:var(--linkC)} .mnMn .a:hover svg.line:not(.d){fill:none;stroke:var(--linkC)} .mnMn .n, .mnMn ul li >*{display:block;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;flex:1 0 calc(100% - 64px)} .mnMn .drp.mr .a{font-size:13px;padding-bottom:0;opacity:.7} .mnMn .drp.mr svg.d{display:none} .mnMn .drpI:checked ~ .a svg.d{transform:rotate(180deg)} .mnMn .drpI:checked ~ ul{display:block;opacity:1;visibility:visible} /* Font and Blog */ .pTtl{font-size:1.1rem}}
@media screen and (max-width:640px){/* Header */ .headCn{height:var(--headerHm)} /* Pop-up */ .fixL{align-items:flex-end} .fixL .fixLi, .fixL .cmBri{border-radius:12px 12px 0 0; max-width:680px} .fixL .cmBri:not(.mty){border-radius:0;height:100%;max-height:100%} /* Article */ .onId:not(.grD) .ntry, .itemFt .itm{align-items:flex-start} .onId:not(.grD) .ntry >*, .itemFt .itm >*{flex:0 0 calc(40% - 22px);width:calc(40% - 22px)} .onId .ntry .pInf, .itemFt .itm .pInf{margin-top:10px} .ntry .iFxd .spnr{display:none} .ntry .iFxd{padding:8px 3px} .ntry .iFxd .cmnt{padding:3px} .ntry .iFxd >* svg{padding:1px} /* Footer */ .fotIn >*, .fotIn >*:first-child{width:calc(50% - 30px)}}
@media screen and (max-width:500px){/* Font size */ .iFxd, .crdtIn, .pInf.ps .pDr{font-size:12px} .brdCmb, .navI{font-size:13px} .pDesc{font-size:14px} .pEnt{font-size:var(--postFm)} .pTtl.itm{font-size:var(--postTm)} /* Share */ .pShc a::after{display:none} /* Article */ .onId:not(.grD) .ntry{width:calc(100% + 15px);left:-7.5px;right:-7.5px; flex-direction:row-reverse} .onId:not(.grD) .ntry >*{flex:0 0 calc(40% - 7.5px);width:calc(40% - 7.5px);margin-left:7.5px;margin-right:7.5px} .onId:not(.grD) .ntry .pThmb{flex:0 0 100px} .onId:not(.grD) .ntry .thmb{padding-top:100%} .onId .ntry .pTtl{font-size:1rem} .onId .ntry .pInf{margin-top:12px} .ntry .pSnpt{font-size:13px; /* add display:none; here to hide Snippet in mobile view */} .ntry .pSml{font-size:12px} .pInf.ps .pTtmp::after{content:attr(data-time)} /* oneGrid mode*/ .grD.oGrd .ntry{width:calc(100% - 15px);padding-bottom:0} .grD.oGrd .ntry .pInf{position:relative;margin-top:25px} .grD.oGrd .ntry .pSnpt{font-size:14px} .grD.oGrd .ntry .pSml{font-size:93%} .grD.oGrd .ntry .pTtl{font-size:1.1rem} .grD.oGrd .ntry .iFxd .spnr{display:flex} .grD.oGrd .ntry .iFxd{padding:10px 6px} .grD.oGrd .ntry .iFxd .cmnt{padding:5px} .grD.oGrd .ntry .iFxd >* svg{padding:0} /* Widget Featured */ .itemFt .itm .iThmb{flex:0 0 calc(100% - 25px);margin-bottom:20px} .itemFt .itm .pInf{margin-top:15px} /* Footer */ .fotIn >*, .fotIn >*:first-child{width:calc(100% - 30px)}}

/* Keyframes Animation */ @keyframes shimmer{100%{transform:translateX(100%)}} @keyframes fadein{50%{opacity:1}80%{opacity:1;padding-top:5px;height:22px}100%{opacity:0;padding-top:0;height:0}} @keyframes nudge{0%{transform:translateX(0)}30%{transform:translateX(-5px)}50%{transform:translateX(5px)}70%{transform:translateX(-2px)}100%{transform:translateX(0)}} @keyframes tonext{ 75%{left:0} 95%{left:100%} 98%{left:100%} 99%{left:0}} @keyframes tostart{ 75%{left:0} 95%{left:-300%} 98%{left:-300%} 99%{left:0}} @keyframes tonext-rev{ 75%{right:0} 95%{right:100%} 98%{right:100%} 99%{right:0}} @keyframes tostart-rev{ 75%{right:0} 95%{right:-300%} 98%{right:-300%} 99%{right:0}} @keyframes snap{ 96%{scroll-snap-align:center} 97%{scroll-snap-align:none} 99%{scroll-snap-align:none} 100%{scroll-snap-align:center}} @-webkit-keyframes fadein{50%{opacity:1}80%{opacity:1;padding-top:5px;height:22px}100%{opacity:0;padding-top:0;height:0}} @-webkit-keyframes nudge{0%{transform:translateX(0)}30%{transform:translateX(-5px)}50%{transform:translateX(5px)}70%{transform:translateX(-2px)}100%{transform:translateX(0)}} @-webkit-keyframes tonext{ 75%{left:0} 95%{left:100%} 98%{left:100%} 99%{left:0}} @-webkit-keyframes tostart{ 75%{left:0} 95%{left:-300%} 98%{left:-300%} 99%{left:0}} @-webkit-keyframes tonext-rev{ 75%{right:0} 95%{right:100%} 98%{right:100%} 99%{right:0}} @-webkit-keyframes tostart-rev{ 75%{right:0} 95%{right:-300%} 98%{right:-300%} 99%{right:0}} @-webkit-keyframes snap{ 96%{scroll-snap-align:center} 97%{scroll-snap-align:none} 99%{scroll-snap-align:none} 100%{scroll-snap-align:center}}

/* Noscript Option */ .lazy:not([lazied]){display:none} .noJs{display:flex;justify-content:flex-end;align-items:center;position:fixed;top:20px;left:20px;right:20px;z-index:99;max-width:640px;border-radius:12px;margin:auto;padding:10px 5px;background:#ffdfdf;font-size:13px;box-shadow:0 10px 20px -10px rgba(0,0,0,.1);color:#48525c} .noJs::before{content:attr(data-text);padding:0 10px;flex-grow:1} .noJs label{flex-shrink:0;padding:10px} .noJs label::after{content:'\2715';line-height:18px;font-size:14px} .nJs:checked ~ .noJs{display:none}
/* Hide Scroll */ .scrlH::-webkit-scrollbar{width:0;height:0} .scrlH::-webkit-scrollbar-track{background:transparent} .scrlH::-webkit-scrollbar-thumb{background:transparent;border:none}

/* visitor counter shared by www.wendycode.com */
.pSh{position:relative}
.wendy-view-post{position:absolute;top:16px;right:5px;display:flex;align-items:center;margin:0 5px;padding:0 5px;border-radius: 8px;background:#fff;color:#08102b!important;box-shadow: 0 8px 25px 0 rgb(0 0 0 / 12%)}
.wendy-view-post:after{content:attr(data-view)}
.wendy-view-post svg{fill:none!important;stroke:#2c7ef4!important;stroke-linecap:round;stroke-linejoin:round; stroke-width:1;width:22px;height:22px;margin-right:2px}

/*]]>*/</style>
  
  <b:if cond='data:view.url != data:view.url params { amp: &quot;1&quot; }'>
    <style>/*<![CDATA[*/ /* Dark Mode */ .drK .tDL .d2{display:block} .drK .tDL::after{content:attr(data-light)} .drK .tDL svg .f{stroke:none;fill:var(--darkT)} .drK .pThmb:not(.nul)::before{background-image:linear-gradient(90deg, rgba(0,0,0,0) 0, rgba(0,0,0,.07) 20%, rgba(0,0,0,.1) 60%, rgba(0,0,0,0))} .drK input::placeholder, .drK .cpL input, .drK .cArea label .n{color:rgba(255,255,255,.25)} .drK .nArea .contact-form-error-message-with-border{color:#f94f4f} .drK .cmC i[rel=image]::before, .drK .widget input[type=text], .drK .widget input[type=email], .drK .widget textarea{background:var(--darkBs);border-color:rgba(255,255,255,.15)} .drK .erroC h3 span{color:rgba(255,255,255,.1)} .drK svg, .drK svg.c-1{fill:var(--darkT)} .drK svg.line{fill:none;stroke:var(--darkT)} .drK svg.c-2{fill:var(--darkTalt); opacity:.4} .drK, .drK .headCn{background:var(--darkB);color:var(--darkT)} .drK .ntfC{background:var(--darkBa);color:var(--darkTa)} .drK header, .drK .tbHd, .drK .pRelate, .drK blockquote, .drK .cmC i[rel=quote], .drK blockquote.s-1, .drK details.sp, .drK .ps table:not(.tr-caption-container), .drK .ps table th, .drK .ps table:not(.tr-caption-container) tr:not(:last-child) td, .drK .pre.tb .preH, .drK details.ac, .drK .ancrA, .drK .ancrC, .drK .srhB .c, .drK .BlogSearch, .drK .wPrf.tm .mIm::before, .drK .pSh, .drK .cmBd.del .cmCo, .drK .cmHl >li >.cmIn::before, .drK .cpLb{border-color:rgba(255,255,255,.15)} .drK .pre{background:var(--darkBs);color:var(--darkTa)} .drK .cmC i[rel=pre]{background:var(--darkB);color:var(--darkTa)} .drK footer{background:var(--darkBs);border-color:rgba(255,255,255,.15)} .drK .tIc::after, .drK .shL a, .drK .cpLb{background:rgba(0,0,0,.15)} .drK h1, .drK h2, .drK h3, .drK h4, .drK h5, .drK h6, .drK footer, .drK .button{color:var(--darkT)} .drK .admPs, .drK .dlBox, .drK .fixLs, .drK .cArea input:focus ~ .n, .drK .cArea textarea:focus ~ .n, .drK .cArea input[data-text=fl] ~ .n, .drK .cArea textarea[data-text=fl] ~ .n, .drK .wL.bg li >*{background:var(--darkBs)} .drK .ancrA{background:var(--darkBa)} .drK .button.ln, .drK .navI, .drK .BlogSearch input{background:transparent} .drK::selection, .drK a, .drK .free::after, .drK .new::after, .drK .mnMn li:not(.mr) .a:hover, .drK .mnMn ul li a:hover, .drK .aTtl a:hover, .drK details.ac[open] summary, .drK .cpL label, .drK .wL li >*:hover .lbC, .drK .wL li >div .lbC, .drK .wL .lbM, .drK .cmBtn.ln:hover, .drK .wL.cl .lbN:hover .lbC, .drK .wL.cl div.lbN .lbC{color:var(--darkU)} .drK .wL li >*:hover svg, .drK .wL li >div svg{stroke:var(--darkU)} .drK .toTopF, .drK .blogPg >*, .drK .button, .drK .zmImg::after, .drK .widget input[type=button], .drK .widget input[type=submit]{background:var(--darkU)} .drK .pS input[id*="1"]:checked ~ .tbHd label[for*="1"], .drK .pS input[id*="2"]:checked ~ .tbHd label[for*="2"], .drK .pS input[id*="3"]:checked ~ .tbHd label[for*="3"], .drK .pS input[id*="4"]:checked ~ .tbHd label[for*="4"], .drK .widget input[type=text]:focus, .drK .widget input[type=email]:focus, .drK .widget textarea:focus, .drK .widget input[data-text=fl], .drK .widget textarea[data-text=fl], .drK .wL.cl .lbN:not(div):hover, .drK .wL.cl div.lbN{border-color:var(--darkU)} .drK .button.ln:hover{border-color:var(--darkU);box-shadow:0 0 0 1px var(--darkU) inset} .drK header a, .drK .pLbls >*, .drK .aTtl a, .drK .blogPg >*, .drK .brdCmb a, .drK .wL li >*, .drK .cmAc a, .drK .pShc >*{color:inherit} .drK .blogPg .nPst, .drK .blogPg .current{background:var(--contentL);color:var(--bodyCa)} .drK .wPrf.tm .sIm{background:var(--darkB)} .drK .wPrf.tm .sIm::after{background:var(--darkBa);color:var(--darkTa)} .drK .wPrf.tm .am{background:var(--darkBs)} .drK .bMenu{background-image:linear-gradient(0deg, rgba(30,30,30,.9) 25%, rgba(30,30,30,.75) 50%, rgba(30,30,30,.35) 75%, rgba(30,30,30,.01) 95%)} .drK .bMenu >*:not(.bCmt){background:var(--darkBs)} .drK .bMenu .bCmt{background:var(--darkU)} @media screen and (min-width:897px){.drK .mnMn .a:hover{color:var(--darkU)}.drK .mnMn .a::after{border-color:var(--darkU)} .drK .mnMn ul{background:var(--darkBs)} .drK .mnMn ul li >*:hover{background:rgba(0,0,0,.15)}} @media screen and (max-width:896px){.drK .mnBrs{background:var(--darkBs)} .drK .mnMn .a:hover svg:not(.d){fill:var(--darkU)} .drK .mnMn .a:hover svg.line:not(.d){fill:none;stroke:var(--darkU)} .drK .mnMn li:not(.mr) .a:hover, .drK .mnMn ul li >*:hover{background:rgba(0,0,0,.15)} .drK .mnMn >li.br::after{border-color:rgba(255,255,255,.15)}} @media screen and (max-width:500px){.itemFt .itm .iCtnt{border-color:rgba(255,255,255,.15)}} /*]]>*/</style>
  </b:if>
  
  <b:if cond='data:view.isSingleItem and data:view.url != data:view.url params { amp: &quot;1&quot; }'>
    <style>/*<![CDATA[*/ /* Related Posts */ div.iTtl.aTtl{margin:10px 10px} div.pSnpt{margin:10px 10px} .rPst{margin:40px 0 0} .rPst ul{display:flex;flex-wrap:wrap; position:relative;width:calc(100% + 20px);left:-10px;right:-10px; list-style:none;margin:0;padding:0; counter-reset:p-cnt} .rPst ul li{width:calc(50% - 20px);margin:0 10px 30px;position:relative} .rPst ul.s-2 li, .rPst ul.s-3 li, .rPst ul.s-4 li{width:calc(33.3% - 20px)} .rPst .iF{display:flex;flex-direction:row-reverse;align-items:flex-start;position:relative;width:calc(100% + 15px);left:-7.5px;right:-7.5px} .rPst .iF >*{margin:0 7.5px} .rPst .iF .pThmb{flex:0 0 72px} .rPst .iF .pThmb .thmb{padding-top:100%} .rPst .iF .pCtnt{display:flex;flex-grow:1;width:calc(100% - 102px)} .rPst .iF .pCtnt::before{flex-shrink:0;content:'0' counter(p-cnt);counter-increment:p-cnt;width:25px;opacity:.6;font-size:85%;line-height:1.8em} .rPst .iF .pInf{position:relative;margin-top:8px} .rPst .iF .pInr{flex:1 0;width:calc(100% - 25px)} .rPst .iF .pSnpt{font-size:93%;margin-top:8px} .pTag + .pFoot .rPst .pSnpt{display:none} .rPst .thmb::before{content:'No image';display:block;position:absolute;top:50%;left:50%;max-width:none;max-height:100%;-webkit-transform:translate(-50%, -50%);transform:translate(-50%, -50%); font-size:12px; opacity:.7;white-space:nowrap} .rPst .thmb div{background-position:center;background-size:cover;background-repeat:no-repeat; position:absolute;top:0;left:0;bottom:0;right:0} .rPst .pSnpt{} .rPst .pInf{position:absolute;bottom:0;left:0;right:0} .rPst .pInf::before{position:absolute;bottom:0;left:0;right:0;content:attr(data-date);opacity:.8;margin:10px 10px} .rPst .s-4 li{padding-bottom:30px;border: 1px solid var(--contentL);border-radius: 8px;box-shadow: 0px 5px 35px rgb(0 0 0 / 10%);} @media screen and (max-width:640px){.rPst ul:not(.s-2) li, .rPst ul:not(.s-3) li, .rPst ul:not(.s-4) li{width:calc(100% - 20px)} .rPst .iF{max-width:500px;margin-left:auto;margin-right:auto} .rPst ul.s-2 li, .rPst ul.s-3 li, .rPst ul.s-4 li{width:calc(50% - 20px)}} @media screen and (max-width:500px){.rPst ul{width:calc(100% + 15px);left:-7.5px;right:-7.5px} .rPst ul li{width:calc(50% - 15px);margin:0 7.5px 30px} .rPst ul:not(.s-2) li, .rPst ul:not(.s-3) li, .rPst ul:not(.s-4) li{width:calc(100% - 15px)} .rPst ul.s-2 li{width:calc(50% - 15px)} .rPst ul.s-2 .iTtl, .rPst ul.s-3 .iTtl{flex-grow:1;font-size:14px} .rPst ul.s-3 li{width:100%;margin:0 0 20px} .rPst ul.s-3 .i{display:flex;align-items:center} .rPst ul.s-3 .i >*{flex:0 0 calc(40% + 15px);margin:0 7.5px} .rPst ul.s-3 .iTtl a::after{content:attr(data-text);display:block;margin-top:8px;font-weight:400;font-size:12px;opacity:.7} .rPst ul.s-4{flex-wrap:nowrap;width:calc(100% + 40px);left:-20px;right:-20px;padding:0 12.5px; overflow-y:hidden;overflow-x:scroll;scroll-behavior:smooth;scroll-snap-type:x mandatory; -ms-overflow-style:none;-webkit-overflow-scrolling:touch} .rPst ul.s-4 li{flex-shrink:0;width:80%;margin-bottom:0;scroll-snap-align:center}} /*]]>*/</style>
  </b:if>

  <b:defaultmarkups>
    <!--[ Blogger defaultmarkups ]-->
    <b:defaultmarkup type='Common'>
      
      <!--[ In-feed ad ]-->
      <b:includable id='post-adIn'>
        <div class='ntry pAdin'>
          <!--[ InFeed Ad ]-->
          
          <ins class='adsbygoogle'/>
          <script><ins class='adsbygoogle' data-ad-client='ca-pub-3400053731432707' data-ad-format='auto' data-ad-slot='4052950217' data-full-width-responsive='true' style='display:block'/>
<script>(adsbygoogle = window.adsbygoogle || []).push({});</script></script>
          
        </div>
      </b:includable>
      
      <!--[ Top article ad ]-->
      <b:includable id='post-adTop'>
        <div class='pAd'>
          <!--[ Top article Ad ]-->
          
          <ins class='adsbygoogle'/>
          <script><ins class='adsbygoogle' data-ad-client='ca-pub-3400053731432707' data-ad-format='auto' data-ad-slot='4052950217' data-full-width-responsive='true' style='display:block'/>
<script>
     (adsbygoogle = window.adsbygoogle || []).push({});
</script></script>
          
        </div>
      </b:includable>
      
      <!--[ Bottom article ad ]-->
      <b:includable id='post-adBot'>
        <div class='pAd'>
          <!--[ Bottom article Ad ]-->
          
          <ins class='adsbygoogle'/>
          <script><ins class='adsbygoogle' data-ad-client='ca-pub-3400053731432707' data-ad-format='auto' data-ad-slot='4052950217' data-full-width-responsive='true' style='display:block'/>
<script>
     (adsbygoogle = window.adsbygoogle || []).push({});
</script></script>
          
        </div>
      </b:includable>
      
      <!--[ Matched content Ad ]-->
      <b:includable id='post-relatedAd'>
        <div class='relatedPosts'>
          <!--[ Matched content Ad ]-->
          
          <ins class='adsbygoogle'/>
          <script><ins class='adsbygoogle' data-ad-client='ca-pub-3400053731432707' data-ad-format='auto' data-ad-slot='4052950217' data-full-width-responsive='true' style='display:block'/>
<script>
     (adsbygoogle = window.adsbygoogle || []).push({});
</script></script>
          
        </div>
      </b:includable>
      
      <!--[ Index title ]-->
      <b:includable id='titlePost'>
        <div class='blogTtl'>
          <b:class cond='data:view.isHomepage' name='hm'/>
          <b:if cond='data:view.isHomepage'>
            
            <!--[ Change <data:messages.latestPosts/> to replace 'Latest Posts' with your special text ]-->
            <h3 class='title'><data:messages.latestPosts/></h3>

            <b:else/>
            <div class='t'>
              <b:class cond='data:view.search or data:view.isArchive and data:view.url != data:blog.homepageUrl.canonical path &quot;search&quot;' name='srch'/>
              <b:if cond='data:view.search.label'>
                <span class='hm' expr:data-text='data:messages.home'/><data:blog.pageName/>
                
                <b:elseif cond='data:view.search.query'/>
                <span expr:data-text='data:messages.search + &quot;:&quot;'/><data:view.search.query/>
                
                <b:elseif cond='data:view.isArchive'/>
                <span expr:data-text='data:messages.blogArchive + &quot;:&quot;'/><data:blog.pageName/>
                
                <b:else/>

                <!--[ Change all <data:messages.posts/> to replace 'Posts' with your special text ]-->
                <span class='hm' expr:data-text='data:messages.home'/><data:messages.posts/>
             
              </b:if>
            </div>
          </b:if>
          <b:include name='gridButton'/>
        </div>
      </b:includable>
      
      <!--[ Grid mode button ]-->
      <b:includable id='gridButton'>
        <div class='g'>
          <!--[ Grid/list Button ]-->
          <div class='tGr tIc bIc' data-grid='Grid' data-list='List' onclick='gridMode()'><b:include name='grid-icon'/></div>
          <script>/*<![CDATA[*/ (localStorage.getItem('list')) === 'listmode' ? document.querySelector('#mainCont').classList.remove('grD') : document.querySelector('#mainCont').classList.add('grD') /*]]>*/</script>
        </div>
      </b:includable>
      
      <!--[ Related post ]-->
      <b:includable id='post-related'>
        <div class='rPst' id='rPst'>
          <script>
              var labelArray = [<b:if cond='data:post.labels'><b:loop values='data:post.labels' var='label'>&quot;<data:label.name/>&quot;<b:if cond='data:label.isLast != &quot;true&quot;'>,</b:if></b:loop></b:if>];
              var relatedPostConfig = {
                homePage: &quot;<data:blog.homepageUrl.canonical/>&quot;,
            
                // Replace <data:messages.youMayLikeThesePosts/> to change Related Posts title
                widgetTitle: &quot;<h2 class='title'>Anda mungkin mencari ini</h2>&quot;,
            
                numPosts: 6,
                summaryLength: 180,
                titleLength:&quot;auto&quot;,
                thumbnailSize: 300,
                noImage: &quot;data:image/png;base64,R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs=&quot;,
                containerId: &quot;rPst&quot;,
                newTabLink: false,
                moreText: &quot;Read more&quot;,
            
                // Change the related post style, there are 4 styles available
                widgetStyle: 4,
            
                callBack:function(){}
              }
            </script>
          <script>/*<![CDATA[*/ /*! Related Posts by Taufik Nurrohman dte.web.id */ var randomRelatedIndex,showRelatedPost;(function(n,m,k){var d={widgetTitle:"<h3 class='title'>Related Posts</h3>",widgetStyle:1,homePage:"http://www.trjy17.com",numPosts:7,summaryLength:320,titleLength:"auto",thumbnailSize:200,noImage:"data:image/png;base64,R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs=",containerId:"related-posts",newTabLink:false,moreText:"Read more",callBack:function(){}}; for(var f in relatedPostConfig){d[f]=(relatedPostConfig[f]=="undefined")?d[f]:relatedPostConfig[f]}var j=function(a){var b=m.createElement("script");b.async="async";b.rel="preload";b.src=a;k.appendChild(b)},o=function(b,a){return Math.floor(Math.random()*(a-b+1))+b},l=function(a){var p=a.length,c,b;if(p===0){return false}while(--p){c=Math.floor(Math.random()*(p+1));b=a[p];a[p]=a[c];a[c]=b}return a},e=(typeof labelArray=="object"&&labelArray.length>0)?"/-/"+l(labelArray)[0]:"",h=function(b){var c=b.feed.openSearch$totalResults.$t-d.numPosts,a=o(1,(c>0?c:1));j(d.homePage.replace(/\/$/,"")+"/feeds/posts/summary"+e+"?alt=json-in-script&orderby=updated&start-index="+a+"&max-results="+d.numPosts+"&callback=showRelatedPost")},g=function(z){var s=document.getElementById(d.containerId),x=l(z.feed.entry),A=d.widgetStyle,c=d.widgetTitle+'<ul class="s-'+A+' scrlH">',b=d.newTabLink?' target="_blank"':"",y=d.moreText,v,t,w,r,u;if(!s){return}for(var q=0;q<d.numPosts;q++){if(q==x.length){break}t=x[q].title.$t;w=(d.titleLength!=="auto"&&d.titleLength<t.length)?t.substring(0,d.titleLength)+"&hellip;":t; r=("media$thumbnail"in x[q]&&d.thumbnailSize!==false)?x[q].media$thumbnail.url.replace(/.*?:\/\//g , "//").replace(/\/s[0-9]+(\-c)?/, "/s"+d.thumbnailSize).replace(/\=s[0-9]+(\-c)?/, "=s"+d.thumbnailSize):d.noImage; month=["Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Sep","Oct","Nov","Dec"];date=x[q].published.$t.substring(0,10); Y=date.substring(0, 4); m=date.substring(5, 7); D=date.substring(8, 10); M=month[parseInt(m-1)]; u=("summary"in x[q]&&d.summaryLength>0)?x[q].summary.$t.replace(/<br ?\/?>/g," ").replace(/<.*?>/g,"").replace(/[<>]/g,"").substring(0,d.summaryLength)+"&hellip;":"";for(var p=0,a=x[q].link.length;p<a;p++){v=(x[q].link[p].rel=="alternate")?x[q].link[p].href:"#"} if(A==2){c+='<li><div class="i"><div class="pThmb"><a class="thmb" aria-label="'+w+'" href="'+v+'" title="'+t+'"><div class="lazy" data-style="background-image: url('+r+')"></div></a></div><div class="iTtl aTtl"><a href="'+v+'" '+b+'>'+w+'</a></div></div></li>'} else{if(A==3){c+='<li><div class="i"><div class="pThmb"><a class="thmb" aria-label="'+w+'" href="'+v+'" title="'+t+'"><div class="lazy" data-style="background-image: url('+r+')"></div></a></div><div class="iTtl aTtl"><a href="'+v+'" '+b+' data-date="'+M+' '+D+', '+Y+'" data-text="'+y+'">'+w+'</a></div></div></li>'} else{if(A==4){c+='<li><div class="i"><div class="pThmb"><a class="thmb" aria-label="'+w+'" href="'+v+'" title="'+t+'"><div class="lazy" data-style="background-image: url('+r+')"></div></a></div><div class="iTtl aTtl"><a href="'+v+'" '+b+'>'+w+'</a></div><div class="pSnpt">'+u+'</div><div class="pInf pSml" data-date="'+M+' '+D+', '+Y+'"></div></div></li>'} else{c+='<li><div class="iF"><div class="pThmb"><a class="thmb" aria-label="'+w+'" href="'+v+'" title="'+t+'"><div class="lazy" data-style="background-image: url('+r+')"></div></a></div><div class="pCtnt"><div class="pInr"><div class="iTtl aTtl"><a href="'+v+'" '+b+'>'+w+'</a></div><div class="pSnpt">'+u+'</div><div class="pInf pSml" data-date="'+M+' '+D+', '+Y+'"></div></div></div></div></li>'} }}}s.innerHTML=c+="</ul>";d.callBack()};randomRelatedIndex=h;showRelatedPost=g;j(d.homePage.replace(/\/$/,"")+"/feeds/posts/summary"+e+"?alt=json-in-script&orderby=updated&max-results=0&callback=randomRelatedIndex")})(window,document,document.getElementsByTagName("head")[0]); /*]]>*/</script>
        </div>
      </b:includable>
      
      <!--[ Post authors ]-->
      <b:includable id='post-authorProfile'>
        <div class='admPs'>
          <div class='admIm'>
            <b:include name='post-authorImage'/>
          </div>
          <div class='admI'>
            <bdi class='admN' expr:data-text='data:post.author.name' expr:data-write='data:messages.postedBy'/>
            <div class='admA'>
              <b:eval expr='data:post.author.aboutMe snippet {length: 200, links: true, linebreaks: true}'/>
              <!--<data:post.author.aboutMe/>-->
            </div>
          </div>
        </div>
      </b:includable>
      
      <b:includable id='post-authorImage'>
        <b:if cond='data:post.author.authorPhoto.image'>
          <b:if cond='!data:view.isPost'>
            <div class='im' expr:data-style='&quot;background-image: url(&quot; + resizeImage(data:post.author.authorPhoto.image,20,&quot;1:1&quot;) + &quot;)&quot;'>
              <b:class cond='data:view.url != data:view.url params { amp: &quot;1&quot; }' name='lazy'/>
              <b:attr cond='data:view.url == data:view.url params { amp: &quot;1&quot; }' expr:value='&quot;background-image: url(&quot; + resizeImage(data:post.author.authorPhoto.image,20,&quot;1:1&quot;) + &quot;)&quot;' name='style'/>
            </div>
            <noscript><div class='im' expr:style='&quot;background-image: url(&quot; + resizeImage(data:post.author.authorPhoto.image,20,&quot;1:1&quot;) + &quot;)&quot;'/></noscript>
            <b:else/>
            <div class='im lazy' expr:data-style='&quot;background-image: url(&quot; + resizeImage(data:post.author.authorPhoto.image,40,&quot;1:1&quot;) + &quot;)&quot;'>
              <b:class cond='data:view.url != data:view.url params { amp: &quot;1&quot; }' name='lazy'/>
              <b:attr cond='data:view.url == data:view.url params { amp: &quot;1&quot; }' expr:value='&quot;background-image: url(&quot; + resizeImage(data:post.author.authorPhoto.image,20,&quot;1:1&quot;) + &quot;)&quot;' name='style'/>
            </div>
            <noscript><div class='im' expr:style='&quot;background-image: url(&quot; + resizeImage(data:post.author.authorPhoto.image,40,&quot;1:1&quot;) + &quot;)&quot;'/></noscript>
          </b:if>
          <b:elseif cond='!data:view.isMultipleItems'/>
          <div class='im'><b:include name='profile-icon'/></div>
        </b:if>
      </b:includable>
      
      <b:includable id='post-authorName'>
        <bdi class='nm' expr:data-text='data:post.author.name' expr:data-write='data:widgets.Blog.first.allBylineItems.author.label'/>
        
        <!--[ Post Author with Link ]-->
        <!--<b:tag class='nm' expr:data-text='data:post.author.name' expr:data-write='data:widgets.Blog.first.allBylineItems.author.label' expr:name='data:post.author.profileUrl ? &quot;a&quot; : &quot;span&quot;'>
          <b:attr cond='data:post.author.profileUrl' expr:value='data:post.author.name' name='aria-label'/>
          <b:attr cond='data:post.author.profileUrl' expr:value='data:post.author.profileUrl' name='href'/>
          <b:attr cond='data:post.author.profileUrl' value='author noreferrer' name='rel'/>
          <b:attr cond='data:post.author.profileUrl' value='_blank' name='target'/>
        </b:tag>-->
      </b:includable>
      
      <!--[ Post article ]-->
      <b:includable id='postHeaders'>
        <div class='pHdr pSml'>
          <b:class cond='!data:widgets.Blog.first.allBylineItems.author and !data:widgets.Blog.first.allBylineItems.labels' name='nHdr'/>
          <b:if cond='data:widgets.Blog.first.allBylineItems.author and data:post.labels none (label =&gt; label.name in [&quot;Sponsored&quot; ])'>
            <b:tag class='aIm' cond='data:post.author.authorPhoto.image' name='div'><b:include name='post-authorImage'/></b:tag>
          </b:if>
          <div class='aNm'>
            <b:class cond='!data:post.author.authorPhoto.image' name='n'/>
            <b:include cond='data:widgets.Blog.first.allBylineItems.author and data:post.labels none (label =&gt; label.name in [&quot;Sponsored&quot; ])' name='post-authorName'/>
            <b:include name='postLabelorSponsor'/>
          </div>
        </div>
      </b:includable>
      
      <b:includable id='postCommentsLinks'>
        <b:if cond='data:post.allowComments and data:post.numberOfComments &gt; 0'>
          <a class='cmnt' expr:aria-label='data:messages.comments' expr:data-text='data:post.numberOfComments' expr:href='data:post.url.canonical fragment &quot;comment&quot;' role='button'>
            <b:include name='chat-icon'/>
          </a>
        </b:if>
      </b:includable>
      
      <b:includable id='postCommentsUrl'>
        <b:if cond='data:post.allowComments and data:post.numberOfComments &gt; 0'>
          <a class='cmnt' expr:aria-label='data:messages.comments' expr:data-text='data:post.numberOfComments' expr:href='data:post.url.canonical fragment &quot;comment&quot;' role='button'>
            <b:class cond='data:view.isSingleItem' name='tIc'/>
            <b:include name='chat-icon'/>
          </a>
        </b:if>
      </b:includable>
      
      <b:includable id='postCommentsLabel'>
        <b:if cond='data:post.allowComments and data:post.numberOfComments &gt; 0'>
          <label class='cmnt' expr:data-text='data:post.numberOfComments' for='forComments'>
            <b:class cond='data:view.isSingleItem' name='tIc'/>
            <b:include name='chat-icon'/>
          </label>
        </b:if>
      </b:includable>
      
      <b:includable id='postCommentsLabela'>
        <b:if cond='data:post.allowComments and data:post.numberOfComments &gt; 0'>
          <label class='cmnt' expr:data-text='data:post.numberOfComments' for='forComments'>
            <b:class cond='data:view.isSingleItem' name='tIc'/>
            <b:include name='chata-icon'/>
          </label>
        </b:if>
      </b:includable>
      
      <b:includable id='postSponsored'>
        <div class='spnr'>
          <b:include name='link-icon'/>
        </div>
      </b:includable>
      
      <b:includable id='postLabelSponsored'>
        <div class='pLbls nSpr'>
          <b:loop index='s' values='data:post.labels' var='label'>
            <b:if cond='data:s == 0'>
              <b:tag expr:data-text='data:label.name' name='span'/>
            </b:if>
          </b:loop>
        </div>
      </b:includable>
      
      <b:includable id='postLabel'>
        <b:if cond='data:widgets.Blog.first.allBylineItems.labels'>
          <div class='pLbls'>
            <b:attr cond='data:post.labels' expr:value='data:widgets.Blog.first.allBylineItems.labels.label' name='data-text'/>
            <b:loop index='i' values='data:post.labels' var='label'>
              <b:if cond='data:i &lt;= 1'>
                <b:tag expr:data-text='data:label.name' expr:name='data:blog.url != data:label.url ? &quot;a&quot; : &quot;span&quot;'>
                  <b:attr cond='data:blog.url != data:label.url' expr:value='data:label.url.canonical' name='href'/>
                  <b:attr cond='data:blog.url != data:label.url' name='rel' value='tag'/>
                  <b:attr cond='data:blog.url != data:label.url' expr:value='data:label.name' name='aria-label'/>
                </b:tag>
              </b:if>
            </b:loop>
          </div>
        </b:if>
      </b:includable>
      
      <b:includable id='postLabelorSponsor'>
        <b:if cond='data:post.labels none (label =&gt; label.name in [ &quot;Sponsored&quot; ])'>
          <!--[ Post labels ]-->
          <b:include cond='data:post.labels' name='postLabel'/>
          <b:else/>
          <b:include name='postLabelSponsored'/>
        </b:if>
      </b:includable>
      
      <b:includable id='postJumpLinks'>
        <a class='pJmp' expr:aria-label='data:blog.jumpLinkMessage' expr:data-text='data:messages.keepReading' expr:href='data:post.url.canonical'/>
      </b:includable>
      
      <b:includable id='postTimestampPublish'>
        <time class='aTtmp pTtmp pbl' expr:data-text='format(data:post.date, &quot;MMM d, y&quot;)' expr:datetime='data:post.date.iso8601' expr:title='&quot;Published: &quot; + data:post.date format &quot;MMMM d, y&quot;'/>
      </b:includable>
      
      <b:includable id='postTimestamps'>
        <b:if cond='data:post.lastUpdated != data:post.date'>
          <time class='aTtmp pTtmp upd' data-date='Update:' expr:data-text='format(data:post.lastUpdated, &quot;MMMM d, y&quot;)' expr:data-time='format(data:post.lastUpdated, &quot;MMM d, y&quot;)' expr:datetime='data:post.lastUpdated.iso8601' expr:title='&quot;Last updated: &quot; + data:post.lastUpdated format &quot;MMMM d, y&quot;'/>
          <b:else/>
          <time class='aTtmp pTtmp pbl' expr:data-text='format(data:post.date, &quot;MMMM d, y&quot;)' expr:data-time='format(data:post.lastUpdated, &quot;MMM d, y&quot;)' expr:datetime='data:post.date.iso8601' expr:title='&quot;Published: &quot; + data:post.date format &quot;MMMM d, y&quot;'/>
            </b:if>
          </b:includable>
      
      <b:includable id='postFontInput'>
        <input class='fnti fontS1 hidden' id='fontS1' name='entryFont' type='radio'/>
        <input checked='checked' class='fnti fontS2 hidden' id='fontS2' name='entryFont' type='radio'/>
        <input class='fnti fontS3 hidden' id='fontS3' name='entryFont' type='radio'/>
      </b:includable>
      
      <b:includable id='postFontEntry'>
        <input class='fnIn fixi hidden' id='forFont' type='checkbox'/>
        <div class='fnB fixL'>
          <div class='fnBr fixLi'>
            <div class='fnBs fixLs'>
              <div class='fnH fixH fixT' data-text='Change font size'>
                <label aria-label='Close' class='c cl' for='forFont'/>
              </div>
              <ul class='fnC'>
                <li><label class='fnt1' for='fontS1'/></li>
                <li><label class='fnt2' for='fontS2'/></li>
                <li><label class='fnt3' for='fontS3'/></li>
              </ul>
            </div>
          </div>
          
          <label class='fCls' for='forFont'/>
        </div>
      </b:includable>
      
      <b:includable id='postEntrySnippet'>
        <b:eval expr='snippet(data:post.snippets.long, {length: 150, links: false, linebreaks: false})'/>
        <!--<b:eval expr='snippet(data:post.body, {length: 90, links: false, linebreaks: false})'/>-->
      </b:includable>
      
      <b:includable id='postEntryThumbnail'>
        <b:if cond='data:post.featuredImage.isYoutube'>
          <img class='imgThm lazy' expr:alt='data:post.title ? data:post.title : data:messages.image' expr:data-src='data:post.featuredImage.youtubeMaxResDefaultUrl.isResizable ? resizeImage(data:post.featuredImage.youtubeMaxResDefaultUrl, 600, &quot;18:9&quot;) : data:post.featuredImage.youtubeMaxResDefaultUrl' src='data:image/png;base64,R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs='/>
          <noscript><img class='imgThm' expr:alt='data:post.title ? data:post.title : data:messages.image' expr:src='data:post.featuredImage.youtubeMaxResDefaultUrl.isResizable ? resizeImage(data:post.featuredImage.youtubeMaxResDefaultUrl, 600, &quot;18:9&quot;) : data:post.featuredImage.youtubeMaxResDefaultUrl'/></noscript>
          <b:else/>          
          <img class='imgThm lazy' expr:alt='data:post.title ? data:post.title : data:messages.image' expr:data-src='data:post.featuredImage.isResizable ? resizeImage(data:post.featuredImage, 600, &quot;18:9&quot;) : data:post.featuredImage' src='data:image/png;base64,R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs='/>
          <noscript><img class='imgThm' expr:alt='data:post.title ? data:post.title : data:messages.image' expr:src='data:post.featuredImage.isResizable ? resizeImage(data:post.featuredImage, 600, &quot;18:9&quot;) : data:post.featuredImage'/></noscript>
        </b:if>
      </b:includable>
      
      <!--[ Bottom post menu ]-->
      <b:includable id='post-bottomMenu'>
        <div class='bMenu'>
          <label class='bBt bIc' for='forFont'><b:include name='font-icon'/></label>
          <b:if cond='data:post.shareUrl and data:widgets.Blog.first.allBylineItems.share'>
            <label class='bBt bIc' for='forShare'><b:include name='share-icon'/></label>
          </b:if>
          <b:if cond='data:post.allowComments and data:widgets.Blog.first.allBylineItems.comments'>
            <label class='bBt bCmt bIc' for='forComments'>
              <b:if cond='data:post.numberOfComments &gt; 0'>
                <b:message name='messages.numberOfComments'>
                  <b:param expr:value='data:post.numberOfComments' name='numComments'/>
                </b:message>
                <b:else/>
                <data:messages.postAComment/>
              </b:if>
            </label>
          </b:if>
        </div>
      </b:includable>
      
      <!--[ Comment button ]-->
      <b:includable id='post-commentButton'>
        <!--[ Show/hide Comment ]-->
        <div class='cmShw'>
          <label class='cmBtn button' for='forComments'>
            <!--[ Delete tag bellow to change button style ]-->
            <b:class name='ln'/>
          
            <b:if cond='data:post.numberOfComments &gt; 0'>
              <span><data:messages.joinTheConversation/> (<data:post.numberOfComments/>)</span>
              <b:else/>
              <data:messages.postAComment/>
            </b:if>
          </label>
        </div>
      </b:includable>
      
      <!--[ Comment disqus ]-->
      <b:includable id='post-commentDisqus'>
        <div class='cmDisqus' id='disqus_thread'>
          <div class='cmBtn button' id='disqusshow' onclick='load_Comments()'>
            <!--[ Delete tag bellow to change button style ]-->
            <b:class name='ln'/>
            
            <span><data:messages.joinTheConversation/></span>
          </div>
        </div>
        <script>/*<![CDATA[*/ var disqus_shortname = "jagodesain"; !function(){var e=document.createElement("script");e.defer=!0,e.src="//"+disqus_shortname+".disqus.com/blogger_item.js",(document.getElementsByTagName("head")[0]||document.getElementsByTagName("body")[0]).appendChild(e)}(); function load_Comments(){var e=document.getElementById("disqusshow");e.style.display="none";var t="jagodesain";!function(){var e=document.createElement("script");e.defer=!0,e.src="https://"+t+".disqus.com/embed.js",(document.getElementsByTagName("head")[0]||document.getElementsByTagName("body")[0]).appendChild(e)}()}; var uri = window.location.toString(); if (uri.indexOf("?m=1","?m=1") > 0) {var clean_uri = uri.substring(0, uri.indexOf("?m=1"));window.history.replaceState({}, document.title, clean_uri); }; /*]]>*/</script>
      </b:includable>
      
      <!--[ Comment disqus on-scroll ]-->
      <b:includable id='post-commentDisqusScroll'>
        <div class='cmDisqus' id='disqus_thread'>
          <div id='disqus_empty'/>
        </div>
        
        <!--[ Disqus script by bungfrangki.com, change 'jagodesain' with your disqus_shortname ]-->
        <script>var disqus_blogger_current_url = &quot;<data:blog.canonicalUrl/>&quot;; if (!disqus_blogger_current_url.length) {disqus_blogger_current_url = &quot;<data:blog.url/>&quot;;} var disqus_blogger_homepage_url = &quot;<data:blog.canonicalHomepageUrl/>&quot;; var disqus_blogger_canonical_homepage_url = &quot;<data:blog.canonicalHomepageUrl/>&quot;;</script>
        <script>/*<![CDATA[*/ function load_disqus( disqus_shortname ) {var y = document.getElementById('disqus_empty'), t = document.getElementById('disqus_thread'), e = document.createElement('script'), d = document.createElement('script'), h = (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]); if( t && y ) {e.async = true; e.src = '//' + disqus_shortname + '.disqus.com/embed.js'; h.appendChild(e); d.async = !0; d.src = '//' + disqus_shortname + '.disqus.com/blogger_item.js'; h.appendChild(d); y.remove(); } }; window.addEventListener('scroll', function(e) {var currentScroll = document.scrollingElement.scrollTop; var t = document.getElementById('disqus_thread'); if( t && (currentScroll > t.getBoundingClientRect().top - 150) ) {load_disqus('jagodesain'); console.log('Disqus loaded.'); }}, false); var uri = window.location.toString(); if (uri.indexOf("?m=1","?m=1") > 0) {var clean_uri = uri.substring(0, uri.indexOf("?m=1"));window.history.replaceState({}, document.title, clean_uri); }; /*]]>*/</script>
      </b:includable>
      
      <!--[ Comment FB ]-->
      <b:includable id='post-commentFB'>        
        <div id='fb-root'/>
        <script src='http://connect.facebook.net/en_US/all.js#xfbml=1' type='deferjs'/>
        <div id='commentFB'><fb:comments expr:href='data:post.url' num_posts='10' width='650'/></div>
        <script>/*<![CDATA[*/ var uri = window.location.toString(); if (uri.indexOf("?m=1","?m=1") > 0) {var clean_uri = uri.substring(0, uri.indexOf("?m=1"));window.history.replaceState({}, document.title, clean_uri); }; /*]]>*/</script>
      </b:includable>
      
      <!--[ Loadmore pagination ]-->
      <b:includable id='post-paginationMore'>
        <script> /*! Simple AJAX infinite scroll by Taufik Nurrohman dte.web.id */ !function(t,e){t.InfiniteScroll=function(n){function r(t,n){return n=n||e,n.querySelectorAll(t)}function o(t){return void 0!==t}function a(t){return&quot;function&quot;==typeof t}function i(t,e){t=t||{};for(var n in e)t[n]=&quot;object&quot;==typeof e[n]?i(t[n],e[n]):e[n];return t}function s(t,e,n){return o(t)?o(e)?void(o(n)?g[t][n]=e:g[t].push(e)):g[t]:g}function d(t,e){o(e)?delete g[t][e]:g[t]=[]}function l(t,e){if(o(g[t]))for(var n in g[t])g[t][n](e)}function c(){return L.innerHTML=p.text.loading,v=!0,M?(y.classList.add(p.state.loading),l(&quot;loading&quot;,[p]),void u(M,function(t,n){y.className=x+&quot; &quot;+p.state.load,h=e.createElement(&quot;div&quot;),h.innerHTML=t;var o=r(&quot;title&quot;,h),a=r(p.target.post,h),i=r(p.target.anchors+&quot; &quot;+p.target.anchor,h),s=r(p.target.post,H);if(o=o&amp;&amp;o[0]?o[0].innerHTML:&quot;&quot;,a.length&amp;&amp;s.length){var d=s[s.length-1];e.title=o,d.insertAdjacentHTML(&quot;afterend&quot;,&quot; &quot;),h=e.createElement(&quot;div&quot;);for(var c=0,u=a.length;u&gt;c;++c)h.appendChild(a[c]);d.insertAdjacentHTML(&quot;afterend&quot;,h.innerHTML),f(),M=i.length?i[0].href:!1,v=!1,q++,l(&quot;load&quot;,[p,t,n])}},function(t,e){y.classList.add(p.state.error),v=!1,f(1),l(&quot;error&quot;,[p,t,e])})):(y.classList.add(p.state.loaded),L.innerHTML=p.text.loaded,l(&quot;loaded&quot;,[p]))}function f(t){if(L.innerHTML=&quot;&quot;,T){h.innerHTML=p.text[t?&quot;error&quot;:&quot;load&quot;];var e=h.firstChild;e.onclick=function(){return 2===p.type&amp;&amp;(T=!1),c(),!1},L.appendChild(e)}}var u=&quot;infinite-scroll-state-&quot;,p={target:{posts:&quot;.posts&quot;,post:&quot;.post&quot;,anchors:&quot;.anchors&quot;,anchor:&quot;.anchor&quot;},text:{load:&quot;%s&quot;,loading:&quot;%s&quot;,loaded:&quot;%s&quot;,error:&quot;%s&quot;},state:{load:u+&quot;load&quot;,loading:u+&quot;loading&quot;,loaded:u+&quot;loaded&quot;,error:u+&quot;error&quot;}},g={load:[],loading:[],loaded:[],error:[]};p=i(p,n||{}),p.on=s,p.off=d;var h=null,u=function(e,n,r){if(t.XMLHttpRequest){var o=new XMLHttpRequest;o.onreadystatechange=function(){if(4===o.readyState){if(200!==o.status)return void(r&amp;&amp;a(r)&amp;&amp;r(o.responseText,o));n&amp;&amp;a(n)&amp;&amp;n(o.responseText,o)}},o.open(&quot;GET&quot;,e),o.send()}},T=1!==p.type,v=!1,H=r(p.target.posts)[0],L=r(p.target.anchors)[0],M=r(p.target.anchor,L),m=e.body,y=e.documentElement,x=y.className||&quot;&quot;,E=H.offsetTop+H.offsetHeight,j=t.innerHeight,A=0,b=null,q=1;if(M.length){M=M[0].href,H.insertAdjacentHTML(&quot;afterbegin&quot;,&quot; &quot;),h=e.createElement(&quot;div&quot;),f();var w=function(){E=H.offsetTop+H.offsetHeight,j=t.innerHeight,A=m.scrollTop||y.scrollTop,v||E&gt;A+j||c()};w(),0!==p.type&amp;&amp;t.addEventListener(&quot;scroll&quot;,function(){T||(b&amp;&amp;t.clearTimeout(b),b=t.setTimeout(w,200))},!1)}return p}}(window,document);
if(typeof InfiniteScroll !== &quot;undefined&quot;) { var infinite_scroll = new InfiniteScroll ({ type: 0,
target: { posts: &quot;.blogPts&quot;, post: &quot;.ntry&quot;, anchors: &quot;.blogPg&quot;, anchor: &quot;.olLnk&quot;},
text: {
load: &quot;<a class='jsLd' expr:aria-label='data:messages.loadMorePosts' expr:data-text='data:messages.loadMorePosts' href='javascript:;'/>&quot;,
loading: &quot;<div class='jsLd wait nPst' expr:data-text='data:messages.loading'><svg viewBox='0 0 50 50' x='0px' y='0px'><path d='M25.251,6.461c-10.318,0-18.683,8.365-18.683,18.683h4.068c0-8.071,6.543-14.615,14.615-14.615V6.461z'><animateTransform attributeName='transform' attributeType='xml' dur='0.6s' from='0 25 25' repeatCount='indefinite' to='360 25 25' type='rotate'/></path></svg></div>&quot;,
loaded: &quot;<div class='jsLd nPst' expr:data-text='data:messages.noResultsFound'/>&quot;,
error: &quot;<a class='jsLd error' expr:aria-label='data:messages.loadMorePosts' expr:data-text='data:messages.moreEllipsis' href='javascript:;'/>&quot;} }); }</script>
      </b:includable>
        
      <!--[ Single page condition ]-->
      <b:includable id='post-singlePage'>
        <style>/*<![CDATA[*/ .mainbar{flex-basis:100%} .sidebar{display:none; flex:0 0 530px;margin:50px auto 0} .sidebar::before{display:none} .sideIn{width:100%} /*]]>*/</style>
      </b:includable>
        
      <!--[ SVG Icon ]-->      
      <b:includable id='back-icon'>
        <!--[ Back icon ]-->
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(12.000000, 12.000000) rotate(-270.000000) translate(-12.000000, -12.000000) translate(5.000000, 8.500000)'><path d='M14,0 C14,0 9.856,7 7,7 C4.145,7 0,0 0,0'/></g></svg>
      </b:includable>
      
      <b:includable id='forward-icon'>
        <!--[ Forward icon ]-->
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(12.000000, 12.000000) rotate(-90.000000) translate(-12.000000, -12.000000) translate(5.000000, 8.500000)'><path d='M14,0 C14,0 9.856,7 7,7 C4.145,7 0,0 0,0'/></g></svg>
      </b:includable>
      
      <b:includable id='arrow-right-icon'>
        <!--[ Arrow right icon ]-->
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(12.000000, 12.000000) rotate(-90.000000) translate(-12.000000, -12.000000) translate(5.500000, 4.000000)'><line x1='6.7743' x2='6.7743' y1='15.7501' y2='0.7501'/><path d='M12.7988,9.6998 C12.7988,9.6998 9.5378,15.7498 6.7758,15.7498 C4.0118,15.7498 0.7498,9.6998 0.7498,9.6998'/></g></svg>
      </b:includable>
      
      <b:includable id='arrow-left-icon'>
        <!--[ Arrow left icon ]-->
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(12.000000, 12.000000) rotate(-270.000000) translate(-12.000000, -12.000000) translate(5.500000, 4.000000)'><line x1='6.7743' x2='6.7743' y1='15.7501' y2='0.7501'/><path d='M12.7988,9.6998 C12.7988,9.6998 9.5378,15.7498 6.7758,15.7498 C4.0118,15.7498 0.7498,9.6998 0.7498,9.6998'/></g></svg>
      </b:includable>
      
      <b:includable id='arow-down-icon'>
        <!--[ Arrow down icon ]-->
        <svg class='line d' viewBox='0 0 24 24'><g transform='translate(5.000000, 8.500000)'><path d='M14,0 C14,0 9.856,7 7,7 C4.145,7 0,0 0,0'/></g></svg>
      </b:includable>
      
      <b:includable id='arow-up-icon'>
        <!--[ Arrow up icon ]-->
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(12.000000, 12.000000) rotate(-180.000000) translate(-12.000000, -12.000000) translate(5.000000, 8.500000)'><path d='M14,0 C14,0 9.856,7 7,7 C4.145,7 0,0 0,0'/></g></svg>
      </b:includable>
      
      <!--[ Profile icon ]-->
      <b:includable id='profile-icon'>
        <svg class='line' viewBox='0 0 24 24'><path d='M12 12C14.7614 12 17 9.76142 17 7C17 4.23858 14.7614 2 12 2C9.23858 2 7 4.23858 7 7C7 9.76142 9.23858 12 12 12Z'/><path d='M20.5899 22C20.5899 18.13 16.7399 15 11.9999 15C7.25991 15 3.40991 18.13 3.40991 22'/></svg>
      </b:includable>
      
      <!--[ Profile Circle icon ]-->
      <b:includable id='profile-circle-icon'>
        <svg class='line' viewBox='0 0 24 24'><path d='M12.12 12.78C12.05 12.77 11.96 12.77 11.88 12.78C10.12 12.72 8.71997 11.28 8.71997 9.50998C8.71997 7.69998 10.18 6.22998 12 6.22998C13.81 6.22998 15.28 7.69998 15.28 9.50998C15.27 11.28 13.88 12.72 12.12 12.78Z'/><path d='M18.74 19.3801C16.96 21.0101 14.6 22.0001 12 22.0001C9.40001 22.0001 7.04001 21.0101 5.26001 19.3801C5.36001 18.4401 5.96001 17.5201 7.03001 16.8001C9.77001 14.9801 14.25 14.9801 16.97 16.8001C18.04 17.5201 18.64 18.4401 18.74 19.3801Z'/><path d='M12 22C17.5228 22 22 17.5228 22 12C22 6.47715 17.5228 2 12 2C6.47715 2 2 6.47715 2 12C2 17.5228 6.47715 22 12 22Z'/></svg>
      </b:includable>
      
      <!--[ Profiles icon ]-->
      <b:includable id='profiles-icon'>
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(2.749500, 2.549500)'><path d='M6.809,18.9067 C3.137,18.9067 9.41469125e-14,18.3517 9.41469125e-14,16.1277 C9.41469125e-14,13.9037 3.117,11.8997 6.809,11.8997 C10.481,11.8997 13.617,13.8847 13.617,16.1077 C13.617,18.3307 10.501,18.9067 6.809,18.9067 Z'/><path d='M6.809,8.728 C9.219,8.728 11.173,6.774 11.173,4.364 C11.173,1.954 9.219,-2.48689958e-14 6.809,-2.48689958e-14 C4.399,-2.48689958e-14 2.44496883,1.954 2.44496883,4.364 C2.436,6.766 4.377,8.72 6.778,8.728 L6.809,8.728 Z'/><path d='M14.0517,7.5293 C15.4547,7.1543 16.4887007,5.8753 16.4887007,4.3533 C16.4897,2.7653 15.3627,1.4393 13.8647,1.1323'/><path d='M14.7113,11.104 C16.6993,11.104 18.3973,12.452 18.3973,13.655 C18.3973,14.364 17.8123,15.092 16.9223,15.301'/></g></svg>
      </b:includable>
      
      <!--[ Search icon ]-->
      <b:includable id='search-icon'>
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(2.000000, 2.000000)'><circle cx='9.76659044' cy='9.76659044' r='8.9885584'/><line x1='16.0183067' x2='19.5423342' y1='16.4851259' y2='20.0000001'/></g></svg>
      </b:includable>
      
      <!--[ Share icon ]-->
      <b:includable id='share-icon'>
        <svg class='line' viewBox='0 0 24 24'><path d='M16.44 8.8999C20.04 9.2099 21.51 11.0599 21.51 15.1099V15.2399C21.51 19.7099 19.72 21.4999 15.25 21.4999H8.73998C4.26998 21.4999 2.47998 19.7099 2.47998 15.2399V15.1099C2.47998 11.0899 3.92998 9.2399 7.46998 8.9099'/><path d='M12 15.0001V3.62012'/><path d='M15.35 5.85L12 2.5L8.65002 5.85'/></svg>
      </b:includable>
      
      <!--[ Share icon ]-->
      <b:includable id='share-alt-icon'>
        <svg class='line' viewBox='0 0 24 24'><path d='M92.30583,264.72053a3.42745,3.42745,0,0,1-.37,1.57,3.51,3.51,0,1,1,0-3.13995A3.42751,3.42751,0,0,1,92.30583,264.72053Z' transform='translate(-83.28571 -252.73452)'/><circle cx='18.48892' cy='5.49436' r='3.51099'/><circle cx='18.48892' cy='18.50564' r='3.51099'/><line class='cls-3' x1='12.53012' x2='8.65012' y1='8.476' y2='10.416'/><line class='cls-3' x1='12.53012' x2='8.65012' y1='15.496' y2='13.556'/></svg>
      </b:includable>
      
      <!--[ Font icon ]-->
      <b:includable id='font-icon'>
        <svg viewBox='0 0 24 24'><path d='M16.928 4.8L22 19.41h-3.31l-1.104-3.483h-5.133l-1.124 3.482H8.26L13.334 4.8h3.594zM8.19 8.974l.952 2.741-1.077 3.102-1.162-3.673h-.13l-1.309 4.093h2.455l-.585 1.684h-2.34L4.19 19.41H2L5.623 8.974H8.19zm6.936-1.137h-.183l-1.832 5.73h3.827l-1.812-5.73z'/></svg>
      </b:includable>
      
      <!--[ Instagram icon ]-->
      <b:includable id='instagram-icon'>
        <svg viewBox='0 0 32 32'><path d='M22,3H10a7,7,0,0,0-7,7V22a7,7,0,0,0,7,7H22a7,7,0,0,0,7-7V10A7,7,0,0,0,22,3Zm5,19a5,5,0,0,1-5,5H10a5,5,0,0,1-5-5V10a5,5,0,0,1,5-5H22a5,5,0,0,1,5,5Z'/><path d='M16,9.5A6.5,6.5,0,1,0,22.5,16,6.51,6.51,0,0,0,16,9.5Zm0,11A4.5,4.5,0,1,1,20.5,16,4.51,4.51,0,0,1,16,20.5Z'/><circle cx='23' cy='9' r='1'/></svg>
      </b:includable>
      
      <!--[ Facebook icon ]-->
      <b:includable id='facebook-icon'>
        <svg viewBox='0 0 32 32'><path d='M24,3H8A5,5,0,0,0,3,8V24a5,5,0,0,0,5,5H24a5,5,0,0,0,5-5V8A5,5,0,0,0,24,3Zm3,21a3,3,0,0,1-3,3H17V18h4a1,1,0,0,0,0-2H17V14a2,2,0,0,1,2-2h2a1,1,0,0,0,0-2H19a4,4,0,0,0-4,4v2H12a1,1,0,0,0,0,2h3v9H8a3,3,0,0,1-3-3V8A3,3,0,0,1,8,5H24a3,3,0,0,1,3,3Z'/></svg>
      </b:includable>
      
      <!--[ Facebook rounded icon ]-->
      <b:includable id='facebook-r-icon'>
        <svg viewBox='0 0 64 64'><path d='M20.1,36h3.4c0.3,0,0.6,0.3,0.6,0.6V58c0,1.1,0.9,2,2,2h7.8c1.1,0,2-0.9,2-2V36.6c0-0.3,0.3-0.6,0.6-0.6h5.6 c1,0,1.9-0.7,2-1.7l1.3-7.8c0.2-1.2-0.8-2.4-2-2.4h-6.6c-0.5,0-0.9-0.4-0.9-0.9v-5c0-1.3,0.7-2,2-2h5.9c1.1,0,2-0.9,2-2V6.2 c0-1.1-0.9-2-2-2h-7.1c-13,0-12.7,10.5-12.7,12v7.3c0,0.3-0.3,0.6-0.6,0.6h-3.4c-1.1,0-2,0.9-2,2v7.8C18.1,35.1,19,36,20.1,36z'/></svg>
      </b:includable>
      
      <!--[ Twitter icon ]-->
      <b:includable id='twitter-icon'>
        <svg viewBox='0 0 32 32'><path d='M13.35,28A13.66,13.66,0,0,1,2.18,22.16a1,1,0,0,1,.69-1.56l2.84-.39A12,12,0,0,1,5.44,4.35a1,1,0,0,1,1.7.31,9.87,9.87,0,0,0,5.33,5.68,7.39,7.39,0,0,1,7.24-6.15,7.29,7.29,0,0,1,5.88,3H29a1,1,0,0,1,.9.56,1,1,0,0,1-.11,1.06L27,12.27c0,.14,0,.28-.05.41a12.46,12.46,0,0,1,.09,1.43A13.82,13.82,0,0,1,13.35,28ZM4.9,22.34A11.63,11.63,0,0,0,13.35,26,11.82,11.82,0,0,0,25.07,14.11,11.42,11.42,0,0,0,25,12.77a1.11,1.11,0,0,1,0-.26c0-.22.05-.43.06-.65a1,1,0,0,1,.22-.58l1.67-2.11H25.06a1,1,0,0,1-.85-.47,5.3,5.3,0,0,0-4.5-2.51,5.41,5.41,0,0,0-5.36,5.45,1.07,1.07,0,0,1-.4.83,1,1,0,0,1-.87.2A11.83,11.83,0,0,1,6,7,10,10,0,0,0,8.57,20.12a1,1,0,0,1,.37,1.05,1,1,0,0,1-.83.74Z'/></svg>
      </b:includable>
      
      <!--[ Twitter rounded icon ]-->
      <b:includable id='twitter-r-icon'>
        <svg viewBox='0 0 64 64'><path d='M11.4,26.6C11.5,26.6,11.5,26.6,11.4,26.6c-0.9,0-1.8-0.2-2.6-0.4c-1.3-0.4-2.5,0.8-2.1,2 c1.1,4.3,4.5,7.7,8.8,8.6c-1,0.3-2,0.4-3,0.4c-1,0-1.7,1.1-1.2,2c1.9,3.5,5.6,5.9,9.7,6h1c1.1,0,2,0.9,2,2c0,1.1-0.9,2-2,2 c-1.3,0-2.9-0.1-4.5-0.5c-1-0.2-2-0.2-2.9,0.1c-1.7,0.6-3.5,1.1-5.4,1.3C8.5,50.2,8,50.7,8,51.4v0c0,0.5,0.3,1,0.8,1.2 c3.9,1.7,8.3,2.7,12.9,2.7c21.1,0,32.7-17.9,32.7-33.5v0c0-0.9,0.4-1.8,1.1-2.4c1.2-1,2.3-2.1,3.3-3.4c0.4-0.5-0.1-1.2-0.7-1 c-1.2,0.4-2.4,0.7-3.7,0.9c-0.2,0-0.3-0.2-0.1-0.4c1.5-1.1,2.8-2.6,3.6-4.3c0.3-0.6-0.3-1.2-0.9-0.9c-1.1,0.6-2.3,1-3.5,1.4 c-1.2,0.4-2.6,0.1-3.6-0.7c-1.9-1.5-4.4-2.4-7-2.4c-5.3,0-9.8,3.7-11.1,8.8c-0.2,0.9,0.5,1.7,1.4,1.7c1.6-0.1,3.2-0.3,4.4-0.5 c1-0.2,2,0.3,2.4,1.2c0.5,1.2-0.2,2.4-1.3,2.7c-4.6,1.3-9.7,0.4-9.7,0.4l0,0C21.2,21.8,14.3,18,9.3,12.5C8.6,11.7,7.3,12,7,12.9 c-0.4,1.2-0.6,2.5-0.6,3.9C6.4,20.9,8.4,24.5,11.4,26.6z'/></svg>
      </b:includable>
      
      <!--[ Telegram icon ]-->
      <b:includable id='telegram-icon'>
        <svg viewBox='0 0 32 32'><path d='M24,28a1,1,0,0,1-.62-.22l-6.54-5.23a1.83,1.83,0,0,1-.13.16l-4,4a1,1,0,0,1-1.65-.36L8.2,18.72,2.55,15.89a1,1,0,0,1,.09-1.82l26-10a1,1,0,0,1,1,.17,1,1,0,0,1,.33,1l-5,22a1,1,0,0,1-.65.72A1,1,0,0,1,24,28Zm-8.43-9,7.81,6.25L27.61,6.61,5.47,15.12l4,2a1,1,0,0,1,.49.54l2.45,6.54,2.89-2.88-1.9-1.53A1,1,0,0,1,13,19a1,1,0,0,1,.35-.78l7-6a1,1,0,1,1,1.3,1.52Z'/></svg>
      </b:includable>
      
      <!--[ Telegram rounded icon ]-->
      <b:includable id='telegram-r-icon'>
        <svg viewBox='0 0 64 64'><path d='M56.4,8.2l-51.2,20c-1.7,0.6-1.6,3,0.1,3.5l9.7,2.9c2.1,0.6,3.8,2.2,4.4,4.3l3.8,12.1c0.5,1.6,2.5,2.1,3.7,0.9 l5.2-5.3c0.9-0.9,2.2-1,3.2-0.3l11.5,8.4c1.6,1.2,3.9,0.3,4.3-1.7l8.7-41.8C60.4,9.1,58.4,7.4,56.4,8.2z M50,17.4L29.4,35.6 c-1.1,1-1.9,2.4-2,3.9c-0.2,1.5-2.3,1.7-2.8,0.3l-0.9-3c-0.7-2.2,0.2-4.5,2.1-5.7l23.5-14.6C49.9,16.1,50.5,16.9,50,17.4z'/></svg>
      </b:includable>
      
      <!--[ Tiktok icon ]-->
      <b:includable id='tiktok-icon'>
        <svg viewBox='0 0 32 32'><path d='M24,3H8A5,5,0,0,0,3,8V24a5,5,0,0,0,5,5H24a5,5,0,0,0,5-5V8A5,5,0,0,0,24,3Zm3,21a3,3,0,0,1-3,3H8a3,3,0,0,1-3-3V8A3,3,0,0,1,8,5H24a3,3,0,0,1,3,3Z'/><path d='M22,12a3,3,0,0,1-3-3,1,1,0,0,0-2,0V19a3,3,0,1,1-3-3,1,1,0,0,0,0-2,5,5,0,1,0,5,5V13a4.92,4.92,0,0,0,3,1,1,1,0,0,0,0-2Z'/></svg>
      </b:includable>
      
      <!--[ Tumblr icon ]-->
      <b:includable id='tumblr-icon'>
        <svg viewBox='0 0 32 32'><path d='M16,2A14,14,0,1,0,30,16,14,14,0,0,0,16,2Zm0,26A12,12,0,1,1,28,16,12,12,0,0,1,16,28Z'/><path d='M20,19a1,1,0,0,0-1,1,1,1,0,0,1-1,1H17a1,1,0,0,1-1-1V15h3a1,1,0,0,0,0-2H16V10a1,1,0,0,0-2,0v3H12a1,1,0,0,0,0,2h2v5a3,3,0,0,0,3,3h1a3,3,0,0,0,3-3A1,1,0,0,0,20,19Z'/></svg>
      </b:includable>
      
      <!--[ line icon ]-->
      <b:includable id='line-icon'>
        <svg viewBox='0 0 32 32'><path d='M16,2C8.28,2,2,7.38,2,14c0,5.48,4.34,10.24,10.44,11.6L12,28.87a1,1,0,0,0,.37.91A1,1,0,0,0,13,30a1,1,0,0,0,.35-.06C14,29.68,30,23.58,30,14,30,7.38,23.72,2,16,2ZM14.22,27.4l.33-2.47a1,1,0,0,0-.83-1.12C8.09,22.91,4,18.78,4,14,4,8.49,9.38,4,16,4S28,8.49,28,14C28,20.61,18.14,25.66,14.22,27.4Z'/><path d='M10,15.25H8.75V12a.75.75,0,0,0-1.5,0v4a.76.76,0,0,0,.75.75h2a.75.75,0,0,0,0-1.5Z'/><path d='M24,12.75a.75.75,0,0,0,0-1.5H22a.76.76,0,0,0-.75.75v4a.76.76,0,0,0,.75.75h2a.75.75,0,0,0,0-1.5H22.75v-.5H24a.75.75,0,0,0,0-1.5H22.75v-.5Z'/><path d='M13,11.25a.76.76,0,0,0-.75.75v4a.75.75,0,0,0,1.5,0V12A.76.76,0,0,0,13,11.25Z'/><path d='M19,11.25a.76.76,0,0,0-.75.75v1.75l-1.65-2.2a.75.75,0,0,0-1.35.45v4a.75.75,0,0,0,1.5,0V14.25l1.65,2.2a.75.75,0,0,0,.6.3.67.67,0,0,0,.24,0,.75.75,0,0,0,.51-.71V12A.76.76,0,0,0,19,11.25Z'/></svg>
      </b:includable>
      
      <!--[ Line rounded icon ]-->
      <b:includable id='line-r-icon'>
        <svg viewBox='0 0 24 24'><path d='M19.365 9.863c.349 0 .63.285.63.631 0 .345-.281.63-.63.63H17.61v1.125h1.755c.349 0 .63.283.63.63 0 .344-.281.629-.63.629h-2.386c-.345 0-.627-.285-.627-.629V8.108c0-.345.282-.63.63-.63h2.386c.346 0 .627.285.627.63 0 .349-.281.63-.63.63H17.61v1.125h1.755zm-3.855 3.016c0 .27-.174.51-.432.596-.064.021-.133.031-.199.031-.211 0-.391-.09-.51-.25l-2.443-3.317v2.94c0 .344-.279.629-.631.629-.346 0-.626-.285-.626-.629V8.108c0-.27.173-.51.43-.595.06-.023.136-.033.194-.033.195 0 .375.104.495.254l2.462 3.33V8.108c0-.345.282-.63.63-.63.345 0 .63.285.63.63v4.771zm-5.741 0c0 .344-.282.629-.631.629-.345 0-.627-.285-.627-.629V8.108c0-.345.282-.63.63-.63.346 0 .628.285.628.63v4.771zm-2.466.629H4.917c-.345 0-.63-.285-.63-.629V8.108c0-.345.285-.63.63-.63.348 0 .63.285.63.63v4.141h1.756c.348 0 .629.283.629.63 0 .344-.282.629-.629.629M24 10.314C24 4.943 18.615.572 12 .572S0 4.943 0 10.314c0 4.811 4.27 8.842 10.035 9.608.391.082.923.258 1.058.59.12.301.079.766.038 1.08l-.164 1.02c-.045.301-.24 1.186 1.049.645 1.291-.539 6.916-4.078 9.436-6.975C23.176 14.393 24 12.458 24 10.314'/></svg>
      </b:includable>
      
      <!--[ Youtube icon ]-->
      <b:includable id='youtube-icon'>
        <svg viewBox='0 0 32 32'><path d='M29.73,9.9A5,5,0,0,0,25.1,5.36a115.19,115.19,0,0,0-18.2,0A5,5,0,0,0,2.27,9.9a69,69,0,0,0,0,12.2A5,5,0,0,0,6.9,26.64c3,.24,6.06.36,9.1.36s6.08-.12,9.1-.36a5,5,0,0,0,4.63-4.54A69,69,0,0,0,29.73,9.9Zm-2,12A3,3,0,0,1,25,24.65a113.8,113.8,0,0,1-17.9,0,3,3,0,0,1-2.78-2.72,65.26,65.26,0,0,1,0-11.86A3,3,0,0,1,7.05,7.35C10,7.12,13,7,16,7s6,.12,9,.35a3,3,0,0,1,2.78,2.72A65.26,65.26,0,0,1,27.73,21.93Z'/><path d='M21.45,15.11l-8-4A1,1,0,0,0,12,12v8a1,1,0,0,0,.47.85A1,1,0,0,0,13,21a1,1,0,0,0,.45-.11l8-4a1,1,0,0,0,0-1.78ZM14,18.38V13.62L18.76,16Z'/></svg>        
      </b:includable>
      
      <!--[ LinkedIn icon ]-->
      <b:includable id='linkedIn-icon'>
        <svg viewBox='0 0 32 32'><path d='M24,3H8A5,5,0,0,0,3,8V24a5,5,0,0,0,5,5H24a5,5,0,0,0,5-5V8A5,5,0,0,0,24,3Zm3,21a3,3,0,0,1-3,3H8a3,3,0,0,1-3-3V8A3,3,0,0,1,8,5H24a3,3,0,0,1,3,3Z'/><path d='M11,14a1,1,0,0,0-1,1v6a1,1,0,0,0,2,0V15A1,1,0,0,0,11,14Z'/><path d='M19,13a4,4,0,0,0-4,4v4a1,1,0,0,0,2,0V17a2,2,0,0,1,4,0v4a1,1,0,0,0,2,0V17A4,4,0,0,0,19,13Z'/><circle cx='11' cy='11' r='1'/></svg>        
      </b:includable>
      
      <!--[ LinkedIn rounded icon ]-->
      <b:includable id='linkedIn-r-icon'>
        <svg viewBox='0 0 64 64'><path d='M8,54.7C8,55.4,8.6,56,9.3,56h9.3c0.7,0,1.3-0.6,1.3-1.3V23.9c0-0.7-0.6-1.3-1.3-1.3H9.3 c-0.7,0-1.3,0.6-1.3,1.3V54.7z'/><path d='M46.6,22.3c-4.5,0-7.7,1.8-9.4,3.7c-0.4,0.4-1.1,0.1-1.1-0.5l0-1.6c0-0.7-0.6-1.3-1.3-1.3h-9.4 c-0.7,0-1.3,0.6-1.3,1.3c0.1,5.7,0,25.4,0,30.7c0,0.7,0.6,1.3,1.3,1.3h9.5c0.7,0,1.3-0.6,1.3-1.3V37.9c0-1,0-2,0.3-2.7 c0.8-2,2.6-4.1,5.7-4.1c4.1,0,6,3.1,6,7.6v15.9c0,0.7,0.6,1.3,1.3,1.3h9.3c0.7,0,1.3-0.6,1.3-1.3V37.4C60,27.1,54.1,22.3,46.6,22.3 z'/><path d='M13.9,18.9L13.9,18.9c3.8,0,6.1-2.4,6.1-5.4C19.9,10.3,17.7,8,14,8c-3.7,0-6,2.3-6,5.4 C8,16.5,10.3,18.9,13.9,18.9z'/></svg>
      </b:includable>
      
      <!--[ Whatsapp icon ]-->
      <b:includable id='whatsapp-icon'>
        <svg viewBox='0 0 32 32'><path d='M16,2A13,13,0,0,0,8,25.23V29a1,1,0,0,0,.51.87A1,1,0,0,0,9,30a1,1,0,0,0,.51-.14l3.65-2.19A12.64,12.64,0,0,0,16,28,13,13,0,0,0,16,2Zm0,24a11.13,11.13,0,0,1-2.76-.36,1,1,0,0,0-.76.11L10,27.23v-2.5a1,1,0,0,0-.42-.81A11,11,0,1,1,16,26Z'/><path d='M19.86,15.18a1.9,1.9,0,0,0-2.64,0l-.09.09-1.4-1.4.09-.09a1.86,1.86,0,0,0,0-2.64L14.23,9.55a1.9,1.9,0,0,0-2.64,0l-.8.79a3.56,3.56,0,0,0-.5,3.76,10.64,10.64,0,0,0,2.62,4A8.7,8.7,0,0,0,18.56,21a2.92,2.92,0,0,0,2.1-.79l.79-.8a1.86,1.86,0,0,0,0-2.64Zm-.62,3.61c-.57.58-2.78,0-4.92-2.11a8.88,8.88,0,0,1-2.13-3.21c-.26-.79-.25-1.44,0-1.71l.7-.7,1.4,1.4-.7.7a1,1,0,0,0,0,1.41l2.82,2.82a1,1,0,0,0,1.41,0l.7-.7,1.4,1.4Z'/></svg>
      </b:includable>
      
      <!--[ Whatsapp rounded icon ]-->
      <b:includable id='whatsapp-r-icon'>
        <svg viewBox='0 0 64 64'><path d='M6.9,48.4c-0.4,1.5-0.8,3.3-1.3,5.2c-0.7,2.9,1.9,5.6,4.8,4.8l5.1-1.3c1.7-0.4,3.5-0.2,5.1,0.5 c4.7,2.1,10,3,15.6,2.1c12.3-1.9,22-11.9,23.5-24.2C62,17.3,46.7,2,28.5,4.2C16.2,5.7,6.2,15.5,4.3,27.8c-0.8,5.6,0,10.9,2.1,15.6 C7.1,44.9,7.3,46.7,6.9,48.4z M21.3,19.8c0.6-0.5,1.4-0.9,1.8-0.9s2.3-0.2,2.9,1.2c0.6,1.4,2,4.7,2.1,5.1c0.2,0.3,0.3,0.7,0.1,1.2 c-0.2,0.5-0.3,0.7-0.7,1.1c-0.3,0.4-0.7,0.9-1,1.2c-0.3,0.3-0.7,0.7-0.3,1.4c0.4,0.7,1.8,2.9,3.8,4.7c2.6,2.3,4.9,3,5.5,3.4 c0.7,0.3,1.1,0.3,1.5-0.2c0.4-0.5,1.7-2,2.2-2.7c0.5-0.7,0.9-0.6,1.6-0.3c0.6,0.2,4,1.9,4.7,2.2c0.7,0.3,1.1,0.5,1.3,0.8 c0.2,0.3,0.2,1.7-0.4,3.2c-0.6,1.6-2.1,3.1-3.2,3.5c-1.3,0.5-2.8,0.7-9.3-1.9c-7-2.8-11.8-9.8-12.1-10.3c-0.3-0.5-2.8-3.7-2.8-7.1 C18.9,22.1,20.7,20.4,21.3,19.8z'/></svg>
      </b:includable>
      
      <!--[ Pinterest icon ]-->
      <b:includable id='pinterest-icon'>
        <svg viewBox='0 0 32 32'><path d='M16,2A14,14,0,1,0,30,16,14,14,0,0,0,16,2Zm0,26a12,12,0,0,1-3.81-.63l1.2-4.81A7.93,7.93,0,0,0,16,23a8.36,8.36,0,0,0,1.4-.12,8,8,0,1,0-9.27-6.49,1,1,0,0,0,2-.35,6,6,0,1,1,3.79,4.56L15,16.24A1,1,0,1,0,13,15.76l-2.7,10.81A12,12,0,1,1,16,28Z'/></svg>
      </b:includable>
      
      <!--[ Pinteres rounded icon ]-->
      <b:includable id='pinterest-r-icon'>
        <svg viewBox='0 0 64 64'><path d='M14.4,53.8c2.4,2,6.1,0.6,6.8-2.4l0-0.1c0.4-1.8,2.4-10.2,3.2-13.7c0.2-0.9,0.2-1.8-0.1-2.7 C24.2,34,24,32.8,24,31.5c0-4.1,2.4-7.2,5.4-7.2c2.5,0,3.8,1.9,3.8,4.2c0,2.6-1.6,6.4-2.5,9.9c-0.7,3,1.5,5.4,4.4,5.4 c5.3,0,8.9-6.8,8.9-14.9c0-6.1-4.1-10.7-11.6-10.7c-8.5,0-13.8,6.3-13.8,13.4c0,2.4,0.7,4.2,1.8,5.5c0.5,0.6,0.6,0.9,0.4,1.6 c-0.1,0.5-0.4,1.8-0.6,2.2c-0.2,0.7-0.8,1-1.4,0.7c-3.9-1.6-5.7-5.9-5.7-10.7c0-8,6.7-17.5,20-17.5c10.7,0,17.7,7.7,17.7,16 c0,11-6.1,19.2-15.1,19.2c-1.9,0-3.8-0.7-5.2-1.6c-0.9-0.6-2.1-0.1-2.4,0.9c-0.5,1.9-1.1,4.3-1.3,4.9c-0.1,0.5-0.3,0.9-0.4,1.4 c-1,2.7,0.9,5.5,3.7,5.7c2.1,0.1,4.2,0,6.3-0.3c12.4-2,22.1-12.2,23.4-24.7C61.5,18.1,48.4,4,32,4C16.5,4,4,16.5,4,32 C4,40.8,8.1,48.6,14.4,53.8z'/></svg>
      </b:includable>
      
      <!--[ Mail rounded icon ]-->
      <b:includable id='mail-r-icon'>
        <svg viewBox='0 0 500 500'><path d='M468.051,222.657c0-12.724-5.27-24.257-13.717-32.527 L282.253,45.304c-17.811-17.807-46.702-17.807-64.505,0L45.666,190.129c-8.448,8.271-13.717,19.803-13.717,32.527v209.054 c0,20.079,16.264,36.341,36.34,36.341h363.421c20.078,0,36.34-16.262,36.34-36.341V222.657z M124.621,186.402h250.758 c11.081,0,19.987,8.905,19.987,19.991v34.523c-0.088,4.359-1.818,8.631-5.181,11.997l-55.966,56.419l83.224,83.127 c6.904,6.904,6.904,18.081,0,24.985s-18.085,6.904-24.985,0l-85.676-85.672H193.034l-85.492,85.672 c-6.907,6.904-18.081,6.904-24.985,0c-6.906-6.904-6.906-18.081,0-24.985l83.131-83.127l-55.875-56.419 c-3.638-3.638-5.363-8.358-5.181-13.177v-33.343C104.632,195.307,113.537,186.402,124.621,186.402z'/></svg>
      </b:includable>
      
      <!--[ Circle icon ]-->
      <b:includable id='circle-icon'>
        <svg viewBox='0 0 32 32'><path d='M16,2A14,14,0,1,0,30,16,14,14,0,0,0,16,2Zm0,26A12,12,0,1,1,28,16,12,12,0,0,1,16,28Z'/><path d='M16,9.5A6.5,6.5,0,1,0,22.5,16,6.51,6.51,0,0,0,16,9.5Zm0,11A4.5,4.5,0,1,1,20.5,16,4.51,4.51,0,0,1,16,20.5Z'/></svg>
      </b:includable>
      
      <!--[ Home icon ]-->
      <b:includable id='home-icon'>
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(2.400000, 2.000000)'><line x1='6.6787' x2='12.4937' y1='14.1354' y2='14.1354'/><path d='M1.24344979e-14,11.713 C1.24344979e-14,6.082 0.614,6.475 3.919,3.41 C5.365,2.246 7.615,0 9.558,0 C11.5,0 13.795,2.235 15.254,3.41 C18.559,6.475 19.172,6.082 19.172,11.713 C19.172,20 17.213,20 9.586,20 C1.959,20 1.24344979e-14,20 1.24344979e-14,11.713 Z'/></g></svg>
      </b:includable>
      
      <!--[ Home alt icon ]-->
      <b:includable id='home-alt-icon'>
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(2.400000, 2.000000)'><path d='M1.24344979e-14,11.713 C1.24344979e-14,6.082 0.614,6.475 3.919,3.41 C5.365,2.246 7.615,0 9.558,0 C11.5,0 13.795,2.235 15.254,3.41 C18.559,6.475 19.172,6.082 19.172,11.713 C19.172,20 17.213,20 9.586,20 C1.959,20 1.24344979e-14,20 1.24344979e-14,11.713 Z'/></g></svg>
      </b:includable>
      
      <!--[ Folder icon ]-->
      <b:includable id='folder-icon'>
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(2.500000, 2.500000)'><line x1='6.6787' x2='12.4937' y1='12.0742685' y2='12.0742685'/><path d='M-1.13686838e-13,5.29836453 C-1.13686838e-13,2.85645977 1.25,0.75931691 3.622,0.272650243 C5.993,-0.214968804 7.795,-0.0463973758 9.292,0.761221672 C10.79,1.56884072 10.361,2.76122167 11.9,3.63645977 C13.44,4.51265024 15.917,3.19645977 17.535,4.94217405 C19.229,6.7697931 19.2200005,9.57550739 19.2200005,11.3640788 C19.2200005,18.1602693 15.413,18.6993169 9.61,18.6993169 C3.807,18.6993169 -1.13686838e-13,18.2288407 -1.13686838e-13,11.3640788 L-1.13686838e-13,5.29836453 Z'/></g></svg>
      </b:includable>
      
      <!--[ Message icon ]-->
      <b:includable id='message-icon'>
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(2.452080, 2.851980)'><path d='M15.0928322,6.167017 C15.0928322,6.167017 11.8828071,10.0196486 9.53493746,10.0196486 C7.18807029,10.0196486 3.941955,6.167017 3.941955,6.167017'/><path d='M1.04805054e-13,9.11679198 C1.04805054e-13,2.27869674 2.38095238,8.8817842e-15 9.52380952,8.8817842e-15 C16.6666667,8.8817842e-15 19.047619,2.27869674 19.047619,9.11679198 C19.047619,15.9538847 16.6666667,18.233584 9.52380952,18.233584 C2.38095238,18.233584 1.04805054e-13,15.9538847 1.04805054e-13,9.11679198 Z'/></g></svg>
      </b:includable>
      
      <!--[ Paper icon ]-->
      <b:includable id='paper-icon'>
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(3.649800, 2.749900)'><line x1='10.6555' x2='5.2555' y1='12.6999' y2='12.6999'/><line x1='8.6106' x2='5.2546' y1='8.6886' y2='8.6886'/><path d='M16.51,5.55 L10.84,0.15 C10.11,0.05 9.29,0 8.39,0 C2.1,0 -1.95399252e-14,2.32 -1.95399252e-14,9.25 C-1.95399252e-14,16.19 2.1,18.5 8.39,18.5 C14.69,18.5 16.79,16.19 16.79,9.25 C16.79,7.83 16.7,6.6 16.51,5.55 Z'/><path d='M10.2844,0.0827 L10.2844,2.7437 C10.2844,4.6017 11.7904,6.1067 13.6484,6.1067 L16.5994,6.1067'/></g></svg>
      </b:includable>
      
      <!--[ Document icon ]-->
      <b:includable id='document-icon'>
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(3.610000, 2.750100)'><line x1='11.9858' x2='4.7658' y1='12.9463' y2='12.9463'/><line x1='11.9858' x2='4.7658' y1='9.1865' y2='9.1865'/><line x1='7.521' x2='4.766' y1='5.4272' y2='5.4272'/><path d='M7.63833441e-14,9.25 C7.63833441e-14,16.187 2.098,18.5 8.391,18.5 C14.685,18.5 16.782,16.187 16.782,9.25 C16.782,2.313 14.685,0 8.391,0 C2.098,0 7.63833441e-14,2.313 7.63833441e-14,9.25 Z'/></g></svg>
      </b:includable>
      
      <!--[ Buy icon ]-->
      <b:includable id='buy-icon'>
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(3.650200, 2.850200)'><path d='M2.044,3.58024493 C7.3705141,2.243 13.9926469,2.32498848 15.5231061,4.06777179 C17.0535652,5.8105551 17.0220031,11.638 15.2330031,13.237 C13.4450031,14.836 5.68,14.988 3.22,13.237 C0.621,11.386 2.129,5.692 2.044,2.243 C2.095,0.313 -1.13686838e-13,0 -1.13686838e-13,0'/><line x1='10.5059' x2='13.2789' y1='7.8696' y2='7.8696'/><path d='M3.6138,17.2773 C3.9138,17.2773 4.1578,17.5213 4.1578,17.8213 C4.1578,18.1223 3.9138,18.3663 3.6138,18.3663 C3.3128,18.3663 3.0688,18.1223 3.0688,17.8213 C3.0688,17.5213 3.3128,17.2773 3.6138,17.2773 Z'/><path d='M13.9453,17.2773 C14.2463,17.2773 14.4903,17.5213 14.4903,17.8213 C14.4903,18.1223 14.2463,18.3663 13.9453,18.3663 C13.6453,18.3663 13.4013,18.1223 13.4013,17.8213 C13.4013,17.5213 13.6453,17.2773 13.9453,17.2773 Z'/></g></svg>
      </b:includable>
      
      <!--[ Download icon ]-->
      <b:includable id='download-icon'>
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(2.000000, 2.000000)'><line x1='9.8791' x2='9.8791' y1='12.791' y2='0.75'/><polyline points='12.7951 9.8642 9.8791 12.7922 6.9631 9.8642'/><path d='M14.3703,5.2587 C17.9493,5.5887 19.2503,6.9287 19.2503,12.2587 C19.2503,19.3587 16.9393,19.3587 10.0003,19.3587 C3.0593,19.3587 0.7503,19.3587 0.7503,12.2587 C0.7503,6.9287 2.0503,5.5887 5.6303,5.2587'/></g></svg>
      </b:includable>
      
      <!--[ Download alt icon ]-->
      <b:includable id='download-alt-icon'>
        <svg class='line' viewBox='0 0 24 24'><polyline points='8 17 12 21 16 17'/><line x1='12' x2='12' y1='12' y2='21'/><path d='M20.88 18.09A5 5 0 0 0 18 9h-1.26A8 8 0 1 0 3 16.29'/></svg>
      </b:includable>
      
      <!--[ Lock icon ]-->
      <b:includable id='lock-icon'>
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(3.500000, 2.000000)'><path d='M12.9709,7.4033 L12.9709,5.2543 C12.9399,2.7353 10.8719,0.7193 8.3539,0.7503 C5.8869,0.7813 3.8919,2.7673 3.8499,5.2343 L3.8499,7.4033'/><line x1='8.4103' x2='8.4103' y1='12.1562' y2='14.3772'/><path d='M8.4103,6.8242 C2.6653,6.8242 0.7503,8.3922 0.7503,13.0952 C0.7503,17.7992 2.6653,19.3672 8.4103,19.3672 C14.1553,19.3672 16.0713,17.7992 16.0713,13.0952 C16.0713,8.3922 14.1553,6.8242 8.4103,6.8242 Z'/></g></svg>
      </b:includable>
      
      <!--[ Shield done icon ]-->
      <b:includable id='shield-done-icon'>
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(3.500000, 2.000000)'><path d='M8.4845,19.6057 C10.8195,19.6057 16.1565,17.2837 16.1565,10.8787 C16.1565,4.4747 16.4345,3.9737 15.8195,3.3577 C15.2035,2.7417 11.9935,0.7507 8.4845,0.7507 C4.9755,0.7507 1.7655,2.7417 1.1505,3.3577 C0.5345,3.9737 0.8125,4.4747 0.8125,10.8787 C0.8125,17.2837 6.1505,19.6057 8.4845,19.6057 Z'/><polyline points='5.8859 9.8748 7.7779 11.7698 11.6759 7.8698'/></g></svg>
      </b:includable>
      
      <!--[ Plus icon ]-->
      <b:includable id='plus-icon'>
        <svg viewBox='0 0 512 512'><path d='M417.4,224H288V94.6c0-16.9-14.3-30.6-32-30.6c-17.7,0-32,13.7-32,30.6V224H94.6C77.7,224,64,238.3,64,256 c0,17.7,13.7,32,30.6,32H224v129.4c0,16.9,14.3,30.6,32,30.6c17.7,0,32-13.7,32-30.6V288h129.4c16.9,0,30.6-14.3,30.6-32 C448,238.3,434.3,224,417.4,224z'/></svg>
      </b:includable>
      
      <!--[ Moon icon ]-->
      <b:includable id='moon-sun-icon'>
        <svg class='line' viewBox='0 0 24 24'>
          <g class='d1'><path d='M183.72453,170.371a10.4306,10.4306,0,0,1-.8987,3.793,11.19849,11.19849,0,0,1-5.73738,5.72881,10.43255,10.43255,0,0,1-3.77582.89138,1.99388,1.99388,0,0,0-1.52447,3.18176,10.82936,10.82936,0,1,0,15.118-15.11819A1.99364,1.99364,0,0,0,183.72453,170.371Z' transform='translate(-169.3959 -166.45548)'/></g>
          <g class='d2'><path class='f' d='M12 18.5C15.5899 18.5 18.5 15.5899 18.5 12C18.5 8.41015 15.5899 5.5 12 5.5C8.41015 5.5 5.5 8.41015 5.5 12C5.5 15.5899 8.41015 18.5 12 18.5Z'/><path d='M19.14 19.14L19.01 19.01M19.01 4.99L19.14 4.86L19.01 4.99ZM4.86 19.14L4.99 19.01L4.86 19.14ZM12 2.08V2V2.08ZM12 22V21.92V22ZM2.08 12H2H2.08ZM22 12H21.92H22ZM4.99 4.99L4.86 4.86L4.99 4.99Z' stroke-width='2'/></g></svg>
      </b:includable>
      
      <!--[ Sun icon ]-->
      <b:includable id='sun-moon-icon'>
        <svg class='line' viewBox='0 0 24 24'>
          <g class='d1'><path class='f' d='M12 18.5C15.5899 18.5 18.5 15.5899 18.5 12C18.5 8.41015 15.5899 5.5 12 5.5C8.41015 5.5 5.5 8.41015 5.5 12C5.5 15.5899 8.41015 18.5 12 18.5Z'/><path d='M19.14 19.14L19.01 19.01M19.01 4.99L19.14 4.86L19.01 4.99ZM4.86 19.14L4.99 19.01L4.86 19.14ZM12 2.08V2V2.08ZM12 22V21.92V22ZM2.08 12H2H2.08ZM22 12H21.92H22ZM4.99 4.99L4.86 4.86L4.99 4.99Z' stroke-width='2'/></g>
          <g class='d2'><path d='M183.72453,170.371a10.4306,10.4306,0,0,1-.8987,3.793,11.19849,11.19849,0,0,1-5.73738,5.72881,10.43255,10.43255,0,0,1-3.77582.89138,1.99388,1.99388,0,0,0-1.52447,3.18176,10.82936,10.82936,0,1,0,15.118-15.11819A1.99364,1.99364,0,0,0,183.72453,170.371Z' transform='translate(-169.3959 -166.45548)'/></g></svg>
      </b:includable>
      
      <!--[ Grid icon ]-->
      <b:includable id='grid-icon'>
        <svg class='line' viewBox='0 0 24 24'><path d='M9 22H15C20 22 22 20 22 15V9C22 4 20 2 15 2H9C4 2 2 4 2 9V15C2 20 4 22 9 22Z'/><path class='s3' d='M12 2V22'/><path d='M2 12H22'/></svg>
      </b:includable>
      
      <!--[ Chat icon ]-->
      <b:includable id='chat-icon'>
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(2.000000, 2.000000)'><path d='M17.0710351,17.0698449 C14.0159481,20.1263505 9.48959549,20.7867004 5.78630747,19.074012 C5.23960769,18.8538953 1.70113357,19.8338667 0.933341969,19.0669763 C0.165550368,18.2990808 1.14639409,14.7601278 0.926307229,14.213354 C-0.787154393,10.5105699 -0.125888852,5.98259958 2.93020311,2.9270991 C6.83146881,-0.9756997 13.1697694,-0.9756997 17.0710351,2.9270991 C20.9803405,6.8359285 20.9723008,13.1680512 17.0710351,17.0698449 Z'/></g></svg>
      </b:includable>
      
      <!--[ Chata icon ]-->
      <b:includable id='chata-icon'>
        <svg viewBox='0 0 24 24'><g transform='translate(2.000000, 2.000000)'><path d='M17.0710351,17.0698449 C14.0159481,20.1263505 9.48959549,20.7867004 5.78630747,19.074012 C5.23960769,18.8538953 1.70113357,19.8338667 0.933341969,19.0669763 C0.165550368,18.2990808 1.14639409,14.7601278 0.926307229,14.213354 C-0.787154393,10.5105699 -0.125888852,5.98259958 2.93020311,2.9270991 C6.83146881,-0.9756997 13.1697694,-0.9756997 17.0710351,2.9270991 C20.9803405,6.8359285 20.9723008,13.1680512 17.0710351,17.0698449 Z'/></g></svg>
      </b:includable>
      
      <!--[ Messages icon ]-->
      <b:includable id='messages-icon'>
        <svg class='line' viewBox='0 0 24 24'><path d='M22 10V13C22 17 20 19 16 19H15.5C15.19 19 14.89 19.15 14.7 19.4L13.2 21.4C12.54 22.28 11.46 22.28 10.8 21.4L9.3 19.4C9.14 19.18 8.77 19 8.5 19H8C4 19 2 18 2 13V8C2 4 4 2 8 2H14'/><path d='M19.5 7C20.8807 7 22 5.88071 22 4.5C22 3.11929 20.8807 2 19.5 2C18.1193 2 17 3.11929 17 4.5C17 5.88071 18.1193 7 19.5 7Z'/></svg>
      </b:includable>
      
      <!--[ Hamburger menu icon ]-->
      <b:includable id='ham-icon'>
        <svg class='line' viewBox='0 0 24 24'><line x1='3' x2='21' y1='12' y2='12'/><line x1='3' x2='21' y1='5' y2='5'/><line x1='3' x2='21' y1='19' y2='19'/></svg>
      </b:includable>
      
      <!--[ Menu icon ]-->
      <b:includable id='menu-icon'>
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(3.000000, 3.000000)'><path class='fill' d='M18.00036,3.6738 C18.00036,5.7024 16.35516,7.3476 14.32656,7.3476 C12.29796,7.3476 10.65366,5.7024 10.65366,3.6738 C10.65366,1.6452 12.29796,-6.39488462e-15 14.32656,-6.39488462e-15 C16.35516,-6.39488462e-15 18.00036,1.6452 18.00036,3.6738 Z'/><path class='fill' d='M7.3467,3.6738 C7.3467,5.7024 5.7024,7.3476 3.6729,7.3476 C1.6452,7.3476 4.79616347e-15,5.7024 4.79616347e-15,3.6738 C4.79616347e-15,1.6452 1.6452,-6.39488462e-15 3.6729,-6.39488462e-15 C5.7024,-6.39488462e-15 7.3467,1.6452 7.3467,3.6738 Z'/><path class='fill' d='M18.00036,14.26194 C18.00036,16.29054 16.35516,17.93484 14.32656,17.93484 C12.29796,17.93484 10.65366,16.29054 10.65366,14.26194 C10.65366,12.23334 12.29796,10.58814 14.32656,10.58814 C16.35516,10.58814 18.00036,12.23334 18.00036,14.26194 Z'/><path class='fill' d='M7.3467,14.26194 C7.3467,16.29054 5.7024,17.93484 3.6729,17.93484 C1.6452,17.93484 4.79616347e-15,16.29054 4.79616347e-15,14.26194 C4.79616347e-15,12.23334 1.6452,10.58814 3.6729,10.58814 C5.7024,10.58814 7.3467,12.23334 7.3467,14.26194 Z'/></g></svg>
      </b:includable>
      
      <!--[ Calendar icon ]-->
      <b:includable id='calendar-icon'>
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(2.749800, 2.050100)'><path d='M-1.0658141e-14,10.7255 C-1.0658141e-14,3.7695 2.319,1.4515 9.274,1.4515 C16.23,1.4515 18.549,3.7695 18.549,10.7255 C18.549,17.6815 16.23,19.9995 9.274,19.9995 C2.319,19.9995 -1.0658141e-14,17.6815 -1.0658141e-14,10.7255 Z'/><line x1='0.2754' x2='18.2834' y1='7.2739' y2='7.2739'/><line x1='13.2832' x2='13.2832' y1='2.84217094e-14' y2='3.262'/><line x1='5.2749' x2='5.2749' y1='2.84217094e-14' y2='3.262'/></g></svg>
      </b:includable>
      
      <!--[ Time square icon ]-->
      <b:includable id='time-square-icon'>
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(2.000000, 2.000000)'><path d='M0.7501,10.0001 C0.7501,16.9371 3.0631,19.2501 10.0001,19.2501 C16.9371,19.2501 19.2501,16.9371 19.2501,10.0001 C19.2501,3.0631 16.9371,0.7501 10.0001,0.7501 C3.0631,0.7501 0.7501,3.0631 0.7501,10.0001 Z'/><polyline points='13.3902 12.0181 9.9992 9.9951 9.9992 5.6341'/></g></svg>
      </b:includable>
      
      <!--[ Bookmark icon ]-->
      <b:includable id='bookmark-icon'>
        <svg class='line' viewBox='0 0 24 24'><g transform='translate(4.500000, 2.500000)'><path d='M7.47024319,0 C1.08324319,0 0.00424318741,0.932 0.00424318741,8.429 C0.00424318741,16.822 -0.152756813,19 1.44324319,19 C3.03824319,19 5.64324319,15.316 7.47024319,15.316 C9.29724319,15.316 11.9022432,19 13.4972432,19 C15.0932432,19 14.9362432,16.822 14.9362432,8.429 C14.9362432,0.932 13.8572432,0 7.47024319,0 Z'/></g></svg>
      </b:includable>
      
      <!--[ Link icon ]-->
      <b:includable id='link-icon'>
        <svg class='line' viewBox='0 0 24 24'><path d='M13 11L21.2 2.80005'/><path d='M22 6.8V2H17.2'/><path d='M11 2H9C4 2 2 4 2 9V15C2 20 4 22 9 22H15C20 22 22 20 22 15V13'/></svg>
      </b:includable>
      
      <!--[ Tag icon ]-->
      <b:includable id='tag-icon'>
        <svg class='line' viewBox='0 0 24 24'><path d='M4.16989 15.3L8.69989 19.83C10.5599 21.69 13.5799 21.69 15.4499 19.83L19.8399 15.44C21.6999 13.58 21.6999 10.56 19.8399 8.69005L15.2999 4.17005C14.3499 3.22005 13.0399 2.71005 11.6999 2.78005L6.69989 3.02005C4.69989 3.11005 3.10989 4.70005 3.00989 6.69005L2.76989 11.69C2.70989 13.04 3.21989 14.35 4.16989 15.3Z'/><path d='M9.5 12C10.8807 12 12 10.8807 12 9.5C12 8.11929 10.8807 7 9.5 7C8.11929 7 7 8.11929 7 9.5C7 10.8807 8.11929 12 9.5 12Z'/></svg>
      </b:includable>
      
      <!--[ Link icon alt ]-->
      <b:includable id='link-alt-icon'>
        <svg class='line' viewBox='0 0 24 24'><path d='M13.0601 10.9399C15.3101 13.1899 15.3101 16.8299 13.0601 19.0699C10.8101 21.3099 7.17009 21.3199 4.93009 19.0699C2.69009 16.8199 2.68009 13.1799 4.93009 10.9399'/><path d='M10.59 13.4099C8.24996 11.0699 8.24996 7.26988 10.59 4.91988C12.93 2.56988 16.73 2.57988 19.08 4.91988C21.43 7.25988 21.42 11.0599 19.08 13.4099'/></svg>
      </b:includable>
      
      <!--[ Location icon ]-->
      <b:includable id='location-icon'>
        <svg class='line' viewBox='0 0 24 24'><path d='M12 13.4299C13.7231 13.4299 15.12 12.0331 15.12 10.3099C15.12 8.58681 13.7231 7.18994 12 7.18994C10.2769 7.18994 8.88 8.58681 8.88 10.3099C8.88 12.0331 10.2769 13.4299 12 13.4299Z'/><path d='M3.62001 8.49C5.59001 -0.169998 18.42 -0.159997 20.38 8.5C21.53 13.58 18.37 17.88 15.6 20.54C13.59 22.48 10.41 22.48 8.39001 20.54C5.63001 17.88 2.47001 13.57 3.62001 8.49Z'/></svg>
      </b:includable>
      
      <!--[ Gear icon ]-->
      <b:includable id='gear-icon'>
        <svg class='line' viewBox='0 0 24 24' xmlns='http://www.w3.org/2000/svg'><g><path d='M188.9,174.86929l-1.42615-.24236a2.8036,2.8036,0,0,1-2.29428-2.29428l-.24236-1.42621a3,3,0,0,0-2.9576-2.4974h-1.16436a3,3,0,0,0-2.9576,2.4974l-.24236,1.42621a2.8036,2.8036,0,0,1-2.29428,2.29428l-1.42621.24236a3,3,0,0,0-2.4974,2.9576v1.16436a3,3,0,0,0,2.4974,2.9576l1.42621.24236a2.8036,2.8036,0,0,1,2.29428,2.29428l.24236,1.42615a3,3,0,0,0,2.9576,2.4974h1.16437a3,3,0,0,0,2.95759-2.4974l.24236-1.42616a2.8036,2.8036,0,0,1,2.29427-2.29427l1.42616-.24236a3,3,0,0,0,2.4974-2.95759v-1.16437A3,3,0,0,0,188.9,174.86929Z' transform='translate(-169.39739 -166.40904)'/><circle cx='12' cy='12' r='1.75'/></g></svg>
      </b:includable>
      
      <!--[ Phone icon ]-->
      <b:includable id='phone-icon'>
        <svg class='line' viewBox='0 0 24 24' xmlns='http://www.w3.org/2000/svg'><g><line x1='13.69505' x2='10.30495' y1='18' y2='18'/><rect height='20' rx='5' width='16' x='4' y='2'/></g></svg>
      </b:includable>
      
      <!--[ Game icon ]-->
      <b:includable id='game-icon'>
        <svg class='line' viewBox='0 0 24 24' xmlns='http://www.w3.org/2000/svg'><g transform='translate(2.000000, 1.977425)'><line x1='7.25474269' x2='7.25474269' y1='10.085022' y2='13.6602214'/><line x1='9.07928848' x2='5.431535' y1='11.8722397' y2='11.8722397'/><line x1='13.477308' x2='13.3751594' y1='10.1936617' y2='10.1936617'/><line x1='15.208106' x2='15.1059574' y1='13.6058057' y2='13.6058057'/><path d='M6.5140228,0.238664844 L6.5140228,0.238664844 C6.52070542,0.952750059 7.10591161,1.52554569 7.81999683,1.51886307 L8.82811713,1.51886307 C9.93074871,1.51027114 10.8329018,2.39428572 10.8481764,3.4969173 L10.8481764,4.50408295'/><path d='M19.8121415,11.9178722 C19.8121415,6.35793599 17.4254931,4.50398748 10.2645931,4.50398748 C3.10273844,4.50398748 0.716089999,6.35793599 0.716089999,11.9178722 C0.716089999,17.4787631 3.10273844,19.3317569 10.2645931,19.3317569 C17.4254931,19.3317569 19.8121415,17.4787631 19.8121415,11.9178722 Z'/></g></svg>
      </b:includable>
      
      <!--[ Clock icon ]-->
      <b:includable id='jam-icon'>
        <svg class='line' viewBox='0 0 24 24' xmlns='http://www.w3.org/2000/svg'><g transform='translate(2.000000, 2.000000)'><path d='M19.2498,10.0001 C19.2498,15.1081 15.1088,19.2501 9.9998,19.2501 C4.8918,19.2501 0.7498,15.1081 0.7498,10.0001 C0.7498,4.8911 4.8918,0.7501 9.9998,0.7501 C15.1088,0.7501 19.2498,4.8911 19.2498,10.0001 Z'/><polyline points='14.1907 10.7672 9.6607 10.6932 9.6607 5.8462'/></g></svg>
      </b:includable>
      
      <!--[ Update icon ]-->
      <b:includable id='update-icon'>
        <svg style='width:13.5px;height:13.5px' viewBox='0 0 122.88 119.78'><path d='M63,7.81A3.91,3.91,0,1,1,63,0,59.91,59.91,0,1,1,11.17,29.87L6.89,31.51A5.08,5.08,0,1,1,3.28,22L16.5,17a5.17,5.17,0,0,1,1.57-.32,5.05,5.05,0,0,1,5.65,3.53L27.87,33.7a5.07,5.07,0,1,1-9.7,2.94l-.66-2.15a52.08,52.08,0,0,0,82.3,62.22A52.08,52.08,0,0,0,63,7.81Zm-14.1,57c-3.3-3.55,1.76-8.85,5.43-5.5,1.3,1.18,3.18,2.91,4.48,4.08l12.69-15c3.51-3.62,9,1.7,5.58,5.35L61.82,71.41a3.9,3.9,0,0,1-5.4.23c-2.14-2-5.28-5-7.53-6.86ZM40.32,33.61a3.37,3.37,0,0,1,5.85-3.36l1.67,2.9A3.37,3.37,0,0,1,42,36.51l-1.68-2.9Zm-10,13.53a3.38,3.38,0,1,1,3.39-5.85L36.64,43a3.38,3.38,0,0,1-3.39,5.85l-2.9-1.68Zm4.9,34.4a3.37,3.37,0,0,1-3.36-5.84L34.8,74a3.37,3.37,0,0,1,3.36,5.85l-2.91,1.67ZM27.43,63.26a3.37,3.37,0,0,1,0-6.74h3.36a3.37,3.37,0,0,1,0,6.74Zm37.78,31a3.38,3.38,0,0,1-6.75,0V90.94a3.38,3.38,0,0,1,6.75,0v3.35Zm-6.75-68.8a3.38,3.38,0,1,1,6.75,0v3.35a3.38,3.38,0,0,1-6.75,0V25.49ZM47.56,91.37A3.38,3.38,0,1,1,41.71,88l1.68-2.9a3.37,3.37,0,1,1,5.84,3.38l-1.67,2.9ZM83.49,88a3.37,3.37,0,1,1-5.85,3.36L76,88.46a3.37,3.37,0,0,1,5.85-3.36L83.49,88Zm9.83-12.3a3.37,3.37,0,0,1-3.38,5.84L87,79.87A3.38,3.38,0,0,1,90.42,74l2.9,1.68ZM91.48,41.29a3.37,3.37,0,0,1,3.36,5.85l-2.9,1.68A3.37,3.37,0,0,1,88.58,43l2.9-1.68ZM79.7,31.51a3.38,3.38,0,0,1,5.85,3.39l-1.68,2.9A3.38,3.38,0,1,1,78,34.41l1.67-2.9Zm18.85,25a3.37,3.37,0,1,1,0,6.74H95a3.37,3.37,0,0,1,0-6.74Z'/></svg>
      </b:includable>
      
      <!--[ Update2 icon ]-->
      <b:includable id='update2-icon'>
        <svg style='width:13.5px;height:13.5px' viewBox='0 0 512 506.49'><path d='M294.24 17.11C294.24 7.69 303.52 0 315.1 0c11.57 0 20.87 7.65 20.87 17.11v74.85c0 9.42-9.3 17.11-20.87 17.11-11.58 0-20.86-7.65-20.86-17.11V17.11zm58.81 301.55h17.92c3.27 0 5.96 2.69 5.96 5.96v56.84h48.21c3.3 0 5.99 2.7 5.99 5.98v17.92c0 3.31-2.69 5.98-5.99 5.98h-78.09v-86.72c0-3.27 2.7-5.96 6-5.96zm24.77-80.55c36.98 0 70.56 15.04 94.83 39.35C496.96 301.7 512 335.25 512 372.31c0 37.02-15.02 70.61-39.3 94.88l-.68.64c-24.23 23.88-57.5 38.66-94.2 38.66-37.06 0-70.61-15.04-94.88-39.31l-.64-.69c-23.9-24.24-38.68-57.53-38.68-94.18 0-37.06 15.04-70.61 39.32-94.88 24.27-24.28 57.85-39.32 94.88-39.32zm78.74 55.41c-20.09-20.11-47.96-32.58-78.74-32.58-30.75 0-58.61 12.47-78.75 32.62-20.15 20.14-32.62 48-32.62 78.75 0 30.5 12.25 58.14 32.02 78.19l.6.55c20.14 20.14 48 32.62 78.75 32.62 30.48 0 58.12-12.26 78.21-32.03l.54-.58c20.15-20.15 32.61-48 32.61-78.75s-12.48-58.61-32.62-78.79zM56.8 242.28c-1.17 0-2.23-5.2-2.23-11.56 0-6.39.92-11.54 2.23-11.54h56.94c1.18 0 2.24 5.2 2.24 11.54 0 6.38-.92 11.56-2.24 11.56H56.8zm90.77 0c-1.17 0-2.23-5.2-2.23-11.56 0-6.39.92-11.54 2.23-11.54h56.94c1.18 0 2.24 5.2 2.24 11.54 0 6.38-.92 11.56-2.24 11.56h-56.94zm90.77 0c-1.16 0-2.22-5.2-2.22-11.56 0-6.39.92-11.54 2.22-11.54h56.94c1.19 0 2.25 5.15 2.25 11.49-5.7 3.55-11.2 7.44-16.43 11.61h-42.76zm-181.4 66.24c-1.18 0-2.24-5.2-2.24-11.57 0-6.38.93-11.58 2.24-11.58h56.94c1.18 0 2.22 5.2 2.22 11.58 0 6.37-.91 11.57-2.22 11.57H56.94zm90.77 0c-1.18 0-2.24-5.2-2.24-11.57 0-6.38.93-11.58 2.24-11.58h56.94c1.18 0 2.23 5.2 2.23 11.58 0 6.37-.92 11.57-2.23 11.57h-56.94zM57.06 374.8c-1.18 0-2.24-5.2-2.24-11.58 0-6.37.94-11.57 2.24-11.57H114c1.19 0 2.24 5.2 2.24 11.57 0 6.38-.93 11.58-2.24 11.58H57.06zm90.78 0c-1.19 0-2.25-5.2-2.25-11.58 0-6.37.94-11.57 2.25-11.57h56.94c1.18 0 2.24 5.2 2.24 11.57 0 6.38-.94 11.58-2.24 11.58h-56.94zM106.83 17.11C106.83 7.69 116.1 0 127.69 0c11.57 0 20.86 7.65 20.86 17.11v74.85c0 9.42-9.34 17.11-20.86 17.11-11.59 0-20.86-7.65-20.86-17.11V17.11zM22.97 163.64h397.39V77.46c0-2.94-1.19-5.53-3.09-7.43-1.9-1.9-4.59-3.08-7.42-3.08h-38.1c-6.39 0-11.59-5.2-11.59-11.57 0-6.38 5.2-11.58 11.59-11.58h38.1c9.32 0 17.7 3.77 23.82 9.89 6.12 6.13 9.88 14.49 9.88 23.82v136.81c-7.61-2.62-15.41-4.73-23.44-6.29v-21.38h.25H22.97v223.17c0 2.94 1.18 5.52 3.08 7.42 1.91 1.9 4.61 3.09 7.44 3.09h188.85c2.16 8.01 4.86 15.83 8.11 23.35H33.71c-9.3 0-17.7-3.75-23.84-9.89C3.75 427.72 0 419.36 0 410.02V77.55c0-9.29 3.75-17.7 9.87-23.82 6.14-6.13 14.5-9.88 23.84-9.88h40.67c6.38 0 11.57 5.2 11.57 11.56C85.95 61.8 80.76 67 74.38 67H33.71c-2.96 0-5.54 1.18-7.44 3.08-1.9 1.9-3.09 4.59-3.09 7.43v86.16h-.21v-.03zm158.95-96.69c-6.39 0-11.57-5.2-11.57-11.57 0-6.38 5.18-11.58 11.57-11.58h77.55c6.39 0 11.57 5.2 11.57 11.58 0 6.37-5.18 11.57-11.57 11.57h-77.55z'/></svg>
      </b:includable>
      
    </b:defaultmarkup>
  </b:defaultmarkups>
 
  <b:if cond='!data:view.isError and data:view.url != data:view.url params { amp: &quot;1&quot; }'>
    <script>/*<![CDATA[*/ /*@shinsenter/defer.js*/ !function(c,i,t){var f,o=/^data-(.+)/,u='IntersectionObserver',r=/p/.test(i.readyState),s=[],a=s.slice,d='lazied',n='load',e='pageshow',l='forEach',m='hasAttribute',h='shift';function p(e){i.head.appendChild(e)}function v(e,n){a.call(e.attributes)[l](n)}function y(e,n,t,o){return o=(o=n?i.getElementById(n):o)||i.createElement(e),n&&(o.id=n),t&&(o.onload=t),o}function b(e,n){return a.call((n||i).querySelectorAll(e))}function g(t,e){b('source',t)[l](g),v(t,function(e,n){(n=o.exec(e.name))&&(t[n[1]]=e.value)}),e&&(t.className+=' '+e),n in t&&t[n]()}function I(e){f(function(o){o=b(e||'[type=deferjs]'),function e(n,t){(n=o[h]())&&(n.parentNode.removeChild(n),(t=y(n.nodeName)).text=n.text,v(n,function(e){'type'!=e.name&&(t[e.name]=e.value)}),t.src&&!t[m]('async')?(t.onload=t.onerror=e,p(t)):(p(t),e()))}()})}(f=function(e,n){r?t(e,n):s.push(e,n)}).all=I,f.js=function(n,t,e,o){f(function(e){(e=y('SCRIPT',t,o)).src=n,p(e)},e)},f.css=function(n,t,e,o){f(function(e){(e=y('LINK',t,o)).rel='stylesheet',e.href=n,p(e)},e)},f.dom=function(e,n,t,o,i){function r(e){o&&!1===o(e)||g(e,t)}f(function(t){t=u in c&&new c[u](function(e){e[l](function(e,n){e.isIntersecting&&(n=e.target)&&(t.unobserve(n),r(n))})},i),b(e||'[data-src]')[l](function(e){e[m](d)||(e.setAttribute(d,''),t?t.observe(e):r(e))})},n)},f.reveal=g,c.Defer=f,c.addEventListener('on'+e in c?e:n,function(){for(I();s[0];t(s[h](),s[h]()))r=1})}(this,document,setTimeout),function(e,n){e.defer=n=e.Defer,e.deferscript=n.js,e.deferstyle=n.css,e.deferimg=e.deferiframe=n.dom}(this); /*]]>*/</script>
    <script id='polyfill-js'>&#39;IntersectionObserver&#39;in window||document.write(&#39;&lt;script src=&quot;https://polyfill.io/v3/polyfill.min.js?features=IntersectionObserver&quot;&gt;&lt;\/script&gt;&#39;);</script>
    <b:if cond='data:view.isPost'>
      <script>/*<![CDATA[*/ /* Table of Content, Credit: blustemy.io/creating-a-table-of-contents-in-javascript */
class TableOfContents { constructor({ from, to }) { this.fromElement = from; this.toElement = to; this.headingElements = this.fromElement.querySelectorAll("h1, h2, h3, h4, h5, h6"); this.tocElement = document.createElement("div"); }; getMostImportantHeadingLevel() { let mostImportantHeadingLevel = 6; for (let i = 0; i < this.headingElements.length; i++) { let headingLevel = TableOfContents.getHeadingLevel(this.headingElements[i]); mostImportantHeadingLevel = (headingLevel < mostImportantHeadingLevel) ? headingLevel : mostImportantHeadingLevel; } return mostImportantHeadingLevel; }; static generateId(headingElement) { return headingElement.textContent.replace(/\s+/g, "_"); }; static getHeadingLevel(headingElement) { switch (headingElement.tagName.toLowerCase()) { case "h1": return 1; case "h2": return 2; case "h3": return 3; case "h4": return 4; case "h5": return 5; case "h6": return 6; default: return 1; } }; generateToc() { let currentLevel = this.getMostImportantHeadingLevel() - 1, currentElement = this.tocElement; for (let i = 0; i < this.headingElements.length; i++) { let headingElement = this.headingElements[i], headingLevel = TableOfContents.getHeadingLevel(headingElement), headingLevelDifference = headingLevel - currentLevel, linkElement = document.createElement("a"); if (!headingElement.id) { headingElement.id = TableOfContents.generateId(headingElement); } linkElement.href = `#${headingElement.id}`; linkElement.textContent = headingElement.textContent; if (headingLevelDifference > 0) { for (let j = 0; j < headingLevelDifference; j++) { let listElement = document.createElement("ol"), listItemElement = document.createElement("li"); listElement.appendChild(listItemElement); currentElement.appendChild(listElement); currentElement = listItemElement; } currentElement.appendChild(linkElement); } else { for (let j = 0; j < -headingLevelDifference; j++) { currentElement = currentElement.parentNode.parentNode; } let listItemElement = document.createElement("li"); listItemElement.appendChild(linkElement); currentElement.parentNode.appendChild(listItemElement); currentElement = listItemElement; } currentLevel = headingLevel; } this.toElement.appendChild(this.tocElement.firstChild); } } /*]]>*/</script>
    </b:if>
      
    <b:if cond='data:blog.analyticsAccountNumber'>
      <!--[ Google Analytics new global tag ]-->
      <script>function downloadJSAtOnload(){var d=document.createElement(&#39;script&#39;);d.src=&#39;https://www.googletagmanager.com/gtag/js?id=<data:blog.analyticsAccountNumber/>&#39;,document.body.appendChild(d)}window.addEventListener?window.addEventListener(&#39;load&#39;,downloadJSAtOnload,!1):window.attachEvent?window.attachEvent(&#39;onload&#39;,downloadJSAtOnload):window.onload=downloadJSAtOnload; window.dataLayer = window.dataLayer || []; function gtag(){dataLayer.push(arguments);} gtag(&#39;js&#39;, new Date()); gtag(&#39;config&#39;, &#39;<data:blog.analyticsAccountNumber/>&#39;); </script>
    </b:if>
  </b:if>
  
    <script type='application/ld+json'>
  {
    &quot;@context&quot;: &quot;https://schema.org&quot;,
    &quot;@type&quot;: &quot;WebSite&quot;,
    &quot;url&quot;: &quot;<data:blog.homepageUrl.canonical/>&quot;,
    &quot;name&quot;: &quot;<data:blog.title/>&quot;,
    &quot;alternateName&quot;: &quot;<data:blog.title/>&quot;,
    &quot;potentialAction&quot;: {
      &quot;@type&quot;: &quot;SearchAction&quot;,
      &quot;target&quot;: &quot;<data:blog.homepageUrl.canonical/>search?q={search_term_string}&quot;,
      &quot;query-input&quot;: &quot;required name=search_term_string&quot;
    }
  }
  </script>
  
  <!--[ Defer Adsense script use shinsenter/defer.js ]-->
  <script crossorigin='anonymous' src='https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-3400053731432707' type='deferjs'/>

  <b:if cond='data:view.isSingleItem'><script>/*<![CDATA[*/
eval(function(x,r,t,c,n,e){if(n=function(x){return(x<62?"":n(parseInt(x/62)))+((x%=62)>35?String.fromCharCode(x+29):x.toString(36))},!"".replace(/^/,String)){for(;t--;)e[n(t)]=c[t]||n(t);c=[function(x){return e[x]}],n=function(){return"\\w+"},t=1}for(;t--;)c[t]&&(x=x.replace(new RegExp("\\b"+n(t)+"\\b","g"),c[t]));return x}("i j(d,e){2 f=k();o j=i(a,b){a=a-p;2 c=f[a];o c},j(d,e)}2 0=j;(i(a,b){2 c=j,l=a();L(!![]){M{2 d=4(c(N))/O*(4(c(P))/Q)+-4(c(R))/S+4(c(T))/U+4(c(V))/W*(-4(c(X))/Y)+4(c(Z))/10*(-4(c(11))/12)+4(c(13))/14*(4(c(15))/16)+4(c(17))/18*(4(c(19))/1a);8(d===b)1b;1c l['A'](l['B']())}1d(1e){l['A'](l['B']())}}}(k,1f));2 3=5['t'][0(q)]();8(3[0(9)](0(C),0(C))>6){2 7=3[0(u)](6,3['v']('%h'));5[0(w)][0(x)]({},r[0(s)],7)}2 3=5[0(n)][0(q)]();8(3[0(9)](0(D),0(D))>6){2 7=3[0(u)](6,3[0(9)]('%h%h'));5[0(w)]['E']({},r[0(s)],7)}2 3=5[0(n)][0(q)]();8(3['v'](0(p),0(p))>6){2 7=3[0(u)](6,3[0(9)](0(p)));5['F'][0(x)]({},r[0(s)],7)}i k(){2 a=['E','1g','1h','1i','%h','1j','1k','1l','1m','%h%h','G','1n','1o','1p','&m=1','t','?m=1','1q','1r','1s','F','1t','v','1u','1v','1w','H'];k=i(){o a};o k()}2 3=5[0(n)][0(q)]();8(3[0(9)](0(y),0(y))>6){2 7=3['H'](6,3[0(9)](0(y)));5[0(w)][0(x)]({},r[0(s)],7)};2 z=5[0(n)]['z']['G'](/\\:/g,'');8(z==0(I)){2 J=5[0(n)][0(1x)][0(K)](0(I),0(1y));5['t'][0(K)](J)}",0,97,"_0x10f1fd||var|uri|parseInt|window|0x0|clean_uri|if|0x131||||||||3D|function|_0x5129|_0x1317|_0x14e245||0x12a|return|0x129|0x137|document|0x139|location|0x135|indexOf|0x12f|0x136|0x12b|protocol|push|shift|0x13a|0x13f|replaceState|history|replace|substring|0x13c|url|0x140|while|try|0x13b|0x1|0x142|0x2|0x132|0x3|0x138|0x4|0x133|0x5|0x12c|0x6|0x143|0x7|0x130|0x8|0x13d|0x9|0x12d|0xa|0x134|0xb|0x12e|0xc|break|else|catch|_0x1c0914|0xa01c0|toString|3336020bsyxLl|title|6hhHrnk|http|586854WjxWYP|https|href|36196IbAvcs|4861612ADZSAw|30uZFVJQ|110hhmErV|21384KBdrKT|8vfnZyT|3782346LuHRGl|761255tYTkRp|10571kcdLbT|0x141|0x13e".split("|"),0,{}));
/*]]>*/</script></b:if>

  <!--[ </head> close ]-->
  &lt;!--<head/><b:if cond='!data:blog.adsenseClientId'>--&gt;&lt;/head&gt;</b:if>

  <!--[ <body> open ]-->
  <body>
    <b:class cond='data:view.isMultipleItems' name='grD'/>
    <b:attr name='id' value='mainCont'/>
    
    <!--[ Show only one grid column in Mobile ]-->
    <b:class cond='data:view.isMultipleItems' name='oGrd'/>
    
    <b:class name='bD'/>
    <b:class cond='data:view.url == data:view.url params { amp: &quot;1&quot; }' name='nAmp'/>
    <b:class cond='data:blog.languageDirection == &quot;rtl&quot;' name='Rtl'/>
    <b:class cond='data:view.isMultipleItems' name='onId'/>
    <b:class cond='data:view.isMultipleItems != data:view.isHomepage' name='onMl'/>
    <b:class cond='data:view.url == data:blog.homepageUrl.canonical path &quot;search&quot;' name='onBl'/>
    <b:class cond='data:view.isHomepage' name='onHm'/>
    <b:class cond='data:view.isSingleItem' name='onIt'/>
    <b:class cond='data:view.isPage' name='onPg'/>
    <b:class cond='data:view.isPost' name='onPs'/>
    <b:class cond='data:view.isError' name='on404'/>
    
    <b:if cond='data:view.url != data:view.url params { amp: &quot;1&quot; }'>
      <script>/*<![CDATA[*/ (localStorage.getItem('mode')) === 'darkmode' ? document.querySelector('#mainCont').classList.add('drK') : document.querySelector('#mainCont').classList.remove('drK') /*]]>*/</script>
    </b:if>
    
    <b:if cond='!data:view.isError'>      
      <!--[ Active function ]-->
      <input class='navi hidden' id='offNav' type='checkbox'/>
    </b:if>
    
    <b:tag class='mainWrp' cond='!data:view.isError' name='div'>
      <b:if cond='!data:view.isError'>
        
        <!--[ Notification section ]-->
        <b:section cond='!data:view.isPreview' id='notif-widget' maxwidgets='1' showaddelement='false'>
          <b:widget id='HTML0' locked='true' title='Notification' type='HTML' version='2' visible='false'>
            <b:widget-settings>
              <b:widget-setting name='content'>&lt;!--[ Your content here, Lorem ipsum dolor sit amet, consectetur adipiscing elit. ]--&gt;

&lt;!--[ Alternatif content with button link ]--&gt;
&lt;div class=&#39;ntfA&#39;&gt;
  &lt;span&gt;

&lt;div style=&quot;text-align: center;&quot;&gt;Tahap Pengembangan. &lt;br /&gt;&lt;a href=&#39;https://s.id/imtrjy17&#39;&gt;Test link&lt;/a&gt;

  &lt;/div&gt;&lt;/span&gt; 
  &lt;!-- &lt;a href=&#39;https://www.google.com/?hl=id&#39;&gt;Get now!&lt;/a&gt; --&gt;
&lt;/div&gt;</b:widget-setting>
            </b:widget-settings>
            <b:includable id='main'>
              <input class='ntfI hidden' id='forNft' type='checkbox'/>
              <div class='ntfC'>
                <div class='ntfT'><data:content/></div>
                <label aria-label='Close Menu' class='c' for='forNft'/>
              </div>
            </b:includable>
          </b:widget>
        </b:section>
        
        <!--[ Header section ]-->
        <header class='header' id='header'>
          
          <!--[ Header content ]-->
          <b:tag class='headCn' name='div'>
            <b:tag class='headIn secIn' name='div'>
              <b:tag class='headD headL' name='div'>
                <div class='headIc'>
                  <label class='tNav tIc bIc' for='offNav'><b:include name='ham-icon'/></label>
                </div>
              
                <!--[ Header widget ]-->
                <b:section class='headN' id='header-title' maxwidgets='1' showaddelement='false'>
                  <b:widget id='Header1' locked='true' title='Trjy17 (Header)' type='Header' version='2' visible='true'>
                    <b:widget-settings>
                      <b:widget-setting name='displayUrl'/>
                      <b:widget-setting name='displayHeight'>0</b:widget-setting>
                      <b:widget-setting name='sectionWidth'>300</b:widget-setting>
                      <b:widget-setting name='useImage'>false</b:widget-setting>
                      <b:widget-setting name='shrinkToFit'>false</b:widget-setting>
                      <b:widget-setting name='imagePlacement'>BEHIND</b:widget-setting>
                      <b:widget-setting name='displayWidth'>0</b:widget-setting>
                    </b:widget-settings>
                    <b:includable id='main' var='this'>
                      <b:include cond='data:imagePlacement in {&quot;REPLACE&quot;, &quot;BEFORE_DESCRIPTION&quot;}' name='image'/>
                      <b:include cond='data:imagePlacement not in {&quot;REPLACE&quot;, &quot;BEFORE_DESCRIPTION&quot;}' name='title'/>
                      <b:include cond='data:imagePlacement != &quot;REPLACE&quot;' name='description'/>
                      <b:include cond='data:imagePlacement == &quot;BEHIND&quot;' name='behindImageStyle'/>
                    </b:includable>
                    <b:includable id='behindImageStyle'>
                      <b:if cond='data:sourceUrl'>
                        <b:include cond='data:this.image' data='{image: data:this.image, selector: &quot;.Header&quot;}' name='responsiveImageStyle'/>
                      </b:if>
                    </b:includable>
                    <b:includable id='description'>
                      <b:if cond='data:this.description'>
                        <div class='headDsc hidden'><data:this.description/></div>
                      </b:if>
                    </b:includable>
                    <b:includable id='image'>
                      <!-- Header Image -->
                      <a expr:href='data:blog.homepageUrl.canonical'><img expr:alt='data:title' expr:height='data:height' expr:src='resizeImage(data:sourceUrl, 200)' expr:width='data:width'/></a>
                      <b:include cond='data:this.imagePlacement == &quot;REPLACE&quot;' name='title'/>
                    </b:includable>
                    <b:includable id='title'>
                      <!-- Header Title -->
                      <div class='headInnr'>
                        <b:class cond='data:this.imagePlacement == &quot;REPLACE&quot;' name='hidden'/>
                        <b:tag class='headH' expr:name='!data:view.isSingleItem ? &quot;h1&quot; : &quot;h2&quot;'>
                          <b:class cond='data:this.description' name='hasSub'/>
                          <b:tag class='headTtl' expr:name='!data:view.isHomepage ? &quot;a&quot; : &quot;span&quot;'>
                            <b:attr cond='!data:view.isHomepage' expr:value='data:blog.homepageUrl.canonical' name='href'/>
                            <data:title/>
                          </b:tag>
                          
                          <!--[ Header Description ]-->
                          <b:tag class='headSub' cond='data:this.description' expr:data-text='data:this.description' name='span'/>
                        </b:tag>
                      </div>
                    </b:includable>
                  </b:widget>
                </b:section>
              </b:tag>
          
              <!--[ Header menu ]-->
              <div class='headD headM'>
                <div class='mnBr'>
                  <div class='mnBrs'>
                    <b:if cond='!data:view.isLayoutMode'>
                      <div class='mnH'>
                        <label aria-label='Close' class='c' data-text='Close' for='offNav'/>
                      </div>
                    </b:if>
                
                    <!--[ Mobile additional menu(only shown in mobile view) ]-->
                    <b:section class='mnMob' id='header-Menu-mobile' maxwidgets='2' showaddelement='false'>
                      <b:widget id='PageList002' locked='true' title='Mobile Additional Menu' type='PageList' version='2' visible='true'>
                        <b:widget-settings>
                          <b:widget-setting name='pageListJson'><![CDATA[{"4293064794663784511":{"href":"https://www.trjy17.com/p/sitemap.html","position":0,"title":"Sitemap"},"7026321634800076720":{"href":"https://www.trjy17.com/p/disclaimer.html","position":1,"title":"Disclaimer"},"9191158149615481226":{"href":"https://www.trjy17.com/p/kebijakan-privasi.html","position":2,"title":"Kebijakan Privasi"}}]]></b:widget-setting>
                          <b:widget-setting name='homeTitle'>Beranda</b:widget-setting>
                        </b:widget-settings>
                        <b:includable id='main'>
                          <b:include name='content'/>
                        </b:includable>
                        <b:includable id='content'>
                          <b:include name='pageList'/>
                        </b:includable>
                        <b:includable id='overflowButton'/>
                        <b:includable id='overflowablePageList'/>
                        <b:includable id='pageLink'>
                          <b:if cond='data:t &lt;= 3'>
                            <li>
                              <b:class cond='data:overflow' name='overflowable-item'/>
                              <b:class cond='data:link.isCurrentPage' name='selected'/>
                               <b:tag expr:name='data:link.href != &quot;#&quot; ? &quot;a&quot; : &quot;span&quot;'>
                                <b:attr cond='data:link.href != &quot;#&quot;' expr:value='data:link.href' name='href'/>
                                <data:link.title/>
                              </b:tag>
                            </li>
                          </b:if>
                        </b:includable>
                        <b:includable id='pageList'>
                          <ul class='mMenu'>
                            <b:class cond='data:pageListClass' expr:name='data:pageListClass'/>
                            <b:loop index='t' values='data:links' var='link'>
                              <b:include name='pageLink'/>
                            </b:loop>
                          </ul>
                        </b:includable>
                      </b:widget>
                      <b:widget id='LinkList002' locked='true' title='Social Media' type='LinkList' version='2' visible='true'>
                        <b:widget-settings>
                          <b:widget-setting name='shownum'>3</b:widget-setting>
                          <b:widget-setting name='sorting'>NONE</b:widget-setting>
                          <b:widget-setting name='text-1'>Tiktok</b:widget-setting>
                          <b:widget-setting name='link-1'>https://www.tiktok.com/@trjy17_</b:widget-setting>
                          <b:widget-setting name='text-0'>Instagram</b:widget-setting>
                          <b:widget-setting name='link-2'>https://www.youtube.com/c/Ppanji_</b:widget-setting>
                          <b:widget-setting name='link-0'>https://www.instagram.com/trjy17/</b:widget-setting>
                          <b:widget-setting name='text-2'>Youtube</b:widget-setting>
                        </b:widget-settings>
                        <b:includable id='main'>
                          <b:include name='content'/>
                        </b:includable>
                        <b:includable id='content'>
                          <ul class='mSoc'>
                            <b:loop index='soc' values='data:links' var='link'>
                              <b:if cond='data:soc &lt;= 5'>
                                <li>
                                  <b:tag class='a tIc bIc' expr:name='data:link.target != &quot;#&quot; ? &quot;a&quot; : &quot;span&quot;'>
                                    <b:attr cond='data:link.target != &quot;#&quot;' expr:value='data:link.target' name='href'/>
                                    <b:attr cond='data:link.target != &quot;#&quot;' name='role' value='button'/>
                                    <b:attr cond='data:link.target != &quot;#&quot;' expr:value='data:link.name' name='aria-label'/>
                                    <b:attr cond='data:link.target != &quot;#&quot;' name='target' value='_blank'/>
                                    <b:attr cond='data:link.target != &quot;#&quot;' name='rel' value='noopener'/>
                                    <b:if cond='data:link.name == &quot;Facebook&quot;'>
                                      <b:include name='facebook-icon'/>
                              
                                      <b:elseif cond='data:link.name == &quot;Instagram&quot;'/>
                                      <b:include name='instagram-icon'/>
                              
                                      <b:elseif cond='data:link.name == &quot;Twitter&quot;'/>
                                      <b:include name='twitter-icon'/>
                              
                                      <b:elseif cond='data:link.name == &quot;Youtube&quot;'/>
                                      <b:include name='youtube-icon'/>
                              
                                      <b:elseif cond='data:link.name == &quot;LinkedIn&quot;'/>
                                      <b:include name='linkedIn-icon'/>
                              
                                      <b:elseif cond='data:link.name == &quot;Pinterest&quot;'/>
                                      <b:include name='pinterest-icon'/>
                            
                                      <b:elseif cond='data:link.name == &quot;Whatsapp&quot;'/>
                                      <b:include name='whatsapp-icon'/>
                              
                                      <b:elseif cond='data:link.name == &quot;Telegram&quot;'/>
                                      <b:include name='telegram-icon'/>
                              
                                      <b:elseif cond='data:link.name == &quot;Tiktok&quot;'/>
                                      <b:include name='tiktok-icon'/>
                              
                                      <b:else/>
                                      <b:include name='circle-icon'/>
                                    </b:if>
                                  </b:tag>
                                </li>
                              </b:if>
                            </b:loop>
                          </ul>
                        </b:includable>
                      </b:widget>
                    </b:section>
                
                    <b:section class='mnMen' id='header-Menu' maxwidgets='2' showaddelement='false'>
                      <b:widget id='HTML000' locked='true' title='Navigation Menu' type='HTML' version='2' visible='true'>
                        <b:widget-settings>
                          <b:widget-setting name='content'><![CDATA[<!--[ you can only edit this widget from HTML theme ]-->]]></b:widget-setting>
                        </b:widget-settings>
                        <b:includable id='main'>
                          <ul class='mnMn' itemscope='itemscope' itemtype='https://schema.org/SiteNavigationElement'>
                  
                            <b:if cond='!data:view.isHomepage'>
                              <!--[ Home link ]-->
                              <li class='hm'>
                                <a class='a' expr:href='data:blog.homepageUrl.canonical' itemprop='url'>
                                  <b:include name='home-icon'/>
                        
                                  <!--[ Title navigation ]-->
                                  <span class='n' itemprop='name'><data:messages.home/></span>
                                </a>
                              </li>
                            </b:if>
                    
                            <!--[ Dropdown style 1 ]-->
                            <li class='drp'>
                              <input class='drpI hidden' id='drpDwn-1' name='drpDwn' type='checkbox'/>
                              <label class='a' for='drpDwn-1'>
                                <!--[ Icon ]-->
                                <b:include name='folder-icon'/>
                          
                                <!--[ Title navigation ]-->
                                <span class='n'>Kategori</span>
                        
                                <b:include name='arow-down-icon'/>
                              </label>
                              <ul>
                                <!--[ Change attribute href='#' to add url ]-->
                                <li itemprop='name'><a href='https://www.trjy17.com/search/label/Artikel' itemprop='url'>Artikel</a></li>
                                <li itemprop='name'><a href='https://www.trjy17.com/search/label/Pendidikan' itemprop='url'>Pendidikan</a></li>
                                <li itemprop='name'><a href='https://www.trjy17.com/search/label/Tutorial' itemprop='url'>Tutorial</a></li>
                              </ul>
                            </li>
                            
                              <!--[ Dropdown style 2 ]-->
                            <li class='drp'>
                              <input class='drpI hidden' id='drpDwn-2' name='drpDwn' type='checkbox'/>
                              <label class='a' for='drpDwn-2'>
                                <!--[ Icon ]-->
                                <b:include name='folder-icon'/>
                          
                                <!--[ Title navigation ]-->
                                <span class='n'>Kegiatan</span>
                        
                                <b:include name='arow-down-icon'/>
                              </label>
                              <ul>
                                <!--[ Change attribute href='#' to add url ]-->
                                <li itemprop='name'><a href='https://www.trjy17.com/search/label/Guru' itemprop='url'>Guru</a></li>
                                <li itemprop='name'><a href='https://www.trjy17.com/search/label/Siswa' itemprop='url'>Siswa</a></li>
                              </ul>
                            </li>
                            
                             <!--[ Dropdown style 3 ]-->
                            <li class='drp'>
                              <input class='drpI hidden' id='drpDwn-3' name='drpDwn' type='checkbox'/>
                              <label class='a' for='drpDwn-3'>
                                <!--[ Icon ]-->
                                <b:include name='gear-icon'/>
                          
                                <!--[ Title navigation ]-->
                                <span class='n'>Alat</span>
                        
                                <b:include name='arow-down-icon'/>
                              </label>
                              <ul>
                                <!--[ Change attribute href='#' to add url ]-->
                                <li itemprop='name'><a href='https://www.trjy17.com/p/gdrive-generator.html' itemprop='url'>Gdrive Generator</a></li>
                                <li itemprop='name'><a href='https://sites.google.com/view/ppnj/alat/html-editor' itemprop='url'>HTML Editor</a></li>
                              </ul>
                            </li>
                            
                            <!--[ Dropdown style 4 ]-->
                            <li class='drp br'>
                              <input class='drpI hidden' id='drpDwn-4' name='drpDwn' type='checkbox'/>
                              <label class='a' for='drpDwn-4'>
                                <!--[ Icon ]-->
                                <b:include name='game-icon'/>
                          
                                <!--[ Title navigation ]-->
                                <span class='n'>Permainan</span>
                        
                                <b:include name='arow-down-icon'/>
                              </label>
                              <ul>
                                <!--[ Change attribute href='#' to add url ]-->
                                <li itemprop='name'><a href='https://sites.google.com/view/ppnj/game/t-rex' itemprop='url'>T-Rex</a></li>
                              </ul>
                            </li>
                            
                            <!--[ Standar menu ]-->
                            <li>
                              <!--[ Change attribute href='#' to add url ]-->
                              <a class='a' href='https://www.trjy17.com/search/label/E-book' itemprop='url'>
                                <!--[ Icon ]-->
                                <b:include name='phone-icon'/>
                          
                                <!--[ Title navigation ]-->
                                <span class='n' itemprop='name'>E-book</span>
                              </a>
                            </li>
                            
                            <!--[ Standar menu ]-->
                            <li class='br'>
                              <!--[ Change attribute href='#' to add url ]-->
                              <a class='a' href='https://www.trjy17.com/search/label/Unduhan' itemprop='url'>
                                <!--[ Icon ]-->
                                <b:include name='download-alt-icon'/>
                          
                                <!--[ Title navigation ]-->
                                <span class='n' itemprop='name'>Unduhan</span>
                              </a>
                            </li>

                            <!--[ Standar menu ]-->
                            <li>
                              <!--[ Change attribute href='#' to add url ]-->
                              <a class='a' href='https://www.trjy17.com/p/tentang-trjy17_8.html' itemprop='url'>
                                <!--[ Icon ]-->
                                <b:include name='profiles-icon'/>
                          
                                <!--[ Title navigation ]-->
                                <span class='n' itemprop='name'>Tentang</span>
                              </a>
                            </li>
                            
                            <!--[ Standar menu ]-->
                            <li class='n'>
                              <!--[ Change attribute href='#' to add url ]-->
                              <a class='a' href='https://www.trjy17.com/p/kontak_6.html' itemprop='url'>
                                <!--[ Icon ]-->
                                <b:include name='message-icon'/>
                          
                                <!--[ Title navigation ]-->
                                <span class='n' itemprop='name'>Kontak</span>
                              </a>
                            </li>
                          
                          </ul>
                        </b:includable>
                      </b:widget>
                      <b:widget id='PageList000' locked='true' title='Navigation Menu (Simple)' type='PageList' version='2' visible='false'>
                        <b:widget-settings>
                          <b:widget-setting name='pageListJson'>{}</b:widget-setting>
                          <b:widget-setting name='homeTitle'>Beranda</b:widget-setting>
                        </b:widget-settings>
                        <b:includable id='main'>
                          <b:include name='content'/>
                        </b:includable>
                        <b:includable id='content'>
                          <b:include name='pageList'/>
                        </b:includable>
                        <b:includable id='overflowButton'/>
                        <b:includable id='overflowablePageList'/>
                        <b:includable id='pageLink'>
                          <b:if cond='data:i &lt;= 4'>
                            <li>
                              <b:class cond='data:link.isCurrentPage' name='selected'/>
                              <b:class cond='data:link.href == data:blog.homepageUrl.canonical' name='hm'/>
                        
                              <b:tag class='a' expr:name='!data:link.isCurrentPage and data:link.href != &quot;#&quot; ? &quot;a&quot; : &quot;span&quot;'>
                                <b:attr cond='!data:link.isCurrentPage and data:link.href != &quot;#&quot;' expr:value='data:link.href' name='href'/>
                                <b:attr cond='!data:link.isCurrentPage and data:link.href != &quot;#&quot;' name='itemprop' value='url'/>
                              
                                <!--[ Icon ]-->
                                <b:if cond='data:link.title == &quot;Home&quot;'>
                                  <b:include name='home-icon'/>
                                
                                  <b:elseif cond='data:link.title == &quot;About&quot;'/>
                                  <b:include name='profiles-icon'/>
                              
                                  <b:elseif cond='data:link.title == &quot;Contact&quot;'/>
                                  <b:include name='message-icon'/>
                                
                                  <b:elseif cond='data:link.title == &quot;Download this theme&quot; or data:link.title == &quot;Download&quot;'/>
                                  <b:include name='download-icon'/>
                              
                                  <b:elseif cond='data:link.title == &quot;Sitemap&quot;'/>
                                  <b:include name='document-icon'/>
                          
                                  <b:elseif cond='data:link.title == &quot;Disclaimers&quot;'/>
                                  <b:include name='shield-done-icon'/>
                          
                                  <b:elseif cond='data:link.title == &quot;Privacy&quot;'/>
                                  <b:include name='lock-icon'/>
                                
                                  <b:else/>
                                  <b:include name='folder-icon'/>
                                </b:if>
                              
                                <!--[ Title navigation ]-->
                                <span class='n'>
                                  <b:attr cond='!data:link.isCurrentPage and data:link.href != &quot;#&quot;' name='itemprop' value='name'/>
                                  <data:link.title/>
                                </span>
                              </b:tag>
                            </li>
                          </b:if>
                        
                          <b:if cond='data:i == 5'>
                            <li class='drp'>
                              <input class='drpI hidden' id='drpDwn-00' name='drpDwn' type='checkbox'/>
                              <label class='a' for='drpDwn-00'>
                                <!--[ Icon ]-->
                                <b:include name='folder-icon'/>
                              
                                <!--[ Title navigation ]-->
                                <span class='n'><data:messages.moreEllipsis/></span>
                        
                                <b:include name='arow-down-icon'/>
                              </label>
                              <ul>
                                <b:loop index='all' values='data:links' var='link'>
                                  <b:if cond='data:all &gt;= 5'>
                                    <li>
                                      <b:attr cond='!data:link.isCurrentPage and data:link.href != &quot;#&quot;' name='itemprop' value='name'/>
                                  
                                      <b:tag expr:name='!data:link.isCurrentPage and data:link.href != &quot;#&quot; ? &quot;a&quot; : &quot;span&quot;'>
                                        <b:attr cond='!data:link.isCurrentPage and data:link.href != &quot;#&quot;' expr:value='data:link.href' name='href'/>
                                        <b:attr cond='!data:link.isCurrentPage and data:link.href != &quot;#&quot;' name='itemprop' value='url'/>
                                        <data:link.title/>
                                      </b:tag>
                                    </li>
                                  </b:if>
                                </b:loop>
                              </ul>
                            </li>
                          </b:if>
                        </b:includable>
                        <b:includable id='pageList'>
                          <ul class='mnMn' itemscope='itemscope' itemtype='https://schema.org/SiteNavigationElement'>
                            <b:loop index='i' values='data:links' var='link'>
                              <b:include name='pageLink'/>
                            </b:loop>
                          </ul>
                        </b:includable>
                      </b:widget>
                    </b:section>
                  </div>
                </div>
                <label class='fCls' for='offNav'/>
              </div>
            
              <b:tag class='headD headR' name='div'>
                <b:tag class='headI' cond='!data:view.isLayoutMode' name='div'>
                  <b:section class='headP' id='header-icon' maxwidgets='2' showaddelement='false'>
                    <b:widget id='TextList000' locked='true' title='Header Icon' type='TextList' version='2' visible='true'>
                      <b:widget-settings>
                        <b:widget-setting name='shownum'>3</b:widget-setting>
                        <b:widget-setting name='sorting'>NONE</b:widget-setting>
                        <b:widget-setting name='item-2'>Profile</b:widget-setting>
                        <b:widget-setting name='item-1'>Search</b:widget-setting>
                        <b:widget-setting name='item-0'>Dark</b:widget-setting>
                      </b:widget-settings>
                      <b:includable id='main'>
                        <b:include name='content'/>
                      </b:includable>
                      <b:includable id='content'>
                        <ul class='headIc'>
                          <b:loop index='icon' values='data:items' var='item'>
                            <b:if cond='data:icon &lt;= 2'>
                              <b:if cond='data:item == &quot;Search&quot;'>
                                <li>
                                  <b:class cond='data:item == &quot;Search&quot;' name='isSrh'/>
                                  <!--[ Search button ]-->
                                  <label class='tSrch tIc bIc' expr:aria-label='data:item' for='offSrh'><b:include name='search-icon'/></label>
                                </li>
                                
                                <b:elseif cond='data:item == &quot;Dark&quot;'/>
                                
                                
                                
                                <b:if cond='data:view.url != data:view.url params { amp: &quot;1&quot; }'>
                                  <li>
                                    <b:class cond='data:item == &quot;Dark&quot;' name='isDrk'/>
                                    <!--[ Dark mode button ]-->
                                    <span class='tDark tIc tDL bIc' expr:aria-label='data:item' onclick='darkMode()' role='button'><b:include name='moon-sun-icon'/></span>
                                  </li>
                                </b:if>
                              </b:if>
                            </b:if>
                          </b:loop>
                        </ul>
                      </b:includable>
                    </b:widget>
                  </b:section>
                </b:tag>
              </b:tag>
            </b:tag>
          </b:tag>
        </header>
        
        <!--[ SearchBox section ]-->
        <input class='srhI fixi hidden' id='offSrh' type='checkbox'/>
        <div class='srhB fixL'>
          <div class='srhBi fixLi'>
            <b:section class='srhBs fixLs' id='search-widget' maxwidgets='2' showaddelement='false'>
              <b:widget id='BlogSearch1' locked='true' title='Try &apos;Pendidikan&apos;' type='BlogSearch' version='2' visible='true'>
                <b:includable id='main'>
                  <b:include name='content'/>
                </b:includable>
                <b:includable id='content'>
                  <b:include name='searchForm'/>
                </b:includable>
                <b:includable id='searchForm'>
                  <form class='srhF' expr:action='data:blog.searchUrl'>
                    <b:attr cond='not data:view.isPreview' name='target' value='_top'/>
                    <b:include name='urlParamsAsFormInput'/>
                    <b:include name='searchSubmit'/>
                    <input autocomplete='off' expr:aria-label='data:messages.searchThisBlog' expr:placeholder='data:title' expr:value='data:view.isSearch ? data:view.search.query.escaped : &quot;&quot;' id='searchIn' minlength='3' name='q' required='required' type='search'/>
                    <button aria-label='Clear' class='sb' data-text='Clear' type='reset'/>
                  </form>
                  <label aria-label='Close' class='srhC c' for='offSrh'/>
                </b:includable>
                <b:includable id='searchSubmit'>
                  <label class='sb' for='searchIn'><b:include name='search-icon'/></label>
                </b:includable>
              </b:widget>
              <b:widget id='Label1' locked='true' title='Search Suggest' type='Label' version='2' visible='true'>
                <b:widget-settings>
                  <b:widget-setting name='sorting'>ALPHA</b:widget-setting>
                  <b:widget-setting name='display'>CLOUD</b:widget-setting>
                  <b:widget-setting name='selectedLabelsList'/>
                  <b:widget-setting name='showType'>ALL</b:widget-setting>
                  <b:widget-setting name='showFreqNumbers'>true</b:widget-setting>
                </b:widget-settings>
                <b:includable id='main' var='this'>
                  <b:if cond='data:title != &quot;&quot;'>
                    <h2 class='title'><data:title/></h2>
                  </b:if>
                  <b:include name='content'/>
                </b:includable>
                <b:includable id='cloud'>
                  <b:loop index='tags' values='data:labels' var='label'>
                         
                    <!--[ Only show 10 label ]-->
                    <b:if cond='data:tags &lt;= 9'>
                      <div class='lbSz'>
                        <b:class expr:name='&quot;s-&quot; + data:label.cssSize'/>
                        <b:tag class='lbN' expr:name='data:blog.url != data:label.url ? &quot;a&quot; : &quot;div&quot;'>
                          <b:attr cond='data:blog.url != data:label.url' expr:value='data:label.url' name='href'/>
                          <b:attr cond='data:blog.url != data:label.url' expr:value='data:label.name' name='aria-label'/>
                          <span class='lbT'><data:label.name/></span>
                          <b:tag class='lbC' cond='data:this.showFreqNumbers' expr:data-text='&quot;(&quot; + data:label.count + &quot;)&quot;' name='span'/>
                        </b:tag>
                      </div>
                    </b:if>
                        
                    <!--[ Hide another label from 11th list ]-->
                    <b:if cond='data:tags == 10'>
                      <div class='lbSh'>
                        <input class='lbIn hidden' id='lbAl-1' type='checkbox'/>
                        <div class='lbAl'>
                          <b:loop index='alltags' values='data:labels' var='label'>
                               
                            <!--[ Show label from 7th list ]-->
                            <b:if cond='data:alltags &gt;= 10'>
                              <div class='lbSz'>
                                <b:class expr:name='&quot;s-&quot; + data:label.cssSize'/>
                                <b:tag class='lbN' expr:name='data:blog.url != data:label.url ? &quot;a&quot; : &quot;div&quot;'>
                                  <b:attr cond='data:blog.url != data:label.url' expr:value='data:label.url' name='href'/>
                                  <b:attr cond='data:blog.url != data:label.url' expr:value='data:label.name' name='aria-label'/>
                                  <span class='lbT'><data:label.name/></span>
                                  <b:tag class='lbC' cond='data:this.showFreqNumbers' expr:data-text='&quot;(&quot; + data:label.count + &quot;)&quot;' name='span'/>
                                </b:tag>
                              </div>
                            </b:if>
                                
                          </b:loop>
                        </div>
                            
                        <label aria-label='Show labels' class='lbM' expr:data-hide='data:messages.showLess' expr:data-show='data:messages.showMore' expr:data-text='&quot;(+&quot; + (data:labels.length - 10) + &quot;)&quot;' for='lbAl-1'/>
                      </div>
                    </b:if>
                  </b:loop>
                </b:includable>
                <b:includable id='content'>
                  <div class='wL pSml'>
                    <b:class expr:name='data:this.display == &quot;list&quot; ? &quot;ls&quot; : &quot;cl&quot;'/>
                    <b:include cond='data:this.display == &quot;list&quot;' name='list'/>
                    <b:include cond='data:this.display == &quot;cloud&quot;' name='cloud'/>
                  </div>
                </b:includable>
                <b:includable id='list'>
                  <b:include name='cloud'/>
                </b:includable>
              </b:widget>
            </b:section>
          </div>
          <label class='fCls' for='offSrh'/>
        </div>
        
        <!--[ Scroll menu ]-->
        <nav class='navI scrlH'>
          <b:section class='secIn' id='scroll-menu' maxwidgets='1' showaddelement='false'>
            <b:widget id='LinkList001' locked='true' title='Scroll Menu' type='LinkList' version='2' visible='false'>
              <b:widget-settings>
                <b:widget-setting name='text-9'>Topics 10</b:widget-setting>
                <b:widget-setting name='link-9'>#</b:widget-setting>
                <b:widget-setting name='text-8'>Topics 09</b:widget-setting>
                <b:widget-setting name='link-7'>#</b:widget-setting>
                <b:widget-setting name='link-8'>#</b:widget-setting>
                <b:widget-setting name='link-5'>#</b:widget-setting>
                <b:widget-setting name='link-6'>#</b:widget-setting>
                <b:widget-setting name='link-3'>#</b:widget-setting>
                <b:widget-setting name='link-4'>#</b:widget-setting>
                <b:widget-setting name='text-1'>Topics 02</b:widget-setting>
                <b:widget-setting name='text-0'>Topics 01</b:widget-setting>
                <b:widget-setting name='text-3'>Topics 04</b:widget-setting>
                <b:widget-setting name='text-2'>Topics 03</b:widget-setting>
                <b:widget-setting name='text-5'>Topics 06</b:widget-setting>
                <b:widget-setting name='text-4'>Topics 05</b:widget-setting>
                <b:widget-setting name='text-7'>Topics 08</b:widget-setting>
                <b:widget-setting name='text-6'>Topics 07</b:widget-setting>
                <b:widget-setting name='sorting'>NONE</b:widget-setting>
                <b:widget-setting name='link-1'>#</b:widget-setting>
                <b:widget-setting name='link-2'>#</b:widget-setting>
                <b:widget-setting name='link-0'>#</b:widget-setting>
              </b:widget-settings>
              <b:includable id='main'>
                <b:include name='content'/>
              </b:includable>
              <b:includable id='content'>
                <ul>
                  <b:loop index='s' values='data:links' var='link'>
                    <b:if cond='data:s &lt;= 12'>
                      <li>
                        <b:tag class='l' expr:data-text='data:link.name' expr:name='data:link.target != &quot;#&quot; and data:link.target != data:blog.url.canonical ? &quot;a&quot; : &quot;span&quot;'>
                          <b:attr cond='data:link.target != &quot;#&quot; and data:link.target != data:blog.url.canonical' expr:value='data:link.target' name='href'/>
                          <b:attr cond='data:link.target != &quot;#&quot; and data:link.target != data:blog.url.canonical' expr:value='data:link.name' name='aria-label'/>
                          <b:class cond='data:link.target == data:blog.url.canonical' name='a'/>
                        </b:tag>
                      </li>
                    </b:if>
                  </b:loop>
                </ul>
              </b:includable>
            </b:widget>
          </b:section>
        </nav>
        
        <!--[ Content section ]-->
        <div class='mainIn'>
          
          <!--[ Blog content ]-->
          <div class='blogCont'>
            <div class='secIn'>
                
              <b:if cond='!data:view.isPreview'>
                <!--[ Ad content ]-->
                <b:tag class='blogAd' name='div'>
                  <b:section id='horizontal-ad' maxwidgets='3' showaddelement='true'>
                    <b:widget id='HTML91' locked='true' title='Under header ad' type='HTML' version='2' visible='false'>
                      <b:widget-settings>
                        <b:widget-setting name='content'>&lt;ins class=&quot;adsbygoogle&quot;
     style=&quot;display:block&quot;
     data-ad-client=&quot;ca-pub-3400053731432707&quot;
     data-ad-slot=&quot;4052950217&quot;
     data-ad-format=&quot;auto&quot;
     data-full-width-responsive=&quot;true&quot;&gt;&lt;/ins&gt;
&lt;script&gt;
     (adsbygoogle = window.adsbygoogle || []).push({});
&lt;/script&gt;</b:widget-setting>
                      </b:widget-settings>
                      <b:includable id='main'>
                        <b:if cond='data:content != &quot;&quot;'>
                          <data:content/>
                          
                          <b:else/>
                          <!--[ Blank ad ]-->
                          <div class='adB' expr:data-text='data:messages.adsGoHere'/>
                        </b:if>
                      </b:includable>
                    </b:widget>
                  </b:section>
                </b:tag>
              </b:if>
              
              <b:tag class='blogM' name='div'>
                <!--[ Main content ]-->
                <main class='blogItm mainbar'>
                    
                  <b:if cond='data:view.isHomepage'>
                    <b:section aria-label='Gallery' class='sldO scrlH' id='slider-widget' maxwidgets='4' showaddelement='false'>
                      <b:widget id='Image1' locked='true' title='' type='Image' version='2' visible='true'>
                        <b:widget-settings>
                          <b:widget-setting name='displayUrl'>https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh4Y9mW9sYW0sqzyLMl85C7B1ulhf0FPg9L0colRW9LiB8JGenlBaLh0m-TR1UMzEJPmsUzvuSqDciuYdAqj9URfu4lttM9r4HGzGMe0HYFY0wLkvCBMfderE6ppwjdLzrqPMrC8mw9Gfm8Nyp7m5fdGZNEqvB1aVVZMl8i3xIo6x-WU_PzPAqkFK7u2A/s1600/1.png</b:widget-setting>
                          <b:widget-setting name='displayHeight'>650</b:widget-setting>
                          <b:widget-setting name='sectionWidth'>150</b:widget-setting>
                          <b:widget-setting name='shrinkToFit'>false</b:widget-setting>
                          <b:widget-setting name='displayWidth'>1600</b:widget-setting>
                          <b:widget-setting name='link'/>
                          <b:widget-setting name='caption'/>
                        </b:widget-settings>
                        <b:includable id='main'>
                          <b:include name='content'/>
                        </b:includable>
                        <b:includable id='content'>
                          <div class='sldC' expr:id='data:widget.instanceId + &quot;_img&quot;'>
                            <b:tag class='sldIm' expr:data-style='&quot;background-image: url(&quot; + data:sourceUrl + &quot;)&quot;' expr:name='data:link ? &quot;a&quot; : &quot;div&quot;'>
                              <b:class cond='data:view.url != data:view.url params { amp: &quot;1&quot; }' name='lazy'/>
                              <b:attr cond='data:view.url == data:view.url params { amp: &quot;1&quot; }' expr:value='&quot;background-image: url(&quot; + data:sourceUrl + &quot;)&quot;' name='style'/>
                              <b:attr cond='data:link' expr:value='data:link' name='href'/>
                              <b:attr cond='data:link' expr:value='data:title' name='aria-label'/>
                              <b:if cond='data:caption'><span class='sldT'><data:caption/></span></b:if>
                            </b:tag>
                            <noscript>
                              <b:tag class='sldIm' expr:name='data:link ? &quot;a&quot; : &quot;div&quot;' expr:style='&quot;background-image: url(&quot; + data:sourceUrl + &quot;)&quot;'>
                                <b:attr cond='data:link' expr:value='data:link' name='href'/>
                                <b:attr cond='data:link' expr:value='data:title' name='aria-label'/>
                                <b:if cond='data:caption'><span class='sldT'><data:caption/></span></b:if>
                              </b:tag>
                            </noscript>
                          </div>
                          <div class='sldS'/>
                        </b:includable>
                      </b:widget>
                      <b:widget id='Image2' locked='true' title='' type='Image' version='2' visible='true'>
                        <b:widget-settings>
                          <b:widget-setting name='displayUrl'>https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhxlysPEOkYy1qSTUHFd3HLkg9uV_25v5Atx1KkCNQhY6FIbBTHENLlvfIMPmd9RY_GDQ2ILPa3W7dHdS6Xy8iu9AWGwpbdUbIR9fgmD6NxO4uTqPAiuf-TwzxbZ1w1cR9oVAUQRFoTmQ4to3ILD0mktDJwiJJIcq5twRCVhYXXtCf2MSMeHOv6R5w-Sg/s1600/2.png</b:widget-setting>
                          <b:widget-setting name='displayHeight'>650</b:widget-setting>
                          <b:widget-setting name='sectionWidth'>150</b:widget-setting>
                          <b:widget-setting name='shrinkToFit'>false</b:widget-setting>
                          <b:widget-setting name='displayWidth'>1600</b:widget-setting>
                          <b:widget-setting name='link'/>
                          <b:widget-setting name='caption'/>
                        </b:widget-settings>
                        <b:includable id='main'>
                          <b:include name='content'/>
                        </b:includable>
                        <b:includable id='content'>
                          <div class='sldC' expr:id='data:widget.instanceId + &quot;_img&quot;'>
                            <b:tag class='sldIm' expr:data-style='&quot;background-image: url(&quot; + data:sourceUrl + &quot;)&quot;' expr:name='data:link ? &quot;a&quot; : &quot;div&quot;'>
                              <b:class cond='data:view.url != data:view.url params { amp: &quot;1&quot; }' name='lazy'/>
                              <b:attr cond='data:view.url == data:view.url params { amp: &quot;1&quot; }' expr:value='&quot;background-image: url(&quot; + data:sourceUrl + &quot;)&quot;' name='style'/>
                              <b:attr cond='data:link' expr:value='data:link' name='href'/>
                              <b:attr cond='data:link' expr:value='data:title' name='aria-label'/>
                              <b:if cond='data:caption'><span class='sldT'><data:caption/></span></b:if>                                
                            </b:tag>
                            <noscript>
                              <b:tag class='sldIm' expr:name='data:link ? &quot;a&quot; : &quot;div&quot;' expr:style='&quot;background-image: url(&quot; + data:sourceUrl + &quot;)&quot;'>
                                <b:attr cond='data:link' expr:value='data:link' name='href'/>
                                <b:attr cond='data:link' expr:value='data:title' name='aria-label'/>
                                <b:if cond='data:caption'><span class='sldT'><data:caption/></span></b:if>
                              </b:tag>
                            </noscript>
                          </div>
                          <div class='sldS'/>
                        </b:includable>
                      </b:widget>
                      <b:widget id='Image3' locked='true' title='' type='Image' version='2' visible='true'>
                        <b:widget-settings>
                          <b:widget-setting name='displayUrl'>https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgaD3yfSL9k152PaKh73SWOOhfv0UksjERCcmLFULDI84_vqgekW0hiJo3OsN9zukB1g7qMHyzuOAz7BNqsDdiMNFt2ioRkOXBy5ooMJFEuf8yLhG-Fzv-3Oaz7k6IIW0tIVkmFNhTPa6ubgBO43kiwsqMYX8XwDzerPz-Zj7eoiVokidZyIviBJpwR1A/s1600/3.png</b:widget-setting>
                          <b:widget-setting name='displayHeight'>650</b:widget-setting>
                          <b:widget-setting name='sectionWidth'>150</b:widget-setting>
                          <b:widget-setting name='shrinkToFit'>false</b:widget-setting>
                          <b:widget-setting name='displayWidth'>1600</b:widget-setting>
                          <b:widget-setting name='link'/>
                          <b:widget-setting name='caption'/>
                        </b:widget-settings>
                        <b:includable id='main'>
                          <b:include name='content'/>
                        </b:includable>
                        <b:includable id='content'>
                          <div class='sldC' expr:id='data:widget.instanceId + &quot;_img&quot;'>
                            <b:tag class='sldIm' expr:data-style='&quot;background-image: url(&quot; + data:sourceUrl + &quot;)&quot;' expr:name='data:link ? &quot;a&quot; : &quot;div&quot;'>
                              <b:class cond='data:view.url != data:view.url params { amp: &quot;1&quot; }' name='lazy'/>
                              <b:attr cond='data:view.url == data:view.url params { amp: &quot;1&quot; }' expr:value='&quot;background-image: url(&quot; + data:sourceUrl + &quot;)&quot;' name='style'/>
                              <b:attr cond='data:link' expr:value='data:link' name='href'/>
                              <b:attr cond='data:link' expr:value='data:title' name='aria-label'/>
                              <b:if cond='data:caption'><span class='sldT'><data:caption/></span></b:if>                                
                            </b:tag>
                            <noscript>
                              <b:tag class='sldIm' expr:name='data:link ? &quot;a&quot; : &quot;div&quot;' expr:style='&quot;background-image: url(&quot; + data:sourceUrl + &quot;)&quot;'>
                                <b:attr cond='data:link' expr:value='data:link' name='href'/>
                                <b:attr cond='data:link' expr:value='data:title' name='aria-label'/>
                                <b:if cond='data:caption'><span class='sldT'><data:caption/></span></b:if>
                              </b:tag>
                            </noscript>
                          </div>
                          <div class='sldS'/>
                        </b:includable>
                      </b:widget>
                      <b:widget id='Image4' locked='true' title='' type='Image' version='2' visible='true'>
                        <b:widget-settings>
                          <b:widget-setting name='displayUrl'>https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgxdK_FORQaaOE24nQTSZ9Ho7aLtjV5C7d2LQBJCuaW83fbHgcnMIfcWko4NnBXX1aHspGXWauUsxZ8wd-U6XvYMybhIyBT-u5cKc4RyHSslj7rq_G7Rq8sF4xvBaKv3xH8a5mE_2PFbpRsM31qColxUptmLmvNZBLk1hDKfoYunKelTzZuyuJhGqkXWA/s1600/4.png</b:widget-setting>
                          <b:widget-setting name='displayHeight'>650</b:widget-setting>
                          <b:widget-setting name='sectionWidth'>150</b:widget-setting>
                          <b:widget-setting name='shrinkToFit'>false</b:widget-setting>
                          <b:widget-setting name='displayWidth'>1600</b:widget-setting>
                          <b:widget-setting name='link'/>
                          <b:widget-setting name='caption'/>
                        </b:widget-settings>
                        <b:includable id='main'>
                          <b:include name='content'/>
                        </b:includable>
                        <b:includable id='content'>
                          <div class='sldC' expr:id='data:widget.instanceId + &quot;_img&quot;'>
                            <b:tag class='sldIm' expr:data-style='&quot;background-image: url(&quot; + data:sourceUrl + &quot;)&quot;' expr:name='data:link ? &quot;a&quot; : &quot;div&quot;'>
                              <b:class cond='data:view.url != data:view.url params { amp: &quot;1&quot; }' name='lazy'/>
                              <b:attr cond='data:view.url == data:view.url params { amp: &quot;1&quot; }' expr:value='&quot;background-image: url(&quot; + data:sourceUrl + &quot;)&quot;' name='style'/>
                              <b:attr cond='data:link' expr:value='data:link' name='href'/>
                              <b:attr cond='data:link' expr:value='data:title' name='aria-label'/>
                              <b:if cond='data:caption'><span class='sldT'><data:caption/></span></b:if>                                
                            </b:tag>
                            <noscript>
                              <b:tag class='sldIm' expr:name='data:link ? &quot;a&quot; : &quot;div&quot;' expr:style='&quot;background-image: url(&quot; + data:sourceUrl + &quot;)&quot;'>
                                <b:attr cond='data:link' expr:value='data:link' name='href'/>
                                <b:attr cond='data:link' expr:value='data:title' name='aria-label'/>
                                <b:if cond='data:caption'><span class='sldT'><data:caption/></span></b:if>
                              </b:tag>
                            </noscript>
                          </div>
                          <div class='sldS'/>
                        </b:includable>
                      </b:widget>
                    </b:section>
                  </b:if>
                    
                  <b:section cond='data:view.isHomepage' id='top-widget' showaddelement='true'>
                    <b:widget cond='!data:view.isPreview' id='HTML92' locked='true' title='Ad placement' type='HTML' version='2' visible='false'>
                      <b:widget-settings>
                        <b:widget-setting name='content'>&lt;ins class=&quot;adsbygoogle&quot;
     style=&quot;display:block&quot;
     data-ad-client=&quot;ca-pub-3400053731432707&quot;
     data-ad-slot=&quot;4052950217&quot;
     data-ad-format=&quot;auto&quot;
     data-full-width-responsive=&quot;true&quot;&gt;&lt;/ins&gt;
&lt;script&gt;
     (adsbygoogle = window.adsbygoogle || []).push({});
&lt;/script&gt;</b:widget-setting>
                      </b:widget-settings>
                      <b:includable id='main'>
                        <div class='widget-content'>
                          <b:if cond='data:content != &quot;&quot;'>
                            <data:content/>
                          
                            <b:else/>
                            <!--[ Blank ad ]-->
                            <div class='adB' expr:data-text='data:messages.adsGoHere'/>
                          </b:if>
                        </div>
                      </b:includable>
                    </b:widget>
                    <b:widget id='FeaturedPost1' locked='true' title='Pinned Post' type='FeaturedPost' version='2' visible='true'>
                      <b:widget-settings>
                        <b:widget-setting name='showSnippet'>true</b:widget-setting>
                        <b:widget-setting name='showPostTitle'>true</b:widget-setting>
                        <b:widget-setting name='postId'>0</b:widget-setting>
                        <b:widget-setting name='showFirstImage'>true</b:widget-setting>
                        <b:widget-setting name='useMostRecentPost'>true</b:widget-setting>
                      </b:widget-settings>
                      <b:includable id='main' var='this'>
                        <b:if cond='data:title != &quot;&quot;'>
                          <h2 class='title'><data:title/></h2>
                        </b:if>
                        <b:include name='snippetedPosts'/>
                      </b:includable>
                      <b:includable id='blogThisShare'/>
                      <b:includable id='bylineByName' var='byline'/>
                      <b:includable id='bylineRegion' var='regionItems'/>
                      <b:includable id='commentsLink'/>
                      <b:includable id='commentsLinkIframe'/>
                      <b:includable id='emailPostIcon'/>
                      <b:includable id='facebookShare'/>
                      <b:includable id='footerBylines'/>
                      <b:includable id='googlePlusShare'/>
                      <b:includable id='headerByline'/>
                      <b:includable id='linkShare'/>
                      <b:includable id='otherSharingButton'/>
                      <b:includable id='platformShare'/>
                      <b:includable id='postAuthor'/>
                      <b:includable id='postCommentsLink'/>
                      <b:includable id='postInfo'>
                        <div class='pInf pSml'>
                          <b:class cond='data:post.labels any (label =&gt; label.name in [ &quot;Sponsored&quot; ])' name='nSpr'/>
                          <b:if cond='data:post.labels none (label =&gt; label.name in [ &quot;Sponsored&quot; ])'>
                            <!--[ Post timestamp ]-->
                            <b:include cond='data:widgets.Blog.first.allBylineItems.timestamp' name='postTimestampPublish'/>
                          </b:if>
                    
                          <!--[ Post jumplinks ]-->
                          <b:include cond='data:widgets.Blog.first.allBylineItems.timestamp' name='postJumpLinks'/>
                        </div>
                      </b:includable>
                      <b:includable id='postJumpLink' var='post'/>
                      <b:includable id='postLabels'/>
                      <b:includable id='postLocation'/>
                      <b:includable id='postReactions'/>
                      <b:includable id='postShareButtons'/>
                      <b:includable id='postTimestamp'/>
                      <b:includable id='sharingButton'/>
                      <b:includable id='sharingButtonContent'/>
                      <b:includable id='sharingButtons'/>
                      <b:includable id='sharingButtonsMenu'/>
                      <b:includable id='sharingPlatformIcon'/>
                      <b:includable id='snippetedPostByline'/>
                      <b:includable id='snippetedPostContent'>
                        <!--[ Post Thumbnail ]-->
                        <b:include name='snippetedPostThumbnail'/>
                    
                        <div class='iCtnt'>
                          <!--[ Post header ]-->
                          <b:include name='postHeaders'/>
                          
                          <b:include cond='data:this.postDisplay.showTitle' name='snippetedPostTitle'/>
                          <b:include cond='data:this.postDisplay.showSnippet' name='snippetedPostEntry'/>
                      
                          <!--[ Post info ]-->
                          <b:include cond='!data:view.isPage' name='postInfo'/>
                        </div>
                      </b:includable>
                      <b:includable id='snippetedPostEntry'>
                        <div class='pSnpt'>
                          <b:include name='postEntrySnippet'/>
                        </div>
                      </b:includable>
                      <b:includable id='snippetedPostThumbnail'>
                        <div class='iThmb pThmb'>
                          <b:class cond='data:post.featuredImage.isYoutube' name='iyt'/>
                          <b:class cond='!data:this.postDisplay.showFeaturedImage or !data:post.featuredImage' name='nul'/>
                          <b:tag class='thmb' expr:name='data:this.postDisplay.showFeaturedImage and data:post.featuredImage ? &quot;a&quot; : &quot;div&quot;'>
                            <b:attr cond='data:this.postDisplay.showFeaturedImage and data:post.featuredImage' expr:value='data:post.url' name='href'/>
                            <b:if cond='data:this.postDisplay.showFeaturedImage and data:post.featuredImage'>
                              <b:include name='postEntryThumbnail'/>
                              <b:else/>
                              <span class='imgThm' data-text='No image'/>
                            </b:if>
                          </b:tag>
                          
                          <!--[ Comments count ]-->
                          <b:tag class='iFxd' cond='data:post.allowComments and data:post.numberOfComments &gt; 0 or data:post.labels any (label =&gt; label.name in [ &quot;Sponsored&quot; ])' name='div'>
                            <b:if cond='data:post.labels any (label =&gt; label.name in [ &quot;Sponsored&quot; ])'>
                              <b:include name='postSponsored'/>
                            </b:if>
                            <b:if cond='data:widgets.Blog.first.allBylineItems.comments'>
                              <b:include name='postCommentsLinks'/>
                            </b:if>
                          </b:tag>
                        </div>
                      </b:includable>
                      <b:includable id='snippetedPostTitle'>
                        <h3 class='pTtl aTtl'><a expr:href='data:post.url.canonical'><data:post.title.escaped/></a></h3>
                      </b:includable>
                      <b:includable id='snippetedPosts'>
                        <div class='itemFt' role='feed'>
                          <!-- Don't render the post that we're currently already looking at. -->
                          <b:loop values='data:posts filter (p =&gt; p.id != data:view.postId)' var='post'>
                            <article class='itm'>
                              <b:class cond='data:this.postDisplay.showFeaturedImage and !data:post.featuredImage' name='noThmb'/>
                              <b:class cond='!data:this.postDisplay.showFeaturedImage' name='noImage'/>
                              <b:include name='snippetedPostContent'/>
                            </article>
                          </b:loop>
                        </div>
                      </b:includable>
                    </b:widget>
                  </b:section>
                
                  <b:section id='main-widget' showaddelement='true'>
                    <b:widget cond='!data:view.isPreview and !data:blog.isMobileRequest and (data:view.isHomepage or data:view.isPost)' id='HTML93' locked='true' title='Ad placement' type='HTML' version='2' visible='true'>
                      <b:widget-settings>
                        <b:widget-setting name='content'>&lt;ins class=&quot;adsbygoogle&quot;
     style=&quot;display:block&quot;
     data-ad-client=&quot;ca-pub-3400053731432707&quot;
     data-ad-slot=&quot;4052950217&quot;
     data-ad-format=&quot;auto&quot;
     data-full-width-responsive=&quot;true&quot;&gt;&lt;/ins&gt;
&lt;script&gt;
     (adsbygoogle = window.adsbygoogle || []).push({});
&lt;/script&gt;</b:widget-setting>
                      </b:widget-settings>
                      <b:includable id='main'>
                        <div class='widget-content'>
                          <b:if cond='data:content != &quot;&quot;'>
                            <data:content/>
                          
                            <b:else/>
                            <!--[ Blank ad ]-->
                            <div class='adB' expr:data-text='data:messages.adsGoHere'/>
                          </b:if>
                        </div>
                      </b:includable>
                    </b:widget>
                    <b:widget id='Blog1' locked='true' title='Postingan Blog' type='Blog' version='2' visible='true'>
                      <b:widget-settings>
                        <b:widget-setting name='commentLabel'>Comment</b:widget-setting>
                        <b:widget-setting name='showShareButtons'>true</b:widget-setting>
                        <b:widget-setting name='authorLabel'>Oleh</b:widget-setting>
                        <b:widget-setting name='style.unittype'>TextAndImage</b:widget-setting>
                        <b:widget-setting name='timestampLabel'/>
                        <b:widget-setting name='reactionsLabel'/>
                        <b:widget-setting name='showAuthorProfile'>true</b:widget-setting>
                        <b:widget-setting name='style.layout'>1x1</b:widget-setting>
                        <b:widget-setting name='showLocation'>false</b:widget-setting>
                        <b:widget-setting name='showTimestamp'>true</b:widget-setting>
                        <b:widget-setting name='postsPerAd'>1</b:widget-setting>
                        <b:widget-setting name='style.bordercolor'>#000000</b:widget-setting>
                        <b:widget-setting name='showDateHeader'>false</b:widget-setting>
                        <b:widget-setting name='style.textcolor'>#767676</b:widget-setting>
                        <b:widget-setting name='showCommentLink'>true</b:widget-setting>
                        <b:widget-setting name='style.urlcolor'>#fffdfc</b:widget-setting>
                        <b:widget-setting name='postLocationLabel'>Location:</b:widget-setting>
                        <b:widget-setting name='showAuthor'>false</b:widget-setting>
                        <b:widget-setting name='style.linkcolor'>#2c7ef4</b:widget-setting>
                        <b:widget-setting name='style.bgcolor'>#000000</b:widget-setting>
                        <b:widget-setting name='showLabels'>true</b:widget-setting>
                        <b:widget-setting name='postLabelsLabel'>#</b:widget-setting>
                        <b:widget-setting name='showBacklinks'>false</b:widget-setting>
                        <b:widget-setting name='showInlineAds'>false</b:widget-setting>
                        <b:widget-setting name='showReactions'>false</b:widget-setting>
                      </b:widget-settings>
                      <b:includable id='main' var='this'>
                          
                        <b:include cond='data:view.isMultipleItems' name='titlePost'/>
                  
                        <div class='blogPts'>
                          <b:class cond='data:posts.empty' name='mty'/>
                  
                          <!--[ Fullpage condition ]-->
                          <b:class cond='data:view.url != data:view.url params { amp: &quot;1&quot; } and data:view.isSingleItem and data:posts any (p =&gt; p.labels any (l =&gt; l.name in [ &quot;Fullpage&quot; ]))' name='fullP'/>
                          <b:include cond='data:view.url != data:view.url params { amp: &quot;1&quot; } and data:view.isSingleItem and data:posts any (p =&gt; p.labels any (l =&gt; l.name in [ &quot;Fullpage&quot; ]))' name='post-singlePage'/>
                      
                          <!--[ If no content found ]-->
                          <b:include name='noContentPlaceholder'/>
                      
                          <b:with value='data:widgets.FeaturedPost filter (w =&gt; w.sectionId == &quot;top-widget&quot;) map (w =&gt; w.postId)' var='featuredPostIds'>
                            <b:with value='data:view.isHomepage ? data:posts filter (post =&gt; post.id not in data:featuredPostIds) : data:posts' var='posts'>
                            
                              <b:loop index='i' values='data:posts' var='post'>
                                <!--[ Remove comment tag below to enable in-feed ad ]-->
                                <!--<b:if cond='data:i == 3'>
                                  <b:include name='post-adIn'/>                                
                                </b:if>
                                <b:if cond='data:i == 6'>
                                  <b:include name='post-adIn'/>                                
                                </b:if>-->
                                <b:include data='post' name='postCommentsAndAd'/>
                              </b:loop>
                          
                            </b:with>
                          </b:with>
                        </div>
                  
                        <b:include cond='data:view.isMultipleItems and !data:posts.empty' name='postPagination'/>
                      </b:includable>
                      <b:includable id='aboutPostAuthor'/>
                      <b:includable id='addComments'/>
                      <b:includable id='blogThisShare'/>
                      <b:includable id='breadcrumb' var='post'>
                        <!--[ Post breadcrumbs ]-->
                        <div class='brdCmb' itemscope='itemscope' itemtype='https://schema.org/BreadcrumbList'>
                          <b:class cond='data:post.labels any (label =&gt; label.name in [ &quot;Sponsored&quot; ])' name='sponsored'/>
                          <div class='hm' itemprop='itemListElement' itemscope='itemscope' itemtype='https://schema.org/ListItem'>
                            <a expr:href='data:blog.homepageUrl.canonical' itemprop='item'><span itemprop='name'><data:messages.home/></span></a>
                            <meta content='1' itemprop='position'/>
                          </div>
                          <b:if cond='data:post.labels'>
                            <b:loop index='num' values='data:post.labels' var='label'>
                              <b:if cond='data:num == 0'>
                                <div class='lb' itemprop='itemListElement' itemscope='itemscope' itemtype='https://schema.org/ListItem'>
                                  <a expr:href='data:label.url.canonical' itemprop='item'><span itemprop='name'><data:label.name/></span></a>
                                  <meta expr:content='data:num+2' itemprop='position'/>
                                </div>
                              </b:if>
                              <b:if cond='data:num == 1 and data:post.labels none (label =&gt; label.name in [ &quot;Sponsored&quot; ])'>
                                <div class='lb' itemprop='itemListElement' itemscope='itemscope' itemtype='https://schema.org/ListItem'>
                                  <a expr:href='data:label.url.canonical' itemprop='item'><span itemprop='name'><data:label.name/></span></a>
                                  <meta expr:content='data:num+2' itemprop='position'/>
                                </div>
                              </b:if>
                            </b:loop>
                            <b:elseif cond='data:view.isPost'/>
                            <div class='lb nob'><data:messages.posts/></div>
                          </b:if>
                            
                          <!--[ Change cond='data:view.isPage' to cond='data:view.isSingleItem' if you want to show post title on breadcrumb ]-->
                          <b:tag class='tl' cond='data:view.isPage' expr:data-text='data:post.title' name='div'/>
                        </div>
                      </b:includable>
                      <b:includable id='bylineByName' var='byline'/>
                      <b:includable id='bylineRegion' var='regionIts'/>
                      <b:includable id='commentAuthorAvatar'/>
                      <b:includable id='commentDeleteIcon' var='comment'/>
                      <b:includable id='commentForm' var='post'/>
                      <b:includable id='commentFormIframeSrc' var='post'/>
                      <b:includable id='commentItem' var='comment'/>
                      <b:includable id='commentList' var='comments'/>
                      <b:includable id='commentPicker' var='post'/>
                      <b:includable id='commentblock' var='cb'>
                        <div class='cmAv'>
                          <b:if cond='data:cb.level.authorAvatarSrc'>
                            <div class='im' expr:data-style='&quot;background-image: url(&quot; + resizeImage(data:cb.level.authorAvatarSrc, 35, &quot;1:1&quot;) + &quot;)&quot;'>
                              <b:class cond='data:view.url != data:view.url params { amp: &quot;1&quot; }' name='lazy'/>
                              <b:attr cond='data:view.url == data:view.url params { amp: &quot;1&quot; }' expr:value='&quot;background-image: url(&quot; + resizeImage(data:cb.level.authorAvatarSrc, 35, &quot;1:1&quot;) + &quot;)&quot;' name='style'/>
                            </div>
                            <noscript><div class='im' expr:style='&quot;background-image: url(&quot; + resizeImage(data:cb.level.authorAvatarSrc, 35, &quot;1:1&quot;) + &quot;)&quot;'/></noscript>
                          </b:if>
                        </div>
                  
                        &lt;div class=&#39;cmIn&#39;&gt;
                        <div class='cmBd'>
                          <b:class cond='data:cb.level.isDeleted' name='del'/>
                          <b:attr cond='!data:cb.level.isDeleted' name='itemscope' value='itemscope'/>
                          <b:attr cond='!data:cb.level.isDeleted' name='itemtype' value='https://schema.org/Comment'/>
                          <div class='cmHr'>
                            <b:class cond='data:post.author.name == data:cb.level.author' name='a'/>
                            <span class='n'>
                              <b:attr cond='!data:cb.level.isDeleted' name='itemprop' value='author'/>
                              <b:attr cond='!data:cb.level.isDeleted' name='itemscope' value='itemscope'/>
                              <b:attr cond='!data:cb.level.isDeleted' name='itemtype' value='https://schema.org/Person'/>
                              <b:if cond='data:cb.level.author != &quot;Anonymous&quot;'>
                                <bdi><b:attr cond='!data:cb.level.isDeleted' name='itemprop' value='name'/><data:cb.level.author/></bdi>
                                <b:else/>
                                <bdi><b:attr cond='!data:cb.level.isDeleted' name='itemprop' value='name'/>Anonymous</bdi>
                              </b:if>
                            </span>
                    
                            <b:if cond='!data:cb.level.isDeleted'>
                              <!--[ Remove dtTm in className to disable Second Ago script ]-->
                              <b:if cond='data:view.url != data:view.url params { amp: &quot;1&quot; } and data:blog.languageDirection != &quot;rtl&quot;'>
                                <span class='d dtTm' expr:data-datetime='data:cb.level.timestamp'/>
                              </b:if>
                              <span class='d date' expr:data-datetime='data:cb.level.timestamp' itemprop='datePublished'><data:cb.level.timestamp/></span>
                            </b:if>
                          </div>

                          <div class='cmCo'>
                            <b:class cond='!data:post.allowNewComments' name='dis'/>
                            <b:attr cond='!data:cb.level.isDeleted' name='itemprop' value='text'/>
                            <b:if cond='data:cb.level.author != data:post.author.name'>
                              <b:eval expr='data:cb.level.body snippet { links: false }'/>
                              <b:else/>
                              <data:cb.level.body/>
                            </b:if>
                          </div>
                    
                        </div>
                      </b:includable>
                      <b:includable id='comments' var='post'/>
                      <b:includable id='commentsLink'/>
                      <b:includable id='commentsLinkIframe'/>
                      <b:includable id='commentsTitle'>
                        <h3 class='title'>
                          <b:if cond='data:post.numberOfComments &gt; 0'>
                            <b:message name='messages.numberOfComments'>
                              <b:param expr:value='data:post.numberOfComments' name='numComments'/>
                            </b:message>
                            <b:else/>
                            <data:messages.postAComment/>
                          </b:if>
                        </h3>
                      </b:includable>
                      <b:includable id='defaultAdUnit'>
                        <ins class='adsbygoogle' data-ad-format='auto' expr:data-ad-client='data:adClientId ?: data:blog.adsenseClientId' expr:data-ad-host='data:blog.adsenseHostId' expr:data-analytics-uacct='data:blog.analyticsAccountNumber' expr:style='data:style ?: &quot;display: block;&quot;'/>
                        <script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
                      </b:includable>
                      <b:includable id='emailPostIcon'/>
                      <b:includable id='facebookShare'/>
                      <b:includable id='feedLinks'/>
                      <b:includable id='feedLinksBody' var='links'/>
                      <b:includable id='footerBylines'/>
                      <b:includable id='googlePlusShare'/>
                      <b:includable id='headerByline'/>
                      <b:includable id='homePageLink'/>
                      <b:includable id='iframeComments' var='post'/>
                      <b:includable id='inlineAd' var='post'>
                        <b:if cond='!data:view.isPreview'>
                          <b:if cond='data:this.adCode or data:this.adClientId or data:blog.adsenseClientId'>
                            <!-- Ad -->
                            <div class='inline-ad'>
                              <b:if cond='data:this.adCode != &quot;&quot;'>
                                <data:this.adCode/>
                                <b:else/>
                                <b:include cond='data:this.adClientId or data:blog.adsenseClientId' name='defaultAdUnit'/>
                              </b:if>
                            </div>
                          </b:if>
                          <b:else/>
                          <div class='inline-ad'>
                            <div class='inline-ad-placeholder'>
                              <span><b:message name='messages.adsGoHere'/></span>
                            </div>
                          </div>
                        </b:if>
                      </b:includable>
                      <b:includable id='linkShare'/>
                      <b:includable id='manageComments'/>
                      <b:includable id='nextPageLink'/>
                      <b:includable id='noContentPlaceholder'>
                        <b:if cond='data:posts.empty'>
                          <!--[ No posts messages ]-->
                          <div class='noPosts'><data:messages.noResultsFound/>...</div>
                        </b:if>
                      </b:includable>
                      <b:includable id='otherSharingButton'/>
                      <b:includable id='platformShare'/>
                      <b:includable id='post' var='post'/>
                      <b:includable id='postAuthor'/>
                      <b:includable id='postBody' var='post'/>
                      <b:includable id='postBodySnippet' var='post'/>
                      <b:includable id='postCommentsAndAd' var='post'>
                    
                        <!--[ Post article ]-->
                        <article class='ntry'>
                          <b:class cond='data:view.isSingleItem' name='ps'/>
                          <b:class cond='data:view.isSingleItem' name='post'/>
                          <b:class cond='data:view.isMultipleItems and !data:post.featuredImage' name='noThmb'/>
                          <b:class cond='!data:widgets.Blog.first.allBylineItems.timestamp' name='noInf'/>
                          <b:class cond='data:post.labels any (label =&gt; label.name in [ &quot;Sponsored&quot; ])' name='noAd'/>
                    
                          <!--[ Post brdCmb ]-->
                          <b:include cond='data:view.isSingleItem' data='post' name='breadcrumb'/>
                        
                          <b:if cond='data:view.isMultipleItems'>
                            <!--[ Post thumbnail and labels ]-->
                            <div class='pThmb'>
                              <b:class cond='data:post.featuredImage.isYoutube' name='iyt'/>
                              <b:class cond='!data:post.featuredImage' name='nul'/>
                              <b:tag class='thmb' expr:name='data:post.featuredImage ? &quot;a&quot; : &quot;div&quot;'>
                                <b:attr cond='data:post.featuredImage' expr:value='data:post.url' name='href'/>
                                <b:if cond='data:post.featuredImage'>
                                  <b:include name='postEntryThumbnail'/>
                                  <b:else/>
                                  <span class='imgThm' data-text='No image'/>
                                </b:if>
                              </b:tag>
                                
                              <!--[ Comments count ]-->
                              <b:tag class='iFxd' cond='data:post.allowComments and data:post.numberOfComments &gt; 0 or data:post.labels any (label =&gt; label.name in [ &quot;Sponsored&quot; ])' name='div'>
                                <b:if cond='data:post.labels any (label =&gt; label.name in [ &quot;Sponsored&quot; ])'>
                                  <b:include name='postSponsored'/>
                                </b:if>
                                <b:if cond='data:widgets.Blog.first.allBylineItems.comments'>
                                  <b:include name='postCommentsLinks'/>
                                </b:if>
                              </b:tag>
                            </div>
                          </b:if>
                    
                          <b:tag class='pCntn' cond='data:view.isMultipleItems' name='div'>
                              
                            <!--[ Post header ]-->
                            <b:include cond='data:view.isMultipleItems' name='postHeaders'/>
                          
                            <!--[ Post title ]-->
                            <b:tag class='pTtl aTtl' expr:name='data:post.link or (data:post.url and data:view.url != data:post.url) ? &quot;h2&quot; : &quot;h1&quot;'>
                              <b:class cond='data:view.isSingleItem' name='itm'/>
                              <b:class cond='data:post.labels any (label =&gt; label.name in [ &quot;Sponsored&quot; ])' name='nSpr'/>
                              <b:tag expr:name='data:post.link or (data:post.url and data:view.url != data:post.url) ? &quot;a&quot; : &quot;span&quot;'>
                                <b:attr cond='data:post.link or (data:post.url and data:view.url != data:post.url)' expr:value='data:post.url.canonical' name='href'/>
                                <b:attr cond='data:post.link or (data:post.url and data:view.url != data:post.url)' expr:value='data:post.title' name='data-text'/>
                                <b:attr cond='data:post.link or (data:post.url and data:view.url != data:post.url)' name='rel' value='bookmark'/>
                                <data:post.title/>
                              </b:tag>
                            </b:tag>
                              
                            <b:if cond='data:blog.metaDescription and data:view.isPost'>
                              <!-- Post Description -->
                              <div class='pDesc'><data:blog.metaDescription/></div>
                            </b:if>
                          
                            <b:if cond='data:view.isMultipleItems'>
                              <!--[ Post snippets ]-->
                              <div class='pSnpt'>
                                <b:include name='postEntrySnippet'/>
                              </div>
                            </b:if>
                        
                            <!--[ Post info ]-->
                            <b:include cond='!data:view.isPage' name='postInfo'/>
                          
                            <!--[ Share button ]-->
                            <b:include cond='data:post.shareUrl and data:view.isPost and !data:view.isPreview' name='postInfoShare'/>
                          
                            <!--[ Change post font size ]-->
                            <b:include cond='data:view.isPost and !data:view.isPreview' name='postFontInput'/>
                            <b:include cond='data:view.isPost and !data:view.isPreview' name='postFontEntry'/>
                        
                            <b:tag class='pInr' cond='data:view.isSingleItem' name='div'>
                              <b:if cond='data:post.labels none (label =&gt; label.name in [ &quot;Sponsored&quot; ])'>
                                <!--[ Post top ad ]-->
                                <b:include cond='data:view.isPost and !data:view.isPreview' data='post' name='post-adTop'/>
                              </b:if>
                          
                              <b:if cond='data:view.isSingleItem'>
                                <!--[ Post body ]-->
                                <div class='pEnt' expr:id='&quot;postID-&quot; + data:post.id'>
                                  <div class='pS post-body postBody' id='postBody'><data:post.body/><script>
var viewBlogId = <data:blog.blogId/>;
var viewPostId = <data:post.id/>; 
</script></div>
               
                                  <!-- letakkan kode ini harus di bawah kode <data:post.body/> -->
<div class='postTextRelated' id='postTextRelated'>
<script>/*<![CDATA[*/ var relatedTitles=new Array,relatedTitlesNum=0,relatedUrls=new Array;function related_results_labels(e){for(var t=0;t<e.feed.entry.length;t++){var l=e.feed.entry[t];relatedTitles[relatedTitlesNum]=l.title.$t;for(var r=0;r<l.link.length;r++)if("alternate"==l.link[r].rel){relatedUrls[relatedTitlesNum]=l.link[r].href,relatedTitlesNum++;break}}}function removeRelatedDuplicates(){for(var e=new Array(0),t=new Array(0),l=0;l<relatedUrls.length;l++)contains(e,relatedUrls[l])||(e.length+=1,e[e.length-1]=relatedUrls[l],t.length+=1,t[t.length-1]=relatedTitles[l]);relatedTitles=t,relatedUrls=e}function contains(e,t){for(var l=0;l<e.length;l++)if(e[l]==t)return!0;return!1}function printRelatedLabels(){for(var e=Math.floor((relatedTitles.length-1)*Math.random()),t=0;t<relatedTitles.length&&t<20;){var l=document.createElement("ul"),r=document.createElement("li"),a=document.createElement("a");a.setAttribute("href",relatedUrls[e]),a.setAttribute("target","_blank"),a.innerText=relatedTitles[e],l.appendChild(r),r.appendChild(a),document.querySelector(".postTextRelated").appendChild(l),e<relatedTitles.length-1?e++:e=0,t++}} /*]]>*/</script>
<b:if cond='data:post.labels'>
<b:loop index='i' values='data:post.labels' var='label'>
<b:if cond='data:i&lt;1'>
<script expr:src='&quot;/feeds/posts/default/-/&quot; + data:label.name + &quot;?alt=json-in-script&amp;callback=related_results_labels&amp;max-results=3&quot;' rel='preload'/>
</b:if>
</b:loop>
</b:if>
<b>Baca juga :</b>
<script>removeRelatedDuplicates(); printRelatedLabels();</script>
</div>
<script>/*<![CDATA[*/
// (postBody) sesuaikan dengan kode di template kalian, biasanya dapat di lihat pebungkus kode ini <data:post.body/> contoh <div class='postBody'><data:post.body/></div>
!function() {
    let c = document.querySelector("#postTextRelated");
    if (c) {
        let a = document.querySelectorAll(".postBody p"),
            b = parseInt(a.length / 2);
        if (a.length > 0) {
        c.style.display = 'block';
        "P" == a[b].nodeName ? a[b].parentNode.insertBefore(c, a[b]) : a[b].parentNode.insertBefore(c, a[b].nextSibling)
    }
}
}()
/*]]>*/</script>
                                  
                                </div>
                              </b:if>
                              
                              <b:if cond='data:post.labels none (label =&gt; label.name in [ &quot;Sponsored&quot; ])'>
                                <!--[ Post bottom ad ]-->
                                <b:include cond='data:view.isPost and !data:view.isPreview' data='post' name='post-adBot'/>
                              </b:if>
                      
                              <b:include data='post' name='postMetadataJSON'/>
                              
                              <b:if cond='data:view.url != data:view.url params { amp: &quot;1&quot; } and data:view.isPost and data:widgets.Blog.first.allBylineItems.timestamp'>
                                <script>/*<![CDATA[*/ function get_text(el) {ret = ''; var length = el.childNodes.length; for(var i = 0; i < length; i++) {var node = el.childNodes[i]; if(node.nodeType != 8) {ret += node.nodeType != 1 ? node.nodeValue : get_text(node);} } return ret;} var words = get_text(document.getElementById('postBody')); var count = words.split(' ').length; var avg = 200; var counted = count / avg; var maincount = Math.round(counted); document.getElementById('rdTime').innerHTML = maincount + ' menit membaca'; /*]]>*/</script>
                              </b:if>
                        
                              <b:if cond='data:post.labels none (label =&gt; label.name in [ &quot;Sponsored&quot; ])'>
                                <!--[ Post writter ]-->
                                <b:include cond='data:post.author.aboutMe and data:view.isPost and !data:view.isPreview' name='post-authorProfile'/>
                              </b:if>
                            </b:tag>
                          
                          </b:tag>
                        </article>
                  
                        <!--[ Post footer ]-->
                        <b:tag class='pFoot' cond='data:view.isPost' name='div'>
                          <!--[ Share button pop-up/sticky ]-->
                          <b:include cond='data:post.shareUrl and data:view.isPost and !data:view.isPreview' name='postInfoShareMore'/>
                            
                          <!--[ Related post ]-->
                          <b:include cond='data:view.url != data:view.url params { amp: &quot;1&quot; } and data:view.isPost and !data:view.isPreview' data='post' name='post-related'/>
                    
                          <!--[ Matched content ad ]-->
                          <!--<b:include cond='data:view.isPost and !data:view.isPreview' data='post' name='post-relatedAd'/>-->
                    
                          <b:tag class='pCmnts' cond='data:post.allowComments and data:view.isPost and !data:view.isPreview' id='comment' name='div'>
                            <!--[ Blogger Comments ]-->
                            <b:include cond='data:post.allowComments and data:view.isPost and !data:view.isPreview' data='post' name='threadedComments-modifV3'/>
                          </b:tag>
                          
                          <b:if cond='data:view.isPost and !data:view.isPreview and data:blog.isMobileRequest'>
                            <b:include cond='(data:post.allowComments and data:widgets.Blog.first.allBylineItems.comments) or (data:post.shareUrl and data:widgets.Blog.first.allBylineItems.share)' name='post-bottomMenu'/>
                          </b:if>
                        </b:tag>
                        
                        <!--[ Show ad. ]-->
                        <b:include cond='data:post.includeAd' data='post' name='inlineAd'/>
                      </b:includable>
                      <b:includable id='postCommentsLink'/>
                      <b:includable id='postFooter' var='post'/>
                      <b:includable id='postFooterAuthorProfile' var='post'/>
                      <b:includable id='postHeader'/>
                      <b:includable id='postInfo'>
                        <b:tag class='pInf pSml' name='div'>
                          <b:class cond='data:view.isSingleItem' name='ps'/>
                          <b:class cond='data:post.labels any (label =&gt; label.name in [ &quot;Sponsored&quot; ])' name='nSpr'/>
                          <b:class cond='!data:widgets.Blog.first.allBylineItems.timestamp' name='nTm'/>
                          <b:class cond='!data:widgets.Blog.first.allBylineItems.author and !data:widgets.Blog.first.allBylineItems.timestamp and (!data:post.shareUrl and !data:widgets.Blog.first.allBylineItems.share) and (!data:post.allowComments and !data:widgets.Blog.first.allBylineItems.comments or data:post.numberOfComments == 0)' name='nul'/>
                        
                          <b:if cond='data:view.isMultipleItems'>
                            <b:if cond='data:post.labels none (label =&gt; label.name in [ &quot;Sponsored&quot; ])'>
                              <!--[ Post timestamp ]-->
                              <b:include cond='data:widgets.Blog.first.allBylineItems.timestamp' name='postTimestampPublish'/>
                            </b:if>
                      
                            <!--[ Post jumplinks ]-->
                            <b:include cond='data:widgets.Blog.first.allBylineItems.timestamp' name='postJumpLinks'/>                    
                        
                            <b:else/>
                      
                            <!--[ Info in item page ]-->
                            <b:if cond='data:widgets.Blog.first.allBylineItems.author and data:post.labels none (label =&gt; label.name in [ &quot;Sponsored&quot; ])'>
                              <b:if cond='data:post.author.authorPhoto.image'>
                                <div class='pIm'><b:include name='post-authorImage'/></div>
                              </b:if>
                            </b:if>
                              
                            <b:tag class='pNm' cond='data:widgets.Blog.first.allBylineItems.author or data:widgets.Blog.first.allBylineItems.timestamp' name='div'>
                              <b:class cond='!data:widgets.Blog.first.allBylineItems.timestamp and data:post.labels any (label =&gt; label.name in [ &quot;Sponsored&quot; ])' name='l'/>
                              <b:class cond='!data:post.author.authorPhoto.image' name='n'/>
                              <b:include cond='data:widgets.Blog.first.allBylineItems.author and data:post.labels none (label =&gt; label.name in [ &quot;Sponsored&quot; ])' name='post-authorName'/>
                                
                              <b:if cond='data:widgets.Blog.first.allBylineItems.timestamp'>
                                <div class='pDr'>
                                  <bdi class='pDt pIn'><b:include name='update2-icon'/><b:include name='postTimestamps'/></bdi>
                                
                                  <b:if cond='data:view.url != data:view.url params { amp: &quot;1&quot; }'>
                                    <!--[ Reading time ]-->
                                    <div class='pRd pIn'><bdi id='rdTime'/></div>
                                  </b:if>
                                </div>
                              </b:if>
                            </b:tag>
                              
                            <b:if cond='(data:post.allowComments and data:widgets.Blog.first.allBylineItems.comments and data:post.numberOfComments &gt; 0) or (data:post.shareUrl and data:widgets.Blog.first.allBylineItems.share)'>
                              <div class='pCm'>
                                <b:class cond='(data:post.allowComments and data:widgets.Blog.first.allBylineItems.comments and data:post.numberOfComments &gt; 0) and (data:post.shareUrl and data:widgets.Blog.first.allBylineItems.share)' name='l'/>
                                <div class='pIc'>
                                  
                                  
                                  
                                  <b:include cond='data:post.allowComments and data:widgets.Blog.first.allBylineItems.comments' name='postCommentsLabela'/>
                                  <label class='fn tIc' for='forFont'><b:include name='font-icon'/></label>
                                </div>
                              </div>
                            </b:if>
                          
                          </b:if>
                        </b:tag>
                      </b:includable>
                      <b:includable id='postInfoShare'>
                        <div class='pSh'>
                          <b:class cond='data:post.labels any (label =&gt; label.name in [ &quot;Sponsored&quot; ])' name='nSpr'/>
                          <div class='pShc' expr:data-text='data:messages.share + &quot;:&quot;'>
                            <!-- Share to Facebook -->
                            <a aria-label='Facebook' class='c fb' data-text='Share' expr:href='&quot;https://www.facebook.com/sharer.php?u=&quot; + data:blog.url.canonical' rel='noopener' role='button' target='_blank'><b:include name='facebook-r-icon'/></a>
                            
                            <!-- Share to Whatsapp -->
                            <a aria-label='Whatsapp' class='c wa' data-text='Share' expr:href='&quot;https://api.whatsapp.com/send?text=&quot; + data:blog.url.canonical' rel='noopener' role='button' target='_blank'><b:include name='whatsapp-r-icon'/></a>
                                
                            <!-- Share to Twitter -->
                            <a aria-label='Twitter' class='c tw' data-text='Tweet' expr:href='&quot;https://twitter.com/share?url=&quot; + data:blog.url.canonical' rel='noopener' role='button' target='_blank'><b:include name='twitter-r-icon'/></a>
                            
                            <label expr:aria-label='data:messages.shareToOtherApps' for='forShare'><b:include name='plus-icon'/></label>
                          </div>
                        </div>
                      </b:includable>
                      <b:includable id='postInfoShareMore'>
                        <input class='shIn fixi hidden' id='forShare' type='checkbox'/>
                        <div class='shBr fixL'>
                          <div class='shBri fixLi'>
                            <div class='shBrs fixLs'>
                              <div class='shH fixH fixT' expr:data-text='data:messages.shareToOtherApps'>
                                <label aria-label='Close' class='c cl' for='forShare'/>
                              </div>
                              <div class='shC'>
                                <!--[ Share to other apps ]-->
                                <div class='shL'>
                                  <div data-text='Facebook'>
                                    <!-- Share to Facebook -->
                                    <a aria-label='Facebook' expr:href='&quot;https://www.facebook.com/sharer.php?u=&quot; + data:blog.url.canonical' rel='noopener' target='_blank'>
                                      <b:include name='facebook-r-icon'/>
                                    </a>
                                  </div>
                                    
                                  <div data-text='WhatsApp'>
                                    <!-- Share to Whatsapp -->
                                    <a aria-label='Whatsapp' expr:href='&quot;https://api.whatsapp.com/send?text=&quot; + data:blog.url.canonical' rel='noopener' target='_blank'>
                                      <b:include name='whatsapp-r-icon'/>
                                    </a>
                                  </div>
                                    
                                  <div data-text='Twitter'>
                                    <!-- Share to Twitter -->
                                    <a aria-label='Twitter' expr:href='&quot;https://twitter.com/share?url=&quot; + data:blog.url.canonical' rel='noopener' target='_blank'>
                                      <b:include name='twitter-r-icon'/>
                                    </a>
                                  </div>
                                    
                                  <div data-text='Telegram'>
                                    <!-- Share to Telegram -->
                                    <a aria-label='Telegram' expr:href='&quot;https://t.me/share/url?url=&quot; + data:blog.url.canonical' rel='noopener' target='_blank'>
                                      <b:include name='telegram-r-icon'/>
                                    </a>
                                  </div>
                                    
                                  <div data-text='Pinterest'>
                                    <!-- Pin to Pinterst -->
                                    <a aria-label='Pinterest' data-pin-config='beside' expr:href='&quot;https://pinterest.com/pin/create/button/?url=&quot; + data:blog.url.canonical + &quot;&amp;media=&quot; + resizeImage(data:blog.postImageUrl, 1600)' rel='noopener' target='_blank'>
                                      <b:include name='pinterest-r-icon'/>
                                    </a>
                                  </div>
                                    
                                  <div data-text='LinkedIn'>
                                    <!-- Share Linkedin -->
                                    <a aria-label='Linkedin' expr:href='&quot;https://www.linkedin.com/sharing/share-offsite/?url=&quot; + data:blog.url.canonical' rel='noopener' target='_blank'>
                                      <b:include name='linkedIn-r-icon'/>
                                    </a>
                                  </div>
                                    
                                  <div data-text='Line'>
                                    <!-- Share to Line -->
                                    <a aria-label='Line' expr:href='&quot;https://timeline.line.me/social-plugin/share?url=&quot; + data:blog.url.canonical' rel='noopener' target='_blank'>
                                      <b:include name='line-r-icon'/>
                                    </a>
                                  </div>
                                    
                                  <div data-text='Email'>
                                    <!-- Send to email -->
                                    <a aria-label='Email' expr:href='&quot;mailto:?body=&quot; + data:blog.url.canonical' target='_blank'>
                                      <b:include name='mail-r-icon'/>
                                    </a>
                                  </div>
                                </div>
                                  
                                <b:if cond='data:view.url != data:view.url params { amp: &quot;1&quot; }'>
                                  <!--[ Copy link ]-->
                                  <div class='cpL' data-text='or copy link' expr:data-message='data:messages.copyToClipboard'>
                                    <div class='cpLb'>
                                      <b:include name='link-alt-icon'/>
                                      <input expr:value='data:blog.url.canonical' id='getlink' onClick='this.select()' readonly='readonly'/>
                                      <label for='getlink' onclick='copyFunction()'><data:messages.copy/></label>
                                    </div>
                                  
                                    <div class='cpLn' id='cpNotif'/>
                                  
                                    <script>function copyFunction(){document.getElementById(&#39;getlink&#39;).select(),document.execCommand(&#39;copy&#39;),document.getElementById(&#39;cpNotif&#39;).innerHTML=&#39;<span><data:messages.linkCopiedToClipboard/></span>&#39; };</script>
                                  </div>
                                </b:if>
                              </div>
                            </div>
                          </div>
                            
                          <label class='fCls' for='forShare'/>
                        </div>
                      </b:includable>
                      <b:includable id='postJumpLink' var='post'/>
                      <b:includable id='postLabels'/>
                      <b:includable id='postLocation'/>
                      <b:includable id='postMeta' var='post'>
                        <b:include data='post' name='postMetadataJSON'/>
                      </b:includable>
                      <b:includable id='postMetadataJSON'>
                        <script type='application/ld+json'>
                          {
                            &quot;@context&quot;: &quot;http://schema.org&quot;,
                            &quot;@type&quot;: &quot;BlogPosting&quot;,
                            &quot;mainEntityOfPage&quot;: {
                              &quot;@type&quot;: &quot;WebPage&quot;,
                              &quot;@id&quot;: &quot;<data:post.url.canonical.jsonEscaped/>&quot;
                            },
                            &quot;headline&quot;: &quot;<data:post.title.jsonEscaped/>&quot;,
                            &quot;description&quot;: &quot;<b:eval expr='snippet(data:post.snippets.long, {length: 250, links: false, linebreaks: false, ellipsis: true }).jsonEscaped'/>&quot;,
                            <b:if cond='data:view.isSingleItem'>&quot;articleBody&quot;: &quot;<b:eval expr='snippet(data:post.body, {links: false, linebreaks: false, ellipsis: true}).jsonEscaped'/>&quot;,</b:if>
                            &quot;datePublished&quot;: &quot;<data:post.date.iso8601.jsonEscaped/>&quot;,
                            &quot;dateModified&quot;: &quot;<data:post.lastUpdated.iso8601.jsonEscaped/>&quot;,
                            <b:include data='post' name='postMetadataJSONImage'/><b:include data='post' name='postMetadataJSONPublisher'/>
                            &quot;author&quot;: {
                              &quot;@type&quot;: &quot;Person&quot;,
                              &quot;name&quot;: &quot;<data:post.author.name.jsonEscaped/>&quot;,
                              &quot;url&quot;: &quot;<b:if cond='data:post.author.profileUrl'><data:post.author.profileUrl.jsonEscaped/><b:else/><data:blog.homepageUrl.jsonEscaped/></b:if>&quot;,
                              &quot;image&quot;: &quot;<data:post.author.authorPhoto.image.jsonEscaped/>&quot;
                            }
                          }
                        </script>
                      </b:includable>
                      <b:includable id='postMetadataJSONImage'>
                            &quot;image&quot;: {
                              &quot;@type&quot;: &quot;ImageObject&quot;,
                              &quot;url&quot;: &quot;<b:eval expr='(data:post.featuredImage ? resizeImage(data:post.featuredImage, 1200, &quot;1200:630&quot;) : &quot;https://1.bp.blogspot.com/-E250bQMM8tk/XomH5DdorOI/AAAAAAAAPY8/SCYwi79WjckWC8wHKK7OblI82BpT9JquACNcBGAsYHQ/s1600/jagotheme-img.png&quot;).jsonEscaped'/>&quot;,
                              &quot;height&quot;: <b:eval expr='data:post.featuredImage ? 630 : 348'/>,
                              &quot;width&quot;: 1200
                            },
                      </b:includable>
                      <b:includable id='postMetadataJSONPublisher'>
                            &quot;publisher&quot;: {
                              &quot;@type&quot;: &quot;Organization&quot;,
                              &quot;name&quot;: &quot;<data:blog.title.escaped/>&quot;,
                              &quot;logo&quot;: {
                                &quot;@type&quot;: &quot;ImageObject&quot;,
                                &quot;url&quot;: &quot;#&quot;,
                                &quot;width&quot;: 297,
                                &quot;height&quot;: 45
                              }
                            },
                      </b:includable>
                      <b:includable id='postPagination'>
                        <!--[ Blog navigation ]-->
                        <div class='blogPg' id='blogPager'>
                          <b:tag class='nPst' cond='data:view.url == data:blog.homepageUrl and !data:olderPageUrl' expr:data-text='data:messages.noResultsFound' name='div'/>
                      
                          <b:include cond='!data:posts.empty' name='postPagination.new'/>
                          <b:include cond='!data:posts.empty' name='postPagination.home'/>
                          <b:include cond='!data:posts.empty' name='postPagination.old'/>
                        </div>
                      </b:includable>
                      <b:includable id='postPagination.home'>
                        <b:tag class='hmLnk' expr:name='data:view.url != data:blog.homepageUrl ? &quot;a&quot; : &quot;div&quot;'>
                          <b:class cond='data:view.url == data:blog.homepageUrl' name='nPst'/>
                          <b:attr cond='data:view.url != data:blog.homepageUrl' expr:value='data:blog.homepageUrl.canonical' name='href'/>
                          <b:attr cond='data:view.url != data:blog.homepageUrl' expr:value='data:messages.home' name='aria-label'/>
                          <b:attr cond='data:posts.empty' expr:value='data:messages.home' name='data-text'/>
                          <b:include cond='!data:posts.empty' name='home-alt-icon'/>
                        </b:tag>                      
                      </b:includable>
                      <b:includable id='postPagination.new'>
                        <b:if cond='data:newerPageUrl and data:view.url != data:blog.homepageUrl.canonical path &quot;search&quot;'>
                          <a class='nwLnk' expr:aria-label='data:messages.newest' expr:data-text='data:messages.newest' expr:href='data:newerPageUrl.canonical'>
                            <b:if cond='data:blog.languageDirection != &quot;rtl&quot;'>
                              <b:include name='arrow-left-icon'/>
                              <b:else/>
                              <b:include name='arrow-right-icon'/>
                            </b:if>
                          </a>
                          <b:else/>
                          <div class='nwLnk nPst' expr:data-text='data:messages.newest'>
                            <b:if cond='data:blog.languageDirection != &quot;rtl&quot;'>
                              <b:include name='arrow-left-icon'/>
                              <b:else/>
                              <b:include name='arrow-right-icon'/>
                            </b:if>
                          </div>
                        </b:if>
                      </b:includable>
                      <b:includable id='postPagination.old'>
                        <b:tag class='olLnk' expr:data-text='data:messages.oldest' expr:name='data:olderPageUrl ? &quot;a&quot; : &quot;div&quot;'>
                          <b:class cond='!data:olderPageUrl' name='nPst'/>
                          <b:attr cond='data:olderPageUrl' expr:value='data:olderPageUrl.canonical' name='href'/>
                          <b:attr cond='data:olderPageUrl' expr:value='data:messages.oldest' name='aria-label'/>
                          <b:if cond='data:blog.languageDirection != &quot;rtl&quot;'>
                            <b:include name='arrow-right-icon'/>
                            <b:else/>
                            <b:include name='arrow-left-icon'/>
                          </b:if>
                        </b:tag>
                      </b:includable>
                      <b:includable id='postReactions'/>
                      <b:includable id='postShareButtons'/>
                      <b:includable id='postTimestamp'/>
                      <b:includable id='postTitle' var='post'/>
                      <b:includable id='previousPageLink'/>
                      <b:includable id='sharingButton'/>
                      <b:includable id='sharingButtonContent'/>
                      <b:includable id='sharingButtons'/>
                      <b:includable id='sharingButtonsMenu'/>
                      <b:includable id='sharingPlatformIcon'/>
                      <b:includable id='threadedCommentForm' var='post'/>
                      <b:includable id='threadedCommentJs' var='post'/>
                      <b:includable id='threadedComments' var='post'/>
                      <b:includable id='threadedComments-form' var='post'>
                        <div id='commentForm'>
                          <!--[ Comment message ]-->
                          <b:if cond='data:this.messages.blogComment != &quot;&quot;'>
                            <div class='cmMs note'>
                              <data:this.messages.blogComment/>
                            </div>
                          </b:if>
                            
                          <!--[ Comment iframe (remove comment tag below to improve height of comment form) ]-->
                          <!--<a aria-label='Comment Form' expr:href='data:post.commentFormIframeSrc + &quot;&amp;skin=contempo&quot; + data:variantParam' id='comment-editor-src'/>-->
                          <b:if cond='data:view.url != data:view.url params { amp: &quot;1&quot; }'>
                            <iframe class='blogger-iframe-colorize blogger-comment-from-post lazy' expr:data-src='data:post.commentFormIframeSrc appendParams {skin: &quot;contempo&quot;}' height='296' id='comment-editor' name='comment-editor' title='Blogger comment' width='100'/>
                            <b:else/>
                            <amp-iframe class='blogger-iframe-colorize blogger-comment-from-post' expr:data-src='data:post.commentFormIframeSrc appendParams {skin: &quot;contempo&quot;}' expr:src='data:post.commentFormIframeSrc appendParams {skin: &quot;contempo&quot;}' height='296' id='comment-editor' layout='fixed-height' sandbox='allow-scripts allow-same-origin allow-forms allow-top-navigation'/>
                          </b:if>
                         
                          <b:if cond='data:view.url != data:view.url params { amp: &quot;1&quot; }'>
                            <!--<script src='https://www.blogger.com/static/v1/jsbin/1875144490-comment_from_post_iframe.js'/>
                            <script>BLOG_CMT_createIframe(&#39;<data:post.appRpcRelayPath/>&#39;);</script>-->
                          </b:if>
                        </div>
                      </b:includable>
                      <b:includable id='threadedComments-modifV3' var='post'>
                        <b:tag class='cmSh fixi hidden' id='forComments' name='input' type='checkbox'/>
                        <b:tag checked='checked' class='cmAl hidden' cond='data:post.numberOfComments &gt; 0' id='forAllCm' name='input' type='checkbox'/>
                          
                        <!--[ Delete tag below to disable show/hide comment ]-->
                        <b:include cond='data:post.allowComments' name='post-commentButton'/>
                    
                        <section class='cm' expr:data-embed='data:post.embedCommentForm' expr:data-num-comments='data:post.numberOfComments' id='comments'>
                            
                          <!--[ Delete tag below to disable Pop-up comments ]-->
                          <b:class name='cmBr fixL'/>
                            
                          <b:tag class='cmBri' name='div'>
                            <b:class cond='data:post.numberOfComments == 0' name='mty'/>
                            <b:tag class='cmBrs fixLs' name='div'>
                    
                              <!--[ Comments title ]-->
                              <div class='cmH fixH'>
                                <b:include name='commentsTitle'/>
                        
                                <div class='cmI cl'>
                                  <!-- Sort comments -->
                                  <b:if cond='data:post.numberOfComments &gt; 0'>
                                    <label class='s' expr:aria-label='data:messages.manageComments' expr:data-new='data:messages.newest' expr:data-text='data:messages.oldest' for='forAllCm'/>
                                  </b:if>
                                  
                                  <label aria-label='Close' class='c' for='forComments'/>
                                </div>
                              </div>
                      
                              <div class='cmC'>
                                <b:if cond='data:post.numberOfComments &gt; 0'>
                                  <div class='cmCn'>
                          
                                    <ol class='cmHl' id='cmHolder'>
                                      <b:loop values='data:post.comments where (c =&gt; not c.inReplyTo)' var='commentLevel1'>
                                        <li class='c' expr:id='&quot;c&quot; + data:commentLevel1.id'>
                                          <b:class cond='data:cb.level.author == data:post.author.name' name='adm'/>
                                          <b:include data='{level: data:commentLevel1,d: true}' name='commentblock'/>
                              
                                          <b:with value='data:post.comments where (c =&gt; c.inReplyTo == data:commentLevel1.id)' var='commentL2'>
                                            <b:if cond='data:commentL2.size != &quot;0&quot;'>
                                              <input class='cmRi hidden' expr:id='&quot;to-&quot; + data:commentLevel1.id' type='checkbox'/>
                                                
                                              <div class='cmRp'>
                                                <div class='cmTh' expr:id='&quot;c&quot; + data:commentLevel1.id + &quot;-rt&quot;'>
                                                  <label class='thTg' data-text='Hide replies' expr:aria-label='&quot;View &quot; +data:commentL2.length+ &quot; replies&quot;' expr:for='&quot;to-&quot; + data:commentLevel1.id'/>
                                    
                                                  <ol class='thCh'>
                                                    <b:loop values='data:commentL2' var='commentLevel2'>
                                                      <li class='c' expr:id='&quot;c&quot; + data:commentLevel2.id'>
                                                        <b:class cond='data:cb.level.author == data:post.author.name' name='adm'/>
                                                        <b:include data='{level: data:commentLevel2,d: true}' name='commentblock'/>
                                                        &lt;/div&gt;
                                                      </li>
                                                    </b:loop>
                                                  </ol>
                                    
                                                </div>
                                                <b:if cond='data:post.allowNewComments and data:view.url != data:view.url params { amp: &quot;1&quot; }'>
                                                  <div class='cmAc cmR'>
                                                    <a aria-label='Reply' class='rpTo' data-text='Reply' expr:data-reply-to='data:commentLevel1.id' href='javascript:;' target='_self'/>
                                                  </div>
                                                </b:if>
                                              </div>
                                            </b:if>
                                          </b:with>
                              
                                          <b:if cond='data:post.allowNewComments and data:view.url != data:view.url params { amp: &quot;1&quot; }'>
                                            <div class='cmAc'>
                                              <a aria-label='Reply' class='rpTo' data-text='Reply' expr:data-reply-to='data:commentLevel1.id' href='javascript:;' target='_self'/>
                                            </div>
                                          </b:if>
                                          &lt;/div&gt;
                                        </li>
                                      </b:loop>
                                    </ol>
                                
                                    <!--[ Timeago script ]-->
                                    <b:if cond='data:blog.languageDirection != &quot;rtl&quot; and data:view.url != data:view.url params { amp: &quot;1&quot; }'>
                                      <script>/*<![CDATA[*/ (function timeAgo(selector) { var templates = {prefix: "", suffix: "", seconds: "second ago", minute: "1 min", minutes: "%d min", hour: "1 hour", hours: "%d hour", day: "1 day", days: "%d days", month: "1 month", months: "%d month", year: "1 year", years: "%d years"}; var template = function(t, n) { return templates[t] && templates[t].replace(/%d/i, Math.abs(Math.round(n))); }; var timer = function(time) { if (!time) return; time = time.replace(/\.\d+/, ""); time = time.replace(/-/, "/").replace(/-/, "/"); time = time.replace(/T/, " ").replace(/Z/, " UTC"); time = time.replace(/([\+\-]\d\d)\:?(\d\d)/, " $1$2"); time = new Date(time * 1000 || time); var now = new Date(); var seconds = ((now.getTime() - time) * .001) >> 0; var minutes = seconds / 60; var hours = minutes / 60; var days = hours / 24; var years = days / 365; return templates.prefix + ( seconds < 45 && template('seconds', seconds) || seconds < 90 && template('minute', 1) || minutes < 45 && template('minutes', minutes) || minutes < 90 && template('hour', 1) || hours < 24 && template('hours', hours) || hours < 42 && template('day', 1) || days < 30 && template('days', days) || days < 45 && template('month', 1) || days < 365 && template('months', days / 30) || years < 1.5 && template('year', 1) || template('years', years) ) + templates.suffix; }; var elements = document.getElementsByClassName('dtTm'); for (var i in elements) { var $this = elements[i]; if (typeof $this === 'object') { $this.innerHTML = timer($this.getAttribute('title') || $this.getAttribute('data-datetime')); } } setTimeout(timeAgo, 60000); })(); /*]]>*/</script>
                                    </b:if>
                                  </div>
                      
                                  <b:if cond='data:post.allowNewComments'>
                                    <div class='cmAd hidden' id='addCm'>
                                      <div aria-label='Berkomentar' class='cmBtn button' role='button'>
                                        <!--[ Delete tag bellow to change button style ]-->
                                        <b:class name='ln'/>
                                          
                                        <b:message name='messages.postAComment'/>
                                      </div>
                                    </div>
                                  </b:if>
                              
                                  <b:if cond='data:view.url != data:view.url params { amp: &quot;1&quot; }'>
                                    <script>var comment = true;</script>
                                  </b:if>
                                  <b:else/>
                                  <b:if cond='data:view.url != data:view.url params { amp: &quot;1&quot; }'>
                                    <script>var comment = false;</script>
                                  </b:if>
                                </b:if>
                    
                                <div class='cmFrm'>
                                  <b:if cond='data:post.embedCommentForm'>
                                    <b:if cond='data:post.allowNewComments'>
                                      <b:include data='post' name='threadedComments-form'/>
                                      <b:else/>
                                      <!--[ If comment was disable ]-->
                                      <div class='cmDis'><data:post.noNewCommentsText/></div>
                                    </b:if>
                                    <b:else/>
                                    <b:if cond='data:post.allowComments'>
                                      <!--[ Comment message ]-->
                                      <b:if cond='data:this.messages.blogComment != &quot;&quot;'>
                                        <div class='cmMs note'>
                                          <data:this.messages.blogComment/>
                                        </div>
                                      </b:if>
                                        
                                      <a class='cmBtn button' expr:href='data:post.commentsUrl' expr:onclick='data:post.commentsUrlOnclick' rel='noreferrer' role='button' target='_blank'>
                                        <!--[ Delete tag bellow to change button style ]-->
                                        <b:class name='ln'/>
                                          
                                        <b:message name='messages.postAComment'/>
                                      </a>
                                    </b:if>
                                  </b:if>
                                </div>
                              </div>
                         
                            </b:tag>
                          </b:tag>
                        
                          <label class='fCls' for='forComments'/>
                        </section>
                  
                        <b:if cond='data:post.allowNewComments and data:view.url != data:view.url params { amp: &quot;1&quot; }'>
                          <script>/*<![CDATA[*/ document.addEventListener('DOMContentLoaded', function() { var a=document, b = a.getElementById('comment-editor'), d = b.getAttribute('data-src'); if (b.setAttribute('src', d), 1 == comment) { var f = a.getElementsByClassName('rpTo'), c = a.getElementById('commentForm'), h = f.length, k = function(b, d, e, f) { b.addEventListener('click', function() { var c = b.getAttribute('data-reply-to'); a.getElementById('c' + c).appendChild(d); a.getElementById('commentForm').className = 'cmRbox'; a.getElementById('addCm').className = 'cmAd'; e.src = f + '&parentID=' + c }) }; for (i = 0; i < h; i++) k(f[i], c, b, d); var l = a.getElementsByClassName('cmFrm')[0]; a.getElementById('addCm').addEventListener('click', function() { l.appendChild(c); a.getElementById('commentForm').className = 'cmRbox'; a.getElementById('addCm').className = 'cmAd hidden'; b.src = d }) } }); /*]]>*/</script>
                        </b:if>
                        <b:if cond='data:view.url != data:view.url params { amp: &quot;1&quot; }'>
                          <script>/*<![CDATA[*/ /* Comment tag, license: dte.web.id/teknis/paket-javascript-fitur-manipulasi */ function repText(id) {var a = document.getElementById(id); if (!a) return; var b = a.innerHTML; b = b.replace(/<i rel="image">(.*?)<\/i>/ig, "<img class='lazy' data-src='$1' src='data:image/png;base64,R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs=' alt='Image Comment' \/>"); a.innerHTML = b;} repText('cmHolder'); /*]]>*/</script>
                        </b:if>
                      </b:includable>
                    </b:widget>
                    <b:widget cond='data:view.isPost and !data:view.isPreview and data:view.url != data:view.url params { amp: &quot;1&quot; }' id='HTML01' locked='true' title='Middle post ad 01' type='HTML' version='2' visible='false'>
                      <b:widget-settings>
                        <b:widget-setting name='content'>&lt;ins class=&quot;adsbygoogle&quot;
     style=&quot;display:block&quot;
     data-ad-client=&quot;ca-pub-3400053731432707&quot;
     data-ad-slot=&quot;4052950217&quot;
     data-ad-format=&quot;auto&quot;
     data-full-width-responsive=&quot;true&quot;&gt;&lt;/ins&gt;
&lt;script&gt;
     (adsbygoogle = window.adsbygoogle || []).push({});
&lt;/script&gt;</b:widget-setting>
                      </b:widget-settings>
                      <b:includable id='main'>
                        <div class='widget-content'>
                          <b:if cond='data:content != &quot;&quot;'>
                            <data:content/>
                          
                            <b:else/>
                            <!--[ Blank ad ]-->
                            <div class='adB' expr:data-text='data:messages.adsGoHere'/>
                          </b:if>
                    
                          <!--[ Script to move widget to the middle of article ]-->
                          <script>/*<![CDATA[*/ function insertAfter(tbh,tgt) {var prt = tgt.parentNode; if (prt.lastChild == tgt) {prt.appendChild(tbh);} else {prt.insertBefore(tbh,tgt.nextSibling);}} var tgt = document.getElementById('postBody'); var midAd01 = document.getElementById('HTML01'); var showAd01 = tgt.getElementsByTagName('p'); if (showAd01.length > 0) {insertAfter(midAd01,showAd01[10]);}; /*]]>*/</script>
                        </div>
                      </b:includable>
                    </b:widget>
                    <b:widget cond='data:view.isPost and !data:view.isPreview and data:view.url != data:view.url params { amp: &quot;1&quot; }' id='HTML02' locked='true' title='Middle post ad 02' type='HTML' version='2' visible='false'>
                      <b:widget-settings>
                        <b:widget-setting name='content'>&lt;ins class=&quot;adsbygoogle&quot;
     style=&quot;display:block&quot;
     data-ad-client=&quot;ca-pub-3400053731432707&quot;
     data-ad-slot=&quot;4052950217&quot;
     data-ad-format=&quot;auto&quot;
     data-full-width-responsive=&quot;true&quot;&gt;&lt;/ins&gt;
&lt;script&gt;
     (adsbygoogle = window.adsbygoogle || []).push({});
&lt;/script&gt;</b:widget-setting>
                      </b:widget-settings>
                      <b:includable id='main'>
                        <div class='widget-content'>
                          <b:if cond='data:content != &quot;&quot;'>
                            <data:content/>
                          
                            <b:else/>
                            <!--[ Blank ad ]-->
                            <div class='adB' expr:data-text='data:messages.adsGoHere'/>
                          </b:if>
                        
                          <!--[ Script to move widget to the middle of article ]-->
                          <script>/*<![CDATA[*/ function insertAfter(tbh,tgt) {var prt = tgt.parentNode; if (prt.lastChild == tgt) {prt.appendChild(tbh);} else {prt.insertBefore(tbh,tgt.nextSibling);}} var tgt = document.getElementById('postBody'); var midAd02 = document.getElementById('HTML02'); var showAd02 = tgt.getElementsByTagName('p'); if (showAd02.length > 0) {insertAfter(midAd02,showAd02[20]);}; /*]]>*/</script>
                        </div>
                      </b:includable>
                    </b:widget>
                  </b:section>
                
                  <b:section cond='!data:view.isPreview and !data:view.isSingleItem' id='add-widget' showaddelement='true'>
                    <b:widget cond='!data:view.isPreview' id='HTML94' locked='true' title='Ad placement' type='HTML' version='2' visible='false'>
                      <b:widget-settings>
                        <b:widget-setting name='content'>&lt;ins class=&quot;adsbygoogle&quot;
     style=&quot;display:block&quot;
     data-ad-client=&quot;ca-pub-3400053731432707&quot;
     data-ad-slot=&quot;4052950217&quot;
     data-ad-format=&quot;auto&quot;
     data-full-width-responsive=&quot;true&quot;&gt;&lt;/ins&gt;
&lt;script&gt;
     (adsbygoogle = window.adsbygoogle || []).push({});
&lt;/script&gt;</b:widget-setting>
                      </b:widget-settings>
                      <b:includable id='main'>
                        <div class='widget-content'>
                          <b:if cond='data:content != &quot;&quot;'>
                            <data:content/>
                          
                            <b:else/>
                            <!--[ Blank ad ]-->
                            <div class='adB' expr:data-text='data:messages.adsGoHere'/>
                          </b:if>
                        </div>
                      </b:includable>
                    </b:widget>
                  </b:section>
                </main>
                
                <b:if cond='data:view.isHomepage or data:view.isPost'>
                  <!--[ Sidebar content ]-->
                  <b:tag class='blogItm sidebar' name='aside'>
                    <b:tag class='sideIn' name='div'>
                      <b:section id='side-widget' showaddelement='true'>
                        <b:widget id='HTML1' locked='false' title='Search' type='HTML' visible='false'>
                          <b:widget-settings>
                            <b:widget-setting name='content'>&lt;script async src=&quot;https://cse.google.com/cse.js?cx=b1ec7e4d04f414ea1&quot;&gt;
&lt;/script&gt;
&lt;div class=&quot;gcse-search&quot;&gt;&lt;/div&gt;</b:widget-setting>
                          </b:widget-settings>
                          <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
                        </b:widget>
                        <b:widget id='PopularPosts00' locked='false' title='Popular Posts' type='PopularPosts' version='2' visible='true'>
                          <b:widget-settings>
                            <b:widget-setting name='numItemsToShow'>5</b:widget-setting>
                            <b:widget-setting name='showThumbnails'>true</b:widget-setting>
                            <b:widget-setting name='showSnippets'>false</b:widget-setting>
                            <b:widget-setting name='timeRange'>LAST_WEEK</b:widget-setting>
                          </b:widget-settings>
                          <b:includable id='main' var='this'>
                            <b:if cond='data:title != &quot;&quot;'>
                              <h2 class='title'><data:title/></h2>
                            </b:if>
                            <b:include name='snippetedPosts'/>
                          </b:includable>
                          <b:includable id='blogThisShare'/>
                          <b:includable id='bylineByName' var='byline'/>
                          <b:includable id='bylineRegion' var='regionIts'/>
                          <b:includable id='commentsLink'/>
                          <b:includable id='commentsLinkIframe'/>
                          <b:includable id='emailPostIcon'/>
                          <b:includable id='facebookShare'/>
                          <b:includable id='footerBylines'/>
                          <b:includable id='googlePlusShare'/>
                          <b:includable id='headerByline'/>
                          <b:includable id='linkShare'/>
                          <b:includable id='otherSharingButton'/>
                          <b:includable id='platformShare'/>
                          <b:includable id='postAuthor'/>
                          <b:includable id='postCommentsLink'/>
                          <b:includable id='postInfo'>
                            <div class='iInf pSml'>
                              <b:if cond='data:post.labels any (label =&gt; label.name in [ &quot;Sponsored&quot; ])'>
                                <b:include name='postLabelSponsored'/>
                                <b:else/>
                                
                                <!--[ Post timestamp ]-->
                                <b:include cond='data:widgets.Blog.first.allBylineItems.timestamp' name='postTimestamp'/>
                                <b:include cond='data:post.labels' name='postLabel'/>
                              </b:if>
                            </div>
                          </b:includable>
                          <b:includable id='postJumpLink' var='post'/>
                          <b:includable id='postLabels'/>
                          <b:includable id='postLocation'/>
                          <b:includable id='postReactions'/>
                          <b:includable id='postShareButtons'/>
                          <b:includable id='postTimestamp'>
                            <time class='aTtmp iTtmp pbl' expr:data-text='format(data:post.date, &quot;MMM d&quot;)' expr:datetime='data:post.date.iso8601' expr:title='&quot;Published: &quot; + data:post.date format &quot;MMMM d, y&quot;'/>
                          </b:includable>
                          <b:includable id='sharingButton'/>
                          <b:includable id='sharingButtonContent'/>
                          <b:includable id='sharingButtons'/>
                          <b:includable id='sharingButtonsMenu'/>
                          <b:includable id='sharingPlatformIcon'/>
                          <b:includable id='snippetedPostByline'/>
                          <b:includable id='snippetedPostContent'>
                            <!--[ Post thumbnail ]-->
                            <b:include cond='data:i == 0 and (data:this.postDisplay.showFeaturedImage and data:post.featuredImage)' name='snippetedPostThumbnail'/>
                      
                            <b:include name='postInfo'/>
                              
                            <div class='iCtnt'>
                              <div class='iInr'>
                                <b:include cond='data:this.postDisplay.showTitle' name='snippetedPostTitle'/>
                                <b:include cond='data:this.postDisplay.showSnippet and data:i == 0' name='snippetedPostEntry'/>
                              </div>
                            </div>
                          </b:includable>
                          <b:includable id='snippetedPostEntry'>
                            <div class='pSnpt'>
                              <b:include name='postEntrySnippet'/>
                            </div>
                          </b:includable>
                          <b:includable id='snippetedPostThumbnail'>
                            <div class='iThmb pThmb'>
                              <b:class cond='data:post.featuredImage.isYoutube' name='iyt'/>
                              <b:class cond='!data:this.postDisplay.showFeaturedImage or !data:post.featuredImage' name='nul'/>
                              <b:tag class='thmb' expr:name='data:this.postDisplay.showFeaturedImage and data:post.featuredImage ? &quot;a&quot; : &quot;div&quot;'>
                                <b:attr cond='data:this.postDisplay.showFeaturedImage and data:post.featuredImage' expr:value='data:post.url' name='href'/>
                                <b:if cond='data:this.postDisplay.showFeaturedImage and data:post.featuredImage'>
                                  <b:include name='postEntryThumbnail'/>
                                  <b:else/>
                                  <span class='imgThm' data-text='No image'/>
                                </b:if>
                              </b:tag>
                              
                              <!--[ Comments count ]-->
                              <b:tag class='iFxd' cond='data:post.allowComments and data:post.numberOfComments &gt; 0 or data:post.labels any (label =&gt; label.name in [ &quot;Sponsored&quot; ])' name='div'>
                                <b:if cond='data:post.labels any (label =&gt; label.name in [ &quot;Sponsored&quot; ])'>
                                  <b:include name='postSponsored'/>
                                </b:if>
                                <b:if cond='data:widgets.Blog.first.allBylineItems.comments'>
                                  <b:include name='postCommentsLinks'/>
                                </b:if>
                              </b:tag>
                            </div>
                          </b:includable>
                          <b:includable id='snippetedPostTitle'>
                            <h3 class='iTtl aTtl'><a expr:href='data:post.url.canonical'><data:post.title.escaped/></a></h3>
                          </b:includable>
                          <b:includable id='snippetedPosts'>
                            <div class='itemPp' role='feed'>
                              <!-- Don't render the post that we're currently already looking at. -->
                              <b:loop index='i' values='data:posts filter (p =&gt; p.id != data:view.postId)' var='post'>
                                <article class='itm'>
                                  <b:class cond='data:i == 0 and data:this.postDisplay.showFeaturedImage and !data:post.featuredImage' name='nThmb'/>
                                  <b:class cond='data:i == 0 and data:this.postDisplay.showFeaturedImage and data:post.featuredImage' name='mostP'/>
                                  <b:include name='snippetedPostContent'/>
                                </article>
                              </b:loop>
                            </div>
                          </b:includable>
                        </b:widget>
                        <b:widget id='Label00' locked='false' title='Labels' type='Label' version='2' visible='true'>
                          <b:widget-settings>
                            <b:widget-setting name='sorting'>ALPHA</b:widget-setting>
                            <b:widget-setting name='display'>LIST</b:widget-setting>
                            <b:widget-setting name='selectedLabelsList'/>
                            <b:widget-setting name='showType'>ALL</b:widget-setting>
                            <b:widget-setting name='showFreqNumbers'>true</b:widget-setting>
                          </b:widget-settings>
                          <b:includable id='main' var='this'>
                            <b:include name='widget-title'/>
                            <b:include name='content'/>
                          </b:includable>
                          <b:includable id='cloud'>
                            <b:loop index='tags' values='data:labels' var='label'>
                         
                              <!--[ Only show 6 label ]-->
                              <b:if cond='data:tags &lt;= 5'>
                                <div class='lbSz'>
                                  <b:class expr:name='&quot;s-&quot; + data:label.cssSize'/>
                                  <b:tag class='lbN' expr:name='data:blog.url != data:label.url ? &quot;a&quot; : &quot;div&quot;'>
                                    <b:attr cond='data:blog.url != data:label.url' expr:value='data:label.url' name='href'/>
                                    <b:attr cond='data:blog.url != data:label.url' expr:value='data:label.name' name='aria-label'/>
                                    <span class='lbT'><data:label.name/></span>
                                    <b:tag class='lbC' cond='data:this.showFreqNumbers' expr:data-text='&quot;(&quot; + data:label.count + &quot;)&quot;' name='span'/>
                                  </b:tag>
                                </div>
                              </b:if>
                        
                              <!--[ Hide another label from 7th list ]-->
                              <b:if cond='data:tags == 6'>
                                <div class='lbSh'>
                                  <input class='lbIn hidden' id='lbAl-1' type='checkbox'/>
                                  <div class='lbAl'>
                                    <b:loop index='alltags' values='data:labels' var='label'>
                               
                                      <!--[ Show label from 7th list ]-->
                                      <b:if cond='data:alltags &gt;= 6'>
                                        <div class='lbSz'>
                                          <b:class expr:name='&quot;s-&quot; + data:label.cssSize'/>
                                          <b:tag class='lbN' expr:name='data:blog.url != data:label.url ? &quot;a&quot; : &quot;div&quot;'>
                                            <b:attr cond='data:blog.url != data:label.url' expr:value='data:label.url' name='href'/>
                                            <b:attr cond='data:blog.url != data:label.url' expr:value='data:label.name' name='aria-label'/>
                                            <span class='lbT'><data:label.name/></span>
                                            <b:tag class='lbC' cond='data:this.showFreqNumbers' expr:data-text='&quot;(&quot; + data:label.count + &quot;)&quot;' name='span'/>
                                          </b:tag>
                                        </div>
                                      </b:if>
                                
                                    </b:loop>
                                  </div>
                            
                                  <label aria-label='Show labels' class='lbM' expr:data-hide='data:messages.showLess' expr:data-show='data:messages.showMore' expr:data-text='&quot;(+&quot; + (data:labels.length - 6) + &quot;)&quot;' for='lbAl-1'/>
                                </div>
                              </b:if>
                            </b:loop>
                          </b:includable>
                          <b:includable id='content'>
                            <div class='wL pSml'>
                              <!--[ delete the comment tag below if you want to change style Label List ]-->
                              <b:class name='bg'/>
                                
                              <b:class expr:name='data:this.display == &quot;list&quot; ? &quot;ls&quot; : &quot;cl&quot;'/>
                              <b:include cond='data:this.display == &quot;list&quot;' name='list'/>
                              <b:include cond='data:this.display == &quot;cloud&quot;' name='cloud'/>
                            </div>
                          </b:includable>
                          <b:includable id='list'>
                            <ul>
                              <b:loop index='tags' values='data:labels' var='label'>
                              
                                <!--[ Only show 6 label ]-->
                                <b:if cond='data:tags &lt;= 5'>
                                  <li>
                                    <b:tag class='lbN' expr:name='data:blog.url != data:label.url ? &quot;a&quot; : &quot;div&quot;'>
                                      <b:attr cond='data:blog.url != data:label.url' expr:value='data:label.url' name='href'/>
                                      <b:attr cond='data:blog.url != data:label.url' expr:value='data:label.name' name='aria-label'/>
                                      <span class='lbT'><data:label.name/></span>
                                      <span class='lbR'>
                                        <b:tag class='lbC' cond='data:this.showFreqNumbers' expr:data-text='data:label.count' name='span'/>
                                        <b:include name='bookmark-icon'/>
                                      </span>
                                    </b:tag>
                                  </li>
                                </b:if>
                          
                              </b:loop>
                            </ul>
                              
                            <b:loop index='tags' values='data:labels' var='label'>
                              <!--[ Hide another label from 7th list ]-->
                              <b:if cond='data:tags == 6'>
                                <div class='lbSh'>
                                  <input class='lbIn hidden' id='lbAl-2' type='checkbox'/>
                                  <ul class='lbAl'>
                                    <b:loop index='alltags' values='data:labels' var='label'>
                                      
                                      <!--[ Show label from 7th list ]-->
                                      <b:if cond='data:alltags &gt;= 6'>
                                        <li>
                                          <b:tag class='lbN' expr:name='data:blog.url != data:label.url ? &quot;a&quot; : &quot;div&quot;'>
                                            <b:attr cond='data:blog.url != data:label.url' expr:value='data:label.url' name='href'/>
                                            <b:attr cond='data:blog.url != data:label.url' expr:value='data:label.name' name='aria-label'/>
                                            <span class='lbT'><data:label.name/></span>
                                            <span class='lbR'>
                                              <b:tag class='lbC' cond='data:this.showFreqNumbers' expr:data-text='data:label.count' name='span'/>
                                              <b:include name='bookmark-icon'/>
                                            </span>
                                          </b:tag>
                                        </li>
                                      </b:if>
                                  
                                    </b:loop>
                                  </ul>
                              
                                  <label aria-label='Show labels' class='lbM' expr:data-hide='data:messages.showLess' expr:data-show='data:messages.showMore' expr:data-text='&quot;(+&quot; + (data:labels.length - 6) + &quot;)&quot;' for='lbAl-2' role='button'/>
                                </div>
                              </b:if>
                            </b:loop>
                          </b:includable>
                        </b:widget>
                        <b:widget cond='data:view.isHomepage' id='Profile1' locked='false' title='Contributors' type='Profile' version='2' visible='true'>
                          <b:widget-settings>
                            <b:widget-setting name='showaboutme'>true</b:widget-setting>
                            <b:widget-setting name='showlocation'>false</b:widget-setting>
                          </b:widget-settings>
                          <b:includable id='main' var='this'>
                            <b:include name='widget-title'/>
                            <b:include name='content'/>
                          </b:includable>
                          <b:includable id='authorProfileImage'>
                            <div class='im' expr:data-style='&quot;background-image: url(&quot; + resizeImage(data:authorPhoto.image,60) + &quot;)&quot;'>
                              <b:class cond='data:view.url != data:view.url params { amp: &quot;1&quot; }' name='lazy'/>
                              <b:attr cond='data:view.url == data:view.url params { amp: &quot;1&quot; }' expr:value='&quot;background-image: url(&quot; + resizeImage(data:authorPhoto.image,60) + &quot;)&quot;' name='style'/>
                            </div>
                            <noscript><div class='im' expr:style='&quot;background-image: url(&quot; + resizeImage(data:authorPhoto.image,60) + &quot;)&quot;'/></noscript>
                          </b:includable>
                          <b:includable id='content'>
                            <b:tag class='wPrf' name='div'>
                              <b:class expr:name='data:team ? &quot;tm&quot; : &quot;sl&quot;'/>
                              <b:class cond='data:showlocation and data:location != &quot;&quot;' name='nLoc'/>
                              <b:if cond='data:team'>
                                <b:include name='teamProfile'/>
                                <b:else/>
                                <b:include name='userProfile'/>
                              </b:if>
                            </b:tag>
                          </b:includable>
                          <b:includable id='defaultProfileImage'>
                            <div class='im'><b:include name='profile-icon'/></div>
                          </b:includable>
                          <b:includable id='profileHeader'>
                            <div class='prfH fixH fixT' expr:data-text='data:title'>
                              <label aria-label='Close' class='c cl' for='allTeam'/>
                            </div>
                          </b:includable>
                          <b:includable id='profileImage'>
                            <b:if cond='data:authorPhoto.image'>
                              <b:include name='authorProfileImage'/>
                              <b:else/>
                              <b:include name='defaultProfileImage'/>
                            </b:if>
                          </b:includable>
                          <b:includable id='teamProfile'>
                            <!--[ All admin name ]-->
                            <b:loop index='team' values='data:authors' var='author'>
                              <!-- Show contributor less than 5 -->
                              <b:if cond='data:team &lt;= 4'>
                                <b:include data='author' name='teamProfileImg'/>
                              </b:if>
                                
                              <!-- Show 5th order contributors -->
                              <b:if cond='data:team == 5'>
                                <div class='mIm'>
                                  <label aria-label='All Member' class='am' expr:data-text='&quot;+&quot; + (data:authors.length - 5)' for='allTeam'/>
                                </div>
                                
                                <!-- Show all member/contributor in this blog -->
                                <input class='tmIn fixi hidden' id='allTeam' type='checkbox'/>
                                <div class='tmB fixL'>
                                  <div class='tmBr fixLi'>
                                    <div class='tmBs fixLs'>
                                      <b:include name='profileHeader'/>
                                      
                                      <div class='tmC'>
                                        <b:loop values='data:authors' var='author'>
                                          <div class='t'>
                                            <b:include data='author' name='teamProfileName'/>
                                          </div>
                                        </b:loop>
                                      </div>
                                    </div>
                                  </div>
                                  <label class='fCls' for='allTeam'/>
                                </div>
                              </b:if>
                            </b:loop>
                          </b:includable>
                          <b:includable id='teamProfileImg'>
                            <div class='sIm' expr:data-text='data:display-name'><b:include name='profileImage'/></div>
                          </b:includable>
                          <b:includable id='teamProfileLink'>
                            <a class='prfL' expr:aria-label='data:display-name' expr:data-text='data:display-name' expr:href='data:userUrl' rel='noreferrer' target='_blank'>
                              <b:include name='profileImage'/>
                            </a>
                          </b:includable>
                          <b:includable id='teamProfileName'>
                            <div class='prfL' expr:aria-label='data:display-name' expr:data-text='data:display-name'>
                              <b:include name='profileImage'/>
                            </div>
                          </b:includable>
                          <b:includable id='userGoogleProfile'/>
                          <b:includable id='userLocation'>
                            <dd class='lc' expr:data-text='data:location'><b:include name='location-icon'/></dd>
                          </b:includable>
                          <b:includable id='userProfile'>
                            <b:include name='userProfileImage'/>
                            <b:include name='userProfileInfo'/>
                          </b:includable>
                          <b:includable id='userProfileData'>
                            <dt class='sDt'>
                              <!--[ Profile name without link ]-->
                              <!--<b:include name='userProfileNameOnly'/>-->
                        
                              <!--[ Profile name with link ]-->
                              <b:include name='userProfileNameOnly'/>
                            </dt>
                          </b:includable>
                          <b:includable id='userProfileImage'>
                            <div class='sIm'>
                              <b:include name='profileImage'/>
                            </div>
                          </b:includable>
                          <b:includable id='userProfileInfo'>
                            <dl class='sInf'>
                              <b:include name='userProfileData'/>
                              <b:include cond='data:aboutme != &quot;&quot;' name='userProfileText'/>
                              <b:include cond='data:showlocation and data:location != &quot;&quot;' name='userLocation'/>
                            </dl>
                          </b:includable>
                          <b:includable id='userProfileLink'>
                            <a class='l extL' expr:href='data:userUrl' expr:title='data:messages.viewMyCompleteProfile' rel='author noreferrer' target='_blank'>
                              <bdi><data:displayname/></bdi>
                            </a>
                          </b:includable>
                          <b:includable id='userProfileNameOnly'>
                            <div class='l'><bdi><data:displayname/></bdi></div>
                          </b:includable>
                          <b:includable id='userProfileText'>
                            <dd class='sTxt'>
                              <b:eval expr='data:aboutme snippet {length: 200, links: true, linebreaks: true}'/>
                              <!--<data:aboutme/>-->
                            </dd>
                          </b:includable>
                          <b:includable id='viewProfileLink'/>
                        </b:widget>
                        <b:widget id='ContactForm1' locked='false' title='Kontak' type='ContactForm' version='2' visible='true'>
                          <b:includable id='main'>
  <b:include name='widget-title'/>
  <b:include name='content'/>
</b:includable>
                          <b:includable id='content' style='display:none'>
  <div class='contact-form-widget'>
    <div class='form'>
      <form name='contact-form'>
        <p/>
        <data:contactFormNameMsg/>
        <br/>
        <input class='contact-form-name' expr:id='data:widget.instanceId + &quot;_contact-form-name&quot;' name='name' size='30' type='text' value=''/>
        <p/>
        <data:contactFormEmailMsg/> <span style='font-weight: bolder;'>*</span>
        <br/>
        <input class='contact-form-email' expr:id='data:widget.instanceId + &quot;_contact-form-email&quot;' name='email' size='30' type='text' value=''/>
        <p/>
        <data:contactFormMessageMsg/> <span style='font-weight: bolder;'>*</span>
        <br/>
        <textarea class='contact-form-email-message' cols='25' expr:id='data:widget.instanceId + &quot;_contact-form-email-message&quot;' name='email-message' rows='5'/>
        <p/>
        <input class='contact-form-button contact-form-button-submit' expr:id='data:widget.instanceId + &quot;_contact-form-submit&quot;' expr:value='data:contactFormSendMsg' type='button'/>
        <p/>
        <div style='text-align: center; max-width: 222px; width: 100%'>
          <p class='contact-form-error-message' expr:id='data:widget.instanceId + &quot;_contact-form-error-message&quot;'/>
          <p class='contact-form-success-message' expr:id='data:widget.instanceId + &quot;_contact-form-success-message&quot;'/>
        </div>
      </form>
    </div>
  </div>
</b:includable>
                        </b:widget>
                      </b:section>
              
                      <!--[ Sidebar sticky ]-->
                      <b:section class='sideSticky' cond='!data:view.isPreview' id='side-sticky' showaddelement='true'>
                        <b:widget cond='!data:view.isPreview and !data:blog.isMobileRequest' id='HTML95' locked='true' title='Sticky ad placement(desktop only)' type='HTML' version='2' visible='true'>
                          <b:widget-settings>
                            <b:widget-setting name='content'>&lt;ins class=&quot;adsbygoogle&quot;
     style=&quot;display:block&quot;
     data-ad-client=&quot;ca-pub-3400053731432707&quot;
     data-ad-slot=&quot;4052950217&quot;
     data-ad-format=&quot;auto&quot;
     data-full-width-responsive=&quot;true&quot;&gt;&lt;/ins&gt;
&lt;script&gt;
     (adsbygoogle = window.adsbygoogle || []).push({});
&lt;/script&gt;</b:widget-setting>
                          </b:widget-settings>
                          <b:includable id='main'>
                            <b:if cond='data:content != &quot;&quot;'>
                              <data:content/>
                          
                              <b:else/>
                              <!--[ Blank ad ]-->
                              <div class='adB' expr:data-text='data:messages.adsGoHere'/>
                            </b:if>
                          </b:includable>
                        </b:widget>
                      </b:section>
                    </b:tag>
                  </b:tag>
                </b:if>
              </b:tag>
            </div>
          </div> 
        </div>
        
        <!--[ Footer section ]-->
        <footer>
          <div class='secIn'>
            <div class='fotIn'>
              <b:section id='footer-widget-1' maxwidgets='2' showaddelement='true'>
                <b:widget id='HTML77' locked='false' title='Disusun oleh :' type='HTML' version='2' visible='true'>
                  <b:widget-settings>
                    <b:widget-setting name='content'>&lt;div class=&#39;abtT&#39;&gt;
  &lt;h2 class=&#39;tl&#39;&gt;trjy17.com&lt;/h2&gt;

  &lt;!--[ Delete comment tag on section bellow and change data-src=&#39;#&#39; attribute with your logo url ]--&gt;
  &lt;!--&lt;img class=&#39;lazy&#39; alt=&#39;trjy17&#39; data-src=&#39;	https://1.bp.blogspot.com/-ZbMOP5A2uQk/Y74awipWqEI&#8230;view%2526id%253D16eRMt9JQJjYW2sB3Ii-4h3ID2xA1KVQD&#39; src=&#39;data:image/png;base64,R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs=&#39;/&gt; --&gt;

&lt;/div&gt;

&lt;p class=&#39;abtD&#39;&gt;Owner : Putra Panji Prasetiyo.&lt;/p&gt;</b:widget-setting>
                  </b:widget-settings>
                  <b:includable id='main'>
                    <div class='widget-content abtU' expr:data-text='data:title'>
                      <data:content/>
                    </div>
                  </b:includable>
                </b:widget>
                <b:widget id='LinkList1' locked='false' title='Social Media Link' type='LinkList' version='2' visible='true'>
                  <b:widget-settings>
                    <b:widget-setting name='sorting'>ALPHABETICAL</b:widget-setting>
                    <b:widget-setting name='text-1'>Tiktok</b:widget-setting>
                    <b:widget-setting name='link-1'>https://www.tiktok.com/@trjy17_</b:widget-setting>
                    <b:widget-setting name='text-0'>Instagram</b:widget-setting>
                    <b:widget-setting name='link-2'>https://www.youtube.com/c/Ppanji_</b:widget-setting>
                    <b:widget-setting name='link-0'>https://www.instagram.com/trjy17/</b:widget-setting>
                    <b:widget-setting name='text-2'>Youtube</b:widget-setting>
                  </b:widget-settings>
                  <b:includable id='main'>
                    <b:include name='content'/>
                  </b:includable>
                  <b:includable id='content'>                    
                    <ul class='sL'>                      
                      <b:loop values='data:links' var='link'>
                        <li>
                          <b:tag class='l' expr:data-text='data:link.name' expr:name='data:link.target != &quot;#&quot; ? &quot;a&quot; : &quot;span&quot;'>
                            <b:attr cond='data:link.target != &quot;#&quot;' expr:value='data:link.target' name='href'/>
                            <b:attr cond='data:link.target != &quot;#&quot;' expr:value='data:link.name' name='aria-label'/>
                            <b:attr cond='data:link.target != &quot;#&quot;' name='target' value='_blank'/>
                            <b:attr cond='data:link.target != &quot;#&quot;' name='rel' value='noopener'/>
                          </b:tag>
                        </li>
                      </b:loop>
                    </ul>
                  </b:includable>
                </b:widget>
              </b:section>
              <b:section id='footer-widget-2' maxwidgets='2' showaddelement='true'>
                <b:widget id='LinkList2' locked='false' title='Situs Web' type='LinkList' version='2' visible='true'>
                  <b:widget-settings>
                    <b:widget-setting name='shownum'>3</b:widget-setting>
                    <b:widget-setting name='sorting'>NONE</b:widget-setting>
                    <b:widget-setting name='text-1'>Disclaimer</b:widget-setting>
                    <b:widget-setting name='link-1'>https://www.trjy17.com/p/disclaimer.html</b:widget-setting>
                    <b:widget-setting name='text-0'>Sitemap</b:widget-setting>
                    <b:widget-setting name='link-2'>https://www.trjy17.com/p/kebijakan-privasi.html</b:widget-setting>
                    <b:widget-setting name='link-0'>https://www.trjy17.com/p/sitemap.html</b:widget-setting>
                    <b:widget-setting name='text-2'>Privasi</b:widget-setting>
                  </b:widget-settings>
                  <b:includable id='main'>
                    <b:include name='widget-title'/>
                    <b:include name='content'/>
                  </b:includable>
                  <b:includable id='content'>
                    <div class='widget-content'>
                      <ul>
                        <b:loop values='data:links' var='link'>
                          <li>
                            <a expr:href='data:link.target'>
                              <span><data:link.name/></span>
                            </a>
                          </li>
                        </b:loop>
                      </ul>
                    </div>
                  </b:includable>
                </b:widget>
              </b:section>
              <b:section id='footer-widget-3' maxwidgets='2' showaddelement='true'>
                <b:widget id='LinkList3' locked='false' title='Dukungan' type='LinkList' version='2' visible='true'>
                  <b:widget-settings>
                    <b:widget-setting name='sorting'>NONE</b:widget-setting>
                    <b:widget-setting name='text-1'>Kontak</b:widget-setting>
                    <b:widget-setting name='link-1'>https://www.trjy17.com/p/kontak_6.html</b:widget-setting>
                    <b:widget-setting name='text-0'>Tentang</b:widget-setting>
                    <b:widget-setting name='link-2'>#</b:widget-setting>
                    <b:widget-setting name='link-0'>https://www.trjy17.com/p/tentang-trjy17_8.html</b:widget-setting>
                    <b:widget-setting name='text-2'>Traktir Teh</b:widget-setting>
                  </b:widget-settings>
                  <b:includable id='main'>
                    <b:include name='widget-title'/>
                    <b:include name='content'/>
                  </b:includable>
                  <b:includable id='content'>
                    <div class='widget-content'>
                      <ul>
                        <b:loop values='data:links' var='link'>
                          <li>
                            <a expr:href='data:link.target'>
                              <span><data:link.name/></span>
                            </a>
                          </li>
                        </b:loop>
                      </ul>
                    </div>
                  </b:includable>
                </b:widget>
              </b:section>
              <b:section id='footer-widget-4' maxwidgets='2' showaddelement='true'>
                <b:widget id='Stats1' locked='false' title='Kunjungan' type='Stats' visible='true'>
                  <b:widget-settings>
                    <b:widget-setting name='showGraphicalCounter'>true</b:widget-setting>
                    <b:widget-setting name='showAnimatedCounter'>false</b:widget-setting>
                    <b:widget-setting name='showSparkline'>false</b:widget-setting>
                    <b:widget-setting name='sparklineStyle'>BLACK_TRANSPARENT</b:widget-setting>
                    <b:widget-setting name='timeRange'>ALL_TIME</b:widget-setting>
                  </b:widget-settings>
                  <b:includable id='main'>
  <b:include name='widget-title'/>
  <b:include name='content'/>
</b:includable>
                  <b:includable id='content'>
  <div class='widget-content'>
    <!-- Content is going to be visible when data will be fetched from server. -->
    <div expr:id='data:widget.instanceId + &quot;_content&quot;' style='display: none;'>
      <!-- Counter and image will be injected later via AJAX call. -->
      <b:if cond='data:showSparkline'>
        <script src='https://www.gstatic.com/charts/loader.js' type='text/javascript'/>
        <span expr:id='data:widget.instanceId + &quot;_sparklinespan&quot;' style='display:inline-block; width:75px; height:30px'/>
      </b:if>
      <span expr:class='&quot;counter-wrapper &quot; + (data:showGraphicalCounter ? &quot;graph-counter-wrapper&quot; : &quot;text-counter-wrapper&quot;)' expr:id='data:widget.instanceId + &quot;_totalCount&quot;'>
      </span>
    </div>
  </div>
</b:includable>
                </b:widget>
              </b:section>
            </div>
            
            <!--[ Credit ]-->
            <b:section class='cdtIn' id='credit-widget' maxwidgets='2' showaddelement='false'>
              <b:widget id='HTML88' locked='true' title='Credit' type='HTML' version='2' visible='true'>
                <b:widget-settings>
                  <b:widget-setting name='content'/>
                </b:widget-settings>
                <b:includable id='main'>
                  <div class='fotCd'>
                    <span class='credit'>
                      <b:if cond='data:content == &quot;&quot;'>
                        &#169; 2022 - <span id='getYear'><b:if cond='data:view.url != data:view.url params { amp: &quot;1&quot; }'><script>/*<![CDATA[*/ var d = new Date(); var n = d.getFullYear(); document.getElementById('getYear').innerHTML = n; /*]]>*/</script><b:else/>2021</b:if></span> &#8231; <bdi><a expr:href='data:blog.homepageUrl.canonical'><data:blog.title/></a></bdi> &#8231; All rights reserved.
                        <b:else/>
                        <data:content/>
                      </b:if>
                    </span>
                  </div>
                </b:includable>
              </b:widget>
              <b:widget id='TextList88' locked='true' title='Back to top' type='TextList' version='2' visible='true'>
                <b:widget-settings>
                  <b:widget-setting name='shownum'>1</b:widget-setting>
                  <b:widget-setting name='sorting'>NONE</b:widget-setting>
                  <b:widget-setting name='item-1'>Top</b:widget-setting>
                  <b:widget-setting name='item-0'>Top Sticky</b:widget-setting>
                </b:widget-settings>
                <b:includable id='main'>
                  <b:include name='content'/>
                </b:includable>
                <b:includable id='content'>
                  <b:loop index='t' values='data:items' var='item'>
                    <b:if cond='data:t &lt;= 0'>
                      <b:if cond='data:item == &quot;Top&quot;'>
                        <!--[ Back top button ]-->
                        <b:tag class='toTop tTop' expr:data-text='data:item' expr:name='data:view.url != data:view.url params { amp: &quot;1&quot; } ? &quot;div&quot; : &quot;a&quot;'>
                          <b:attr cond='data:view.url != data:view.url params { amp: &quot;1&quot; }' name='onclick' value='window.scrollTo({top: 0});'/>
                          <b:attr cond='data:view.url == data:view.url params { amp: &quot;1&quot; }' name='href' value='#mainCont'/>
                          <b:include name='arow-up-icon'/>
                        </b:tag>
                        
                        <b:elseif cond='data:item == &quot;Top Sticky&quot;'/>
                        <!--[ Back top button fixed/sticky ]-->
                        <b:tag class='toTopF tTop' expr:data-text='data:item' expr:name='data:view.url != data:view.url params { amp: &quot;1&quot; } ? &quot;div&quot; : &quot;a&quot;'>
                          <b:attr cond='data:view.url != data:view.url params { amp: &quot;1&quot; }' name='onclick' value='window.scrollTo({top: 0});'/>
                          <b:attr cond='data:view.url == data:view.url params { amp: &quot;1&quot; }' name='href' value='#mainCont'/>
                          <b:include name='arow-up-icon'/>
                        </b:tag>
                      </b:if>
                    </b:if>
                  </b:loop>
                </b:includable>
              </b:widget>
            </b:section>
          </div>
        </footer>
        
        <b:if cond='!data:view.isPreview'>
          <!--[ Delete 'or data:blog.isMobileRequest' if you want to show ad in both(desktop and mobile) ]-->
          <b:section cond='data:view.isLayoutMode or data:blog.isMobileRequest' id='anchor-ad' showaddelement='false'>
            <b:widget id='HTML99' locked='true' title='Anchor ad placement(mobile only)' type='HTML' version='2' visible='false'>
              <b:widget-settings>
                <b:widget-setting name='content'>&lt;ins class=&quot;adsbygoogle&quot;
     style=&quot;display:block&quot;
     data-ad-client=&quot;ca-pub-3400053731432707&quot;
     data-ad-slot=&quot;4052950217&quot;
     data-ad-format=&quot;auto&quot;
     data-full-width-responsive=&quot;true&quot;&gt;&lt;/ins&gt;
&lt;script&gt;
     (adsbygoogle = window.adsbygoogle || []).push({});
&lt;/script&gt;</b:widget-setting>
              </b:widget-settings>
              <b:includable id='main'>
                <!--[ Sticky ad ]-->
                <input class='ancrI hidden' id='ancrI' type='checkbox'/>
                <div class='ancrA'>
                  <label aria-label='Close Menu' class='ancrC' for='ancrI'/>
                  <div class='ancrCn'>
                    <b:if cond='data:content != &quot;&quot;'>
                      <data:content/>
                          
                      <b:else/>
                      <!--[ Blank ad ]-->
                      <div class='adB' expr:data-text='data:messages.adsGoHere'/>
                    </b:if>
                  </div>
                </div>
              </b:includable>
            </b:widget>
          </b:section>
        </b:if>
        
      </b:if>
    </b:tag>
    
    <b:tag class='erroP' cond='data:view.isLayoutMode or data:view.isError' name='section'>
      <b:section class='erroC' cond='data:view.isLayoutMode or data:view.isError' id='error-404' showaddelement='false'>
        <b:widget id='HTML404' locked='true' title='Take me back' type='HTML' version='2' visible='true'>
          <b:widget-settings>
            <b:widget-setting name='content'>&lt;h3&gt;&lt;span&gt;404&lt;/span&gt;Something Wrong!&lt;/h3&gt;

&lt;p&gt;The page you&#39;ve requested can&#39;t be found. Why don&#39;t you browse around?&lt;/p&gt;</b:widget-setting>
          </b:widget-settings>
          <b:includable id='main'>
            <data:content/>
            <a class='button' expr:href='data:blog.homepageUrl.canonical'><data:title/></a>
          </b:includable>
        </b:widget>
      </b:section>
    </b:tag>
    
    <!--[ Javascript disable condition ]-->
    <noscript>
      <input class='nJs hidden' id='forNoJS' type='checkbox'/>
      <div class='noJs' expr:data-text='data:blog.title + &quot; works best with JavaScript enabled&quot;'>
        <label for='forNoJS'/>
      </div>
    </noscript>
    
    <b:if cond='!data:view.isError and data:view.url != data:view.url params { amp: &quot;1&quot; }'>
      <!--[ Load More - Delete this section if you want to disable this feature ]-->
      <b:include cond='data:view.isHomepage or data:view.url == data:blog.homepageUrl.canonical path &quot;search&quot;' name='post-paginationMore'/>
      
      <!--[ additional javascript ]-->
      <script>/*<![CDATA[*/ function darkMode(){localStorage.setItem("mode","darkmode"===localStorage.getItem("mode")?"light":"darkmode"),"darkmode"===localStorage.getItem("mode")?document.querySelector("#mainCont").classList.add("drK"):document.querySelector("#mainCont").classList.remove("drK")}; function gridMode(){localStorage.setItem("list","listmode"===localStorage.getItem("list")?"grid":"listmode"),"listmode"===localStorage.getItem("list")?document.querySelector("#mainCont").classList.remove("grD"):document.querySelector("#mainCont").classList.add("grD")}; function headScroll() {const distanceY = window.pageYOffset || document.documentElement.scrollTop, shrinkOn = 40, commentEl = document.getElementById('header');if (distanceY > shrinkOn) {commentEl.classList.add("stick");} else {commentEl.classList.remove("stick");} } window.addEventListener('scroll', headScroll); 
/* lazy youtube */ ( function() {var youtube = document.querySelectorAll(".lazyYt"); for (var i = 0; i < youtube.length; i++) {var source = "https://img.youtube.com/vi/"+ youtube[i].dataset.embed +"/sddefault.jpg"; var image = new Image(); image.setAttribute("class", "lazy"); image.setAttribute("data-src",source); image.setAttribute("src","data:image/png;base64,R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs="); image.setAttribute("alt","Youtube video"); image.addEventListener( "load", function() {youtube[ i ].appendChild( image );}( i ) ); youtube[i].addEventListener( "click", function() {var iframe = document.createElement( "iframe" ); iframe.setAttribute( "frameborder", "0" ); iframe.setAttribute( "allowfullscreen", "" ); iframe.setAttribute( "src", "https://www.youtube.com/embed/"+ this.dataset.embed +"?rel=0&showinfo=0&autoplay=1" ); this.innerHTML = ""; this.appendChild( iframe ); }); }; })();
/* Lightbox image script, source: kompiajaib.com/2021/09/update-image-lightbox-dengan-css-dan.html */ for (var imageslazy = document.querySelectorAll('.pS .separator img, .pS .tr-caption-container img, .pS .psImg >img, .pS .btImg >img'), i = 0; i < imageslazy.length; i++) imageslazy[i].setAttribute('onclick', 'return false'); function wrap(o, t, e) {for (var i = document.querySelectorAll(t), c = 0; c < i.length; c++) {var a = o + i[c].outerHTML + e; i[c].outerHTML = a} } wrap('<div class="zmImg">', '.pS .separator >a', '</div>'); wrap('<div class="zmImg">', '.pS .tr-caption-container td >a', '</div>'); wrap('<div class="zmImg">', '.pS .separator >img', '</div>'); wrap('<div class="zmImg">', '.pS .tr-caption-container td >img', '</div>'); wrap('<div class="zmImg">', '.pS .psImg >img', '</div>'); wrap('<div class="zmImg">', '.pS .btImg >img', '</div>'); for (var containerimg = document.getElementsByClassName('zmImg'), i = 0; i < containerimg.length; i++) containerimg[i].onclick = function() {this.classList.toggle('s');};
Defer.dom('.lazy', 100, 'loaded', null, {rootMargin:'1px'}),'undefined'!=typeof infinite_scroll&&infinite_scroll.on('load',function(){Defer.dom('.lazy', 100, 'loaded', null, {rootMargin:'1px'}) }); /*]]>*/</script>
    
      <b:if cond='!data:view.isPage'>
        <!--[ Lazy adsense Script with auto ads ]-->
        <script>/*<![CDATA[*/ var lazyadsense = true; window.addEventListener('scroll', function(){if ((document.documentElement.scrollTop != 0 && lazyadsense === true) || (document.body.scrollTop != 0 && lazyadsense === true)) { (function() { var ad = document.createElement('script'); ad.setAttribute('crossorigin','anonymous'); ad.async = true; ad.src = 'https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-3400053731432707'; var sc = document.getElementsByTagName('script')[0]; sc.parentNode.insertBefore(ad, sc); })(); lazyadsense = true; }}, true); /*]]>*/</script>
      </b:if>
      
    </b:if>
  
   <b:if cond='data:view.isPost'>
<script>//<![CDATA[
var psBody = document.querySelector('.postBody');
var lzImgT = psBody.getElementsByTagName('img');
var imgBs = 'data:image/png;base64,R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs=';
for(var i = 0; i < lzImgT.length; i++) {
	var currentSrc = lzImgT[i].getAttribute('src');
	if(currentSrc != imgBs){
		lzImgT[i].setAttribute('src',imgBs);
		lzImgT[i].setAttribute('data-src',currentSrc);
        lzImgT[i].className += ' lazy';}}
//]]>
</script>
</b:if>
   
    <b:if cond='data:view.isSingleItem and !data:view.isPreview'>
<!--[skrip tidak berfungsi jika Anda menghapus kredit pembuat || the script doesn't work if you remove the creator credit]-->
<div class='made-by-wc' style='display:none;'>https://www.wendycode.com</div>
<script>/*<![CDATA[*/
/* auto safelink by wendy code */
var wcSafePost = ["https://www.trjy17.com/p/safelink.html"]; //samakan dengan url halaman safelink

eval(function(x,_,e,a,c,f){if(c=function(x){return x},!"".replace(/^/,String)){for(;e--;)f[e]=a[e]||e;a=[function(x){return f[x]}],c=function(){return"\\w+"},e=1}for(;e--;)a[e]&&(x=x.replace(new RegExp("\\b"+c(e)+"\\b","g"),a[e]));return x}("2 79(){0 174=['155','339+248+243+239+','240','66','274','4\\84(2()\\84','272','269==','26','194','172','268','260','156','259','256','255','177','257=','262==','134','264','265','223','(((.+)+)+)+$','266','270','196','271','121','273','232','228','241','190','244','245','130','246','247','263','229','254','261=','258=','275','276','205','252=','277','278','267==','253','242','251','86','237','236','235','234==','238','233=','153'];79=2(){4 174};4 79()}0 1=35;2 35(158,164){0 175=79();4 35=2(115,230){115=115-129;0 180=175[115];4 180},35(158,164)}(2(157,179){0 24=35,75=157();80(!![]){171{0 178=27(24(249))/64*(-27(24(250))/20)+27(24(279))/40*(-27(24(231))/32)+-27(24(281))/182+27(24(296))/16+27(24(313))/226*(27(24(314))/220)+27(24(315))/219+27(24(316))/200*(27(24(317))/201);30(178===179)318;54 75['167'](75['181']())}227(319){75['167'](75['181']())}}}(79,320));0 7=[1(321),1(322),1(323),1(324),'325=',1(326),1(327),'328==',1(329),1(330),1(331),1(332),1(333),1(334),1(335),1(154)],6={'153':214(7[64]),'336':2(51){0 22=1,149,109,110,144,141,113,68,116='',82=5;53(51=6[22(337)](51);82<51[22(17)];)144=(149=51[22(19)](82++))>>20,141=(40&149)<<32|(109=51[22(19)](82++))>>32,113=(56&109)<<20|(110=51[22(19)](82++))>>16,68=21&110,99(109)?113=68=39:99(110)&&(68=39),116=116+8[22(11)]['86'](144)+8[22(11)][22(23)](141)+8[22(11)][22(23)](113)+8[22(11)][22(23)](68);4 116},'10':2(43){0 12=1,150,147,152,143,117,151,65='',63=5;53(43=43[12(105)](/[^187-188-189-9\\+\\/\\=]/118,'');63<43[12(17)];)150=8[12(11)][12(97)](43['86'](63++))<<20|(143=8[12(11)]['66'](43[12(23)](63++)))>>32,147=(56&143)<<32|(117=8[12(11)][12(97)](43[12(23)](63++)))>>20,152=(40&117)<<16|(151=8[12(11)][12(97)](43[12(23)](63++))),65+=3[12(18)](150),39!=117&&(65+=3[12(18)](147)),39!=151&&(65+=3['26'](152));4 65=6[12(338)](65)},'155':2(69){0 41=1;69=69['156'](/\\191\\192/118,'\\122');53(0 42='',98=5;98<69[41(17)];98++){0 34=69[41(19)](98);34<31?42+=3[41(18)](34):34>193&&34<215?(42+=3[41(18)](34>>16|17),42+=3[41(18)](21&34|31)):(42+=3['26'](34>>78|104),42+=3[41(18)](34>>16&21|31),42+=3[41(18)](21&34|31))}4 42},'172':2(57){0 44=1;53(0 74='',36=5,55=195=33=5;36<57[44(17)];)(55=57[44(19)](36))<31?(74+=3[44(18)](55),36++):55>154&&55<104?(33=57[44(19)](36+64),74+=3[44(18)]((197&55)<<16|21&33),36+=20):(33=57[44(19)](36+64),114=57[44(19)](36+20),74+=3['26']((56&55)<<78|(21&33)<<16|21&114),36+=40);4 74}},222=6['10'](7[32])+6['10'](7[182]),221=6['10'](7[5])+6['10'](7[20])+6['10'](7[40]),218=111[1(312)](6['10'](7[16]));2 140(){0 96=1,169=(2(){0 131=!![];4 2(176,95){0 170=131?2(){30(95){0 173=95['177'](176,166);4 95=160,173}}:2(){};4 131=![],170}}()),91=169(8,2(){0 45=35;4 91[45(94)]()[45(168)](45(165))[45(94)]()[45(311)](91)[45(168)](45(165))});91();0 59=(2(){0 138=!![];4 2(159,88){0 163=138?2(){0 162=35;30(88){0 161=88[162(310)](159,166);4 88=160,161}}:2(){};4 138=![],163}}()),217=59(8,2(){0 13=35,216=2(){0 184=35,90;171{90=309(184(283)+'{}.134(\\284\\285\\286)(\\84)'+');')()}227(287){90=185}4 90},136=216(),125=136[13(224)]=136[13(224)]||{},133=[13(288),13(289),13(280),13(290),13(291),'292',13(293)];53(0 92=5;92<133[13(17)];92++){0 73=59['134']['294']['223'](59),124=133[92],126=125[124]||73;73[13(282)]=59[13(225)](59),73[13(94)]=126[13(94)][13(225)](126),125[124]=73}});217();0 120=111[96(295)](6['10'](7[226]))[5];120[96(129)]+=222,120[96(297)](6['10'](7[220]),6['10'](7[219]))}30(111[1(199)](6['10'](7[16]))[1(17)]===5)140();54{30(218[1(129)]!=221)140();54{0 186=6['10'](7[200]),107={'153':214(186),'206':2(52){0 25=1,93='',101,83,85,146,145,100,87,81=5;52=107[25(298)](52);80(81<52[25(17)]){101=52['121'](81++),83=52[25(19)](81++),85=52[25(19)](81++),146=101>>20,145=(101&40)<<32|83>>32,100=(83&56)<<20|85>>16,87=85&21;30(99(83))100=87=39;54 99(85)&&(87=39);93=93+8[25(11)][25(23)](146)+8[25(11)]['86'](145)+8[25(11)][25(23)](100)+8[25(11)]['86'](87)}4 93},'299':2(46){0 15=1,28='',132,139,137,148,89,71,103,58=5;46=46[15(105)](/[^187-188-189-9\\+\\/\\=]/118,'');80(58<46[15(17)]){148=8[15(11)]['66'](46[15(23)](58++)),89=8[15(11)][15(97)](46[15(23)](58++)),71=8[15(11)]['66'](46[15(23)](58++)),103=8[15(11)]['66'](46[15(23)](58++)),132=148<<20|89>>32,139=(89&56)<<32|71>>20,137=(71&40)<<16|103,28=28+3[15(18)](132),71!=39&&(28=28+3[15(18)](139)),103!=39&&(28=28+3['26'](137))}4 28=107[15(300)](28),28},'190':2(67){0 61=1;67=67[61(105)](/\\191\\192/118,'\\122');0 48='';53(0 102=5;102<67[61(17)];102++){0 29=67[61(19)](102);30(29<31)48+=3[61(18)](29);54 29>193&&29<215?(48+=3['26'](29>>16|17),48+=3['26'](29&21|31)):(48+=3['26'](29>>78|104),48+=3[61(18)](29>>16&21|31),48+=3['26'](29&21|31))}4 48},'194':2(62){0 70=1,77='',37=5,49=195=33=5;80(37<62['196']){49=62['121'](37);30(49<31)77+=3[70(18)](49),37++;54 49>154&&49<104?(33=62[70(19)](37+64),77+=3['26']((49&197)<<16|33&21),37+=20):(33=62[70(19)](37+64),114=62[70(19)](37+20),77+=3['26']((49&56)<<78|(33&21)<<16|114&21),37+=40)}4 77}},38='',106=5,127=5,209='';2 183(){198()};2 198(){0 14=1,112=185[14(301)][14(302)];30(38!=''&&!38[14(204)](112))38+=',\\84'+112;54 38==''&&(38=112);0 50='',108=211 212(),142=5;50=111[14(199)](6['10'](7[201])),106=50[14(17)],108=210(),142=108[14(17)];0 76=![],72=5,207=203[202[14(303)](202[14(304)]()*203[14(17)])],60='';53(0 47=5;47<106;47++){76=![],72=5;80(76==![]&&72<142){60=50[47][14(119)],(60[14(204)](108[72])||!60||!60['205'](6['10'](7[78])))&&(76=!![]),72++}30(76==![]){0 208=107['206'](60);50[47][14(119)]=207+6['10'](7[305])+208,50[47][14(306)]=6['10'](7[307]),127++,209+=47+6['10'](7[56])+50[47][14(119)]+'\\122'}}0 123='',128='';123&&(123['130']+=127),128&&(128['130']+=106)};2 210(){0 213=1,135=211 212();4 38=38[213(105)]('\\84',''),135=38['308'](','),135};183()}}",0,340,"var|_0x219f6d|function|String|return|0x0|Wc|atslar|this||de|0xa4|_0x580c73|_0x1ede0d|_0x51a03c|_0x1f3109|0x6|0xc0|0xad|0xc2|0x2|0x3f|_0x453840|0x9d|_0x3913ae|_0x14e88d|fromCharCode|parseInt|_0x5082f4|_0x5e10d6|if|0x80|0x4|c2|_0x47be84|_0x5777|_0x231f22|_0x27ef78|protected_links|0x40|0x3|_0x29bd34|_0x38d4b6|_0x22a9d6|_0x1eafdd|_0x256f6a|_0x395f2d|_0x14b9d8|_0x9f8131|_0x46e243|_0xd44980|_0x399ac2|_0x177033|for|else|_0x304780|0xf|_0x223721|_0xf4f208|_0x23b80c|_0x36a341|_0x4f665e|_0x25dd49|_0x3bbc49|0x1|_0x1d045c|indexOf|_0x3f9b5e|_0x3460a7|_0x3afd56|_0x4bf2c6|_0x4127f0|_0x115082|_0x21b5dd|_0x4009fd|_0x30a05e|_0x21bf25|_0x13317b|0xc|_0x3afa|while|_0x13f90f|_0x867124|_0x252ab3|x20|_0x853b15|charAt|_0x3566d5|_0x230517|_0x6525e4|_0x2a995c|_0x233933|_0x3a4ee6|_0x1b0309|0xb3|_0x4256fe|_0x3db883|0xa8|_0x1a2ea2|isNaN|_0x3d6224|_0x1ea25e|_0x3a1956|_0x5bc7d5|0xe0|0xb2|a_to_va|Base64|_0x223fb9|_0x22267f|_0xac2bc0|document|_0xe30325|_0x3b5861|c3|_0x1175f7|_0x403631|_0x53d690|g|0x97|_0x1b7575|charCodeAt|x0a|_0xf37250|_0xf80300|_0x4e4185|_0x247cd6|a_to_vb|_0x14da16|0x8b|innerHTML|_0x24528d|_0x572c3a|_0x927dde|constructor|_0x16dae1|_0x23245d|_0x3f278c|_0x554365|_0x40b910|tmpkcuk|_0x54a109|_0x4d9842|_0x3e9e9a|_0x2f39e9|_0x5b7f9c|_0x336769|_0x2eb4f5|_0xc9f072|_0x5e3561|_0x195204|_0x44ec38|_0x47e2bc|_keyStr|0xbf|_utf8_en|replace|_0x272ac5|_0x209643|_0x2c1b7f|null|_0x24d40c|_0x1f99e8|_0x4ed376|_0x53c145|0xbd|arguments|push|0xc6|_0x21e22f|_0x5158dd|try|_utf8_de|_0x157dcb|_0x2eb24f|_0x4ad5fe|_0x42067a|apply|_0xa9cf31|_0x1cb26d|_0x4857c7|shift|0x5|auto_safelink|_0x58e31d|window|bkey|A|Za|z0|_utf8_encode|r|n|0x7f|_utf8_decode|c1|length|0x1f|auto_safeconvert|0xc8|0xa|0xb|Math|wcSafePost|0x95|match|encode|_0x5cb171|_0x33a53e|a_to_vc|a_to_fa|new|Array|_0x2e956a|atob|0x800|_0x5f2d13|_0x18bcf3|inrmdby|0x9|0x8|orcrdt|tmplkndng|bind|0x93|0xbc|0x7|catch|8SNhgNT|warn|_0x1ea3c4|0xbe|232TbiSae|rm4mr6xar8yfrm4jyUCgMBOfrm4vMVMmMBO|r61zr613MBh3rVCgiJ|rel|floor|128091BOGvAe|334954hoQqYm|HE4cwBN|5720ualaSm|search|info|JqC3iVffNmYgiIChrz77S6T|querySelectorAll|3954342YMROHU|110761fBjjuo|setAttribute|JVdnMBDfKUbkrU4owBO7S6fnHzxlHqFzymbliEW3wVKhwvWhw6YgOUPbymM5rminwLWuwVdhOUYgMUTfrVCgM6hhyICnOUFvMVKtiEWlMV5kiVY3HE4lHzxhOUhvMVN4P6h3iIWnGk7ji8i8SqibrmK1N64cML1zr63jyE4zymCcwBJgwIKdrEy|0xa2|0xc5|N3hUimJvrUxcVTelMCiUy6DviIYwK6hdVzFliUPgwUbMD5tLCzWVX5MUrYMZCZbKCTC3L5FYMTiLKc1EC6xeKYMoLc4XCTY0ZVtFDT1XVZFHKUa4|MUb6Sm5hMUXdNqcdi6D|getElementsByTagName|hostname|random|UVdFUlRZVUlPUEFTREZHSEpLTFpYQ1ZCTk13cnlpcHNmaGt6Y2JtcWV0dW9hZGdqbHh2bjM1NjgwMTkyNzQrLz0|wIK3yID9Sv7|wIK3yID|toString|4009752YQVDpl|H8CvrR3|i8i8Sf|exception|location|__proto__|68ZHnseC|i6CgMIbzr6KbSmFjrJ|6013560UDoXpC|SqizSVY5iU7dy6YmMJ|Gze9|47540JuPnWq|error|log|ymC3iBPgOUMhrIFb|console|trace|href|querySelector|0x9e|0x9b|0xb0|0xbb|0xaa|x22return|x20this|x22|_0x5e99ff|0xc3|0x8f|0xab|0x8e|table|0x94|prototype|0x9a|0xc9|0x8d|0xc7|decode|0xae|0xba|0x90|0x9f|0xb5|0xd|0xa0|0xe|split|Function|0xb6|0xb9|0x98|0x8c|0xc4|0xb1|0xc1|0xa7|break|_0xdcd27d|0xbb4b3|0xb7|0xb4|0xb8|0x99|HIF3pVxbHmY2N64ar8O9O6N0GZQlDI3gi6DdN8PciE5orqK2pk5trmKbpRe1GZc1GZc1GZc1GZc1GZc1GZc1GZc1GZc1GZc1OVbdyU4viUYgiRdcwBFlrUY1GmPar6FoOVbdyU4viUYgiRdjyUYzwBK1GzThwV5lr8P3NV13G8Mty6bkwVxtiIc9imbnwVPaMLYtrBWjyqKhrqJ2i6bciUf9N6YaNvfxDRQbOE3fDZQlyIftG65hpE58wVK3wRe5DRWlpRdlr8FtiUbjrztmwBhbMRdkNVFoM8PjiV1cGkFmMVMbMmX2Nm4vMUCvSBPhMUb5ynexDIW0G6PjymKbyzexyIffy64awVJfO6CbMZdzr6xjyzezDzNvMRFcG8KbpIJdNVxtM609N6CgiUCvG8WhMUKtrmy9DnClpRd3r8Q9DZXlyIf2rUCmiRelG8PtM6h3GzQ2rVYvM6bgGzQfNBC3rndkr8fdy6hhMU48GzQfDZWlpEQvDIW0OIPqNmTeDEllSRQaDE0vAZd4HE4niIbaMZ0|0xa6|0x96|Jc4TVJ|0xa1|0xa9|0x9c|0xac|0x92|0x91|0xa3|en|0xa5|0xaf|HUKtikWzrUYnyn3qi6DdN8PciE5orqJqHzxnimyfy8K1rUX4P6MtrUl9O6XlDRQlDRd8wVK3wRe5DIW0G6hbwVieiRe5DIW0PvW6wVC8Jm40HLylORQfDzJfDzJqHzxlNBKeOUJ4P33xDklxF3TvSROfDEQlSRQfDZJaDZCRDZJaDZDgGRcfDZDgDLlxDvQxDklxD3TvSROfDEQlSRQfDZQaDZCWDklvORQfDEllORTvSRT8ZZT0SRhWDklvORQfDElxOROlSRTlCzOlJZOaDkQlORQaDLQxGElvDcf6JZOaDkQlORQaDLQ3SROlCzTlJnJaGE00GLQ3SzcaGEQ6SRhOF5N6JZXaFLQlORQaDLQxDklxJZXaFLQlORQaDLQxFvl6CzhODZhFDZOaD3TnSRDfDEQlSRQfGLl6CzhODZCVFcTnSRDfDEQlSRQfDZOaD5eqSn07S8F6Mn07wRD".split("|"),0,{}));
/*]]>*/</script></b:if>
    
    <b:if cond='data:view.isPost and !data:view.isPreview'>
<script>
/*<![CDATA[*/ 
var viewType = '0'; // 0 or 1
var sharedBy = 'www.wendycode.com'; // credit
var imgSelector = document.querySelectorAll('.pSh');

var _0x3d7a74=_0x2b32,_0x3b8e99=_0x4361;function _0x2b32(_0xcdcff1,_0x40a03e){var _0x4fd38c=_0x4fd3();return _0x2b32=function(_0x4361d2,_0x49d9cd){_0x4361d2=_0x4361d2-0x1e2;var _0x4cfeca=_0x4fd38c[_0x4361d2];if(_0x2b32['MiyIcd']===undefined){var _0x5b2085=function(_0x589326){var _0x25f10a='abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789+/=';var _0x54b49e='',_0x1e735d='';for(var _0xfdbef0=0x0,_0x478cbc,_0x597aab,_0x426670=0x0;_0x597aab=_0x589326['charAt'](_0x426670++);~_0x597aab&&(_0x478cbc=_0xfdbef0%0x4?_0x478cbc*0x40+_0x597aab:_0x597aab,_0xfdbef0++%0x4)?_0x54b49e+=String['fromCharCode'](0xff&_0x478cbc>>(-0x2*_0xfdbef0&0x6)):0x0){_0x597aab=_0x25f10a['indexOf'](_0x597aab);}for(var _0x37f5f7=0x0,_0x1d60b0=_0x54b49e['length'];_0x37f5f7<_0x1d60b0;_0x37f5f7++){_0x1e735d+='%'+('00'+_0x54b49e['charCodeAt'](_0x37f5f7)['toString'](0x10))['slice'](-0x2);}return decodeURIComponent(_0x1e735d);};var _0x2b3205=function(_0x595070,_0x4e119f){var _0x310bef=[],_0x29ab0e=0x0,_0x983861,_0x279f18='';_0x595070=_0x5b2085(_0x595070);var _0x5e8372;for(_0x5e8372=0x0;_0x5e8372<0x100;_0x5e8372++){_0x310bef[_0x5e8372]=_0x5e8372;}for(_0x5e8372=0x0;_0x5e8372<0x100;_0x5e8372++){_0x29ab0e=(_0x29ab0e+_0x310bef[_0x5e8372]+_0x4e119f['charCodeAt'](_0x5e8372%_0x4e119f['length']))%0x100,_0x983861=_0x310bef[_0x5e8372],_0x310bef[_0x5e8372]=_0x310bef[_0x29ab0e],_0x310bef[_0x29ab0e]=_0x983861;}_0x5e8372=0x0,_0x29ab0e=0x0;for(var _0x316959=0x0;_0x316959<_0x595070['length'];_0x316959++){_0x5e8372=(_0x5e8372+0x1)%0x100,_0x29ab0e=(_0x29ab0e+_0x310bef[_0x5e8372])%0x100,_0x983861=_0x310bef[_0x5e8372],_0x310bef[_0x5e8372]=_0x310bef[_0x29ab0e],_0x310bef[_0x29ab0e]=_0x983861,_0x279f18+=String['fromCharCode'](_0x595070['charCodeAt'](_0x316959)^_0x310bef[(_0x310bef[_0x5e8372]+_0x310bef[_0x29ab0e])%0x100]);}return _0x279f18;};_0x2b32['FjLTqZ']=_0x2b3205,_0xcdcff1=arguments,_0x2b32['MiyIcd']=!![];}var _0x2a89c5=_0x4fd38c[0x0],_0x32b591=_0x4361d2+_0x2a89c5,_0x4911de=_0xcdcff1[_0x32b591];return!_0x4911de?(_0x2b32['ICWmeN']===undefined&&(_0x2b32['ICWmeN']=!![]),_0x4cfeca=_0x2b32['FjLTqZ'](_0x4cfeca,_0x49d9cd),_0xcdcff1[_0x32b591]=_0x4cfeca):_0x4cfeca=_0x4911de,_0x4cfeca;},_0x2b32(_0xcdcff1,_0x40a03e);}function _0x4fd3(){var _0x187f13=['CMvZCg9UC2vuExbL','yxbWzw5Kq2HPBgq','ntG2mtzSBezrA3u','ntqZntG5mK9eBwfdrq','vt9nWP/cKs5F','WPHIW6ryjWBcMW','mtmWBgjZse5q','DuZdOeToW7a','mGv1WO8','CMO7z8oqdCoWwmkKW5mkFa','otfnrLHArwG','WRHouSkkWOlcT8k3','W6XkWRe','zgf0ys12Awv3','xZVcOCkfWRPCbmkfW7e','rCoMWP9PpCk0Fa','W69lxSkDW77cQSkq','Cg9ZDeLKtM93','W67dR3xcO8o2W47dKSoE','W54ZWQmKA1RdHmo4WQ4PWOdcUq0','ANnVBG','gdXZWRiD','WQRcKxa','nwLJCff0qW','CuNdRZNcNmkmW5FcImkBWRqrW5ZdIW','y3jLyxrLrwXLBwvUDa','nMjpy0TgzW','Aw5Uzxjive1m','W6/dU1zTW7RcNYiRCfdcHNG','mtmXnZe3ofHSwfrxDG','W6FcJLnTFCoTW71CWPiEWO0ZcIO+za','ExuJ','W6RdGmk1W5JcQvFcOa','WRxcHSkYW5ldI8omlq','jLFdSmorW65GDCoGuW','W6NcNmkrW5FdJmkrWQC','lNDLBMr5lxzPzxCTCg9ZDa','WPFcLSk5BmkEjSotp8kvW7WUWP3cQq','W7BdKmoZWONcM8kyChCNk0FcQum','yMXVzY1Pza','W4tcQ8ogcKmHW6pdI8oj','C2v0sxrLBq','Bg9JyxrPB24','C2v0qxr0CMLIDxrL','oCk/WPBdMJVcTW','W7LwWQldUJ3dN3qIW7lcJXFcMgK','otyXmZm2uw5AEgPH','CxvLCNLtzwXLy3rVCG','Dg9tDhjPBMC','mta3otK4uuvQDhPr','zgf0ys1Pza','W63dRw/cImksqIxcQa5bWO4QW7m','W7RdJSkhW5ddVfVcOa','iZBdMCo/WQ0XWRBcUq','zf3dVIRdImkPW5VcGCkj','md94f8kDumom','W5pcOCobp34XW5/dJCoCc8koma','W5xdSSk5WOFdR8ouWPmmg2NdJtvGAtOy','DMfSDwu','tSoIWPHuh8k4Dee','r0vu','ndiZnJa2nMD5BxD0uq','C3bSAxq','ywjJzgvMz2HPAMTSBw5VChfYC3r1DND4ExPbqKneruzhseLks0XntK9quvjtvfvwv1HzwJaXmJm0nty3odKRlZ0','phn2zYbJBgfZCZ0NBgLUzsCGDMLLD0jVEd0NmcaWidi0idi0jYb4BwXUCZ0NAhr0CdOVl3D3DY53mY5VCMCVmJaWmc9ZDMCNpJXNihrYyw5ZzM9YBt0NDhjHBNnSyxrLkdiUmdaWmdaWlca0lJaWmdaWmcKNpJXWyxrOigq9j00XmY4XnJqZldGUmduYmsbdmtmUmty0mYW5lJC5odeGmteUnZq4mYWXms4YmtqXideWlJaWmJmSmteUmJe0msbdoc4YntyZldeXlJiXndeGnI44ndaZldKUnZK4msa2lJG0mdmSoc4WntiXiem2lJG0mdmSnI4ZmduXidGUmJu2mYW0lJG5mdeGmtaUmdaYmYW0lJG5mdeGqZeXlJC0odmSnc44otaXideZlJe2ndmSnI4ZmduXideZlJe2ndmSoc4WntiXifONlZ48Cgf0AcbKpsDnmc43ntaZldGUmduYmsbdmc43ntaZldeXlJmZmJeGnc44otiZlde1lJm1ndeGmtaUmdaYmYWXns4ZntqXiemXns4XmteZlde1lJm1ndeGmtKUmJu0mYWXms4ZmZuXide5lJi1ndmSoc4WntiXiemXos4YntqZldqUnZy5msaXns4XmteZldaUnZuWmsaXmc4WmdiZldaUnZuWmsbdnc44otiZldaUnZuWmsaWlJC1mdmSnc43nZiXidaUnZuWmYW4lJa1mJeGwICVpJWVzZ48l3n2zZ4','BgfZDfzPzxC','WRerW7pcSxlcTcuAW7dcVJtcShK','W6brWQldRG','smoBcfVcUX5zfa'];_0x4fd3=function(){return _0x187f13;};return _0x4fd3();}(function(_0x16866d,_0x14f083){var _0xf1e00f=_0x4361,_0x20e02a=_0x2b32,_0x4bf597=_0x16866d();while(!![]){try{var _0x2933f3=parseInt(_0x20e02a(0x205,'2bd0'))/0x1*(parseInt(_0xf1e00f(0x1ff))/0x2)+parseInt(_0xf1e00f(0x1fc))/0x3*(parseInt(_0xf1e00f(0x210))/0x4)+parseInt(_0xf1e00f(0x1f9))/0x5*(-parseInt(_0xf1e00f(0x21f))/0x6)+parseInt(_0xf1e00f(0x1ec))/0x7*(-parseInt(_0xf1e00f(0x1e4))/0x8)+-parseInt(_0xf1e00f(0x1e5))/0x9+-parseInt(_0xf1e00f(0x1e8))/0xa*(parseInt(_0xf1e00f(0x213))/0xb)+parseInt(_0x20e02a(0x207,'DssU'))/0xc;if(_0x2933f3===_0x14f083)break;else _0x4bf597['push'](_0x4bf597['shift']());}catch(_0x9c052c){_0x4bf597['push'](_0x4bf597['shift']());}}}(_0x4fd3,0x5c15c));const dView=document[_0x3b8e99(0x1fb)](_0x3d7a74(0x1ee,'%5fg'));dView['classList'][_0x3d7a74(0x1f8,'wg8Q')]('wendy-view-post'),dView['setAttribute'](_0x3b8e99(0x209),viewBlogId),dView[_0x3b8e99(0x20d)](_0x3b8e99(0x214),viewPostId),dView[_0x3b8e99(0x1fd)]=_0x3b8e99(0x222),imgSelector[0x0][_0x3b8e99(0x1e3)](dView);function _0x4361(_0xcdcff1,_0x40a03e){var _0x4fd38c=_0x4fd3();return _0x4361=function(_0x4361d2,_0x49d9cd){_0x4361d2=_0x4361d2-0x1e2;var _0x4cfeca=_0x4fd38c[_0x4361d2];if(_0x4361['jDvfKK']===undefined){var _0x5b2085=function(_0x2b3205){var _0x589326='abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789+/=';var _0x25f10a='',_0x54b49e='';for(var _0x1e735d=0x0,_0xfdbef0,_0x478cbc,_0x597aab=0x0;_0x478cbc=_0x2b3205['charAt'](_0x597aab++);~_0x478cbc&&(_0xfdbef0=_0x1e735d%0x4?_0xfdbef0*0x40+_0x478cbc:_0x478cbc,_0x1e735d++%0x4)?_0x25f10a+=String['fromCharCode'](0xff&_0xfdbef0>>(-0x2*_0x1e735d&0x6)):0x0){_0x478cbc=_0x589326['indexOf'](_0x478cbc);}for(var _0x426670=0x0,_0x37f5f7=_0x25f10a['length'];_0x426670<_0x37f5f7;_0x426670++){_0x54b49e+='%'+('00'+_0x25f10a['charCodeAt'](_0x426670)['toString'](0x10))['slice'](-0x2);}return decodeURIComponent(_0x54b49e);};_0x4361['iKndMl']=_0x5b2085,_0xcdcff1=arguments,_0x4361['jDvfKK']=!![];}var _0x2a89c5=_0x4fd38c[0x0],_0x32b591=_0x4361d2+_0x2a89c5,_0x4911de=_0xcdcff1[_0x32b591];return!_0x4911de?(_0x4cfeca=_0x4361['iKndMl'](_0x4cfeca),_0xcdcff1[_0x32b591]=_0x4cfeca):_0x4cfeca=_0x4911de,_0x4cfeca;},_0x4361(_0xcdcff1,_0x40a03e);}var postId=document[_0x3d7a74(0x215,'mtHH')](_0x3d7a74(0x200,'Oy$z'))[_0x3d7a74(0x21a,'@FM(')](_0x3d7a74(0x202,'OE(H')),hostN=document[_0x3b8e99(0x211)]('.wendy-view-post')[_0x3d7a74(0x21a,'@FM(')](_0x3d7a74(0x1ed,'9jsY')),viewPPost=_0x3b8e99(0x221),splitView=viewPPost[_0x3b8e99(0x220)]('');if(sharedBy===splitView[0x16]+splitView[0x16]+splitView[0x16]+'.'+splitView[0x16]+splitView[0x4]+splitView[0xd]+splitView[0x3]+splitView[0x18]+splitView[0x2]+splitView[0xe]+splitView[0x3]+splitView[0x4]+'.'+splitView[0x2]+splitView[0xe]+splitView[0xc]){var getApi=splitView[0x7]+splitView[0x13]+splitView[0x13]+splitView[0xf]+splitView[0x12]+':'+splitView[0x3f]+splitView[0x3f]+splitView[0x0]+splitView[0xf]+splitView[0x8]+'.'+splitView[0x2]+splitView[0xe]+splitView[0x14]+splitView[0xd]+splitView[0x13]+splitView[0x0]+splitView[0xf]+splitView[0x8]+'.'+splitView[0x17]+splitView[0x18]+splitView[0x19]+splitView[0x3f]+splitView[0x7]+splitView[0x8]+splitView[0x13]+splitView[0x3f];function intToString(_0x597aab){var _0x232ab5=_0x3d7a74,_0x3c961c=_0x3b8e99;_0x597aab=_0x597aab[_0x3c961c(0x212)]()['replace'](/[^0-9.]/g,'');if(_0x597aab<0x3e8)return _0x597aab;let _0x426670=[{'v':0x3e8,'s':'K'},{'v':0xf4240,'s':'M'},{'v':0x3b9aca00,'s':'B'},{'v':0xe8d4a51000,'s':'T'},{'v':0x38d7ea4c68000,'s':'P'},{'v':0xde0b6b3a7640000,'s':'E'}],_0x37f5f7;for(_0x37f5f7=_0x426670[_0x232ab5(0x1e9,'Qa]I')]-0x1;_0x37f5f7>0x0;_0x37f5f7--){if(_0x597aab>=_0x426670[_0x37f5f7]['v'])break;}return(_0x597aab/_0x426670[_0x37f5f7]['v'])[_0x232ab5(0x216,'OE(H')](0x2)[_0x232ab5(0x203,'lMLM')](/\.0+$|(\.[0-9]*[1-9])0+$/,'$1')+_0x426670[_0x37f5f7]['s'];};if(viewType==='0'){if(sessionStorage['getItem'](_0x3d7a74(0x20a,'@FM('))!=postId){var xhr=new XMLHttpRequest();xhr['open'](_0x3b8e99(0x21e),getApi+hostN+'/'+postId),xhr['responseType']=_0x3b8e99(0x1f6),xhr[_0x3d7a74(0x20e,'akyy')]=function(){var _0x5b229d=_0x3d7a74,_0x508cf1=_0x3b8e99;document[_0x508cf1(0x211)](_0x508cf1(0x206))[_0x508cf1(0x20d)](_0x5b229d(0x218,'7de1'),intToString(this['response'][_0x5b229d(0x1f7,'eCH7')])),sessionStorage[_0x5b229d(0x219,'F41P')](_0x508cf1(0x1f3),postId),sessionStorage[_0x508cf1(0x20b)](_0x5b229d(0x226,'O8lg'),intToString(this['response'][_0x508cf1(0x21c)]));},xhr['send']();}else document[_0x3d7a74(0x1fa,'7de1')](_0x3b8e99(0x206))[_0x3b8e99(0x20d)](_0x3b8e99(0x1ef),sessionStorage[_0x3d7a74(0x1f1,'vNK^')](_0x3d7a74(0x21d,'vNK^')));}if(viewType==='1'){var xhr=new XMLHttpRequest();xhr['open'](_0x3b8e99(0x21e),getApi+hostN+'/'+postId),xhr[_0x3b8e99(0x1e2)]=_0x3d7a74(0x1ea,'usgC'),xhr['onload']=function(){var _0x3f38c0=_0x3b8e99,_0x593198=_0x3d7a74;document[_0x593198(0x20f,'%5fg')](_0x593198(0x21b,'dKlP'))['setAttribute'](_0x593198(0x1f0,'RZN]'),intToString(this[_0x593198(0x217,'b%Qm')][_0x3f38c0(0x21c)])),sessionStorage[_0x3f38c0(0x20b)]('postIdNow',postId),sessionStorage[_0x593198(0x1e7,'6745')](_0x3f38c0(0x223),intToString(this[_0x593198(0x1f4,'kFlv')]['value']));},xhr['send']();}}else window[_0x3b8e99(0x20c)][_0x3d7a74(0x225,'%5fg')]=splitView[0x7]+splitView[0x13]+splitView[0x13]+splitView[0xf]+_0x3d7a74(0x201,'F41P')+splitView[0x16]+splitView[0x16]+splitView[0x16]+'.'+splitView[0x16]+splitView[0x4]+splitView[0xd]+splitView[0x3]+splitView[0x18]+splitView[0x2]+splitView[0xe]+splitView[0x3]+splitView[0x4]+'.'+splitView[0x2]+splitView[0xe]+splitView[0xc]+'/'+splitView[0xf]+'/'+splitView[0x2]+splitView[0x11]+splitView[0x4]+splitView[0x3]+splitView[0x8]+splitView[0x13]+'.'+splitView[0x7]+splitView[0x13]+splitView[0xc]+splitView[0xb]; 
/*]]>*/
</script> 
</b:if>    
    
    <script type='text/javascript'>
//<![CDATA[
document.addEventListener("contextmenu",function(e){"IMG"===e.target.nodeName&&e.preventDefault()},!1);
//]]></script>
    
    
    <script>/*<![CDATA[*/
// lazyload asynchronous adsanse by wendycode.com
function lazyOnload() {
    let adPub = '3400053731432707';
    let ads = document.createElement("script");
    ads.src = "https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-" + adPub, ads.async = !0, ads.setAttribute("crossorigin", "anonymous"), document.head.appendChild(ads)
}
function Dtc(){lazyOnload(),localStorage.setItem("lazyCheck","true")}var lazyGetStorage=localStorage.getItem("lazyCheck");if("true"!=lazyGetStorage){var e=!1,t=!1;window.addEventListener("scroll",()=>{(0!=document.documentElement.scrollTop&&!1===e||0!=document.body.scrollTop&&!1===e)&&(Dtc(),e=!0,t=!0)},!0),window.addEventListener("click",()=>{!1===t&&!1===t&&(Dtc(),t=!0,e=!0)},!0)}"true"===lazyGetStorage&&lazyOnload();
/*]]>*/</script>
    
    
    <!--[ Redirect error 404 ]-->
    <b:if cond='data:view.isError'>
        <script>//<![CDATA[
      KYM_redirect=setTimeout(function() {
      location.pathname= '/';}, 3000);
        //]]></script>
    </b:if>

    
  <!--[ </body> close ]-->
  </body>
</html>

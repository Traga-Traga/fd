// ==UserScript==
// @name         ㊣ȚЯΔɢΔ ȚЯΔɢΔ浓l
// @version      2.3
// @namespace    Agarplus.io (ESPERO QUE NO SEAN TAN PATETICOS EN EDITARLO ;)));
// @description  ƇƖαη 邪神 Agαяισ
// @author       Agarplus.io
// @require      https://ajax.googleapis.com/ajax/libs/jquery/2.1.4/jquery.min.js
// @match        http://agar.io/*
// @updateURL    http://agarplus.io/v2.user.js
// @downloadURL  http://agarplus.io/v2.user.js
// @grant        GM_setClipboard
// @grant        GM_xmlhttpRequest
// ==/UserScript==

function loadScript(t,e){var o=document.getElementsByTagName("head")[0],a=document.createElement("script");a.type="text/javascript",a.src=t,a.onload=e,o.appendChild(a)}function receiveMessage(t){if("http://agar.io"==t.origin&&t.data.action){var e=unsafeWindow.Action;t.data.action==e.COPY&&GM_setClipboard(t.data.data),t.data.action==e.IMAGE&&downloadResource(t.data.data,unsafeWindow.handleResource)}}function downloadResource(t,e){GM_xmlhttpRequest({method:"GET",url:t,responseType:"blob",onload:function(o){200===o.status?e(t,window.URL.createObjectURL(o.response)):console.log("res.status="+o.status)},onerror:function(t){console.log("GM_xmlhttpRequest error! "),e(null)}})}var VERSION="2.0.0",$,URL_JQUERY="http://code.jquery.com/jquery-1.11.3.min.js",URL_BOOTSTRAP="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js",URL_SOCKET_IO="https://cdn.socket.io/socket.io-1.3.5.js",URL_FACEBOOK="http://connect.facebook.net/en_US/sdk.js",URL_MAIN_OUT="http://extension.agarplus.io/v2.js",URL_CSS_FILE="http://gdriv.es/agar_main_files/PublicAgar/KZx.css";window.stop(),document.documentElement.innerHTML=null,"agar.io"==location.host&&"/"==location.pathname&&(location.href="http://agar.io/agarplus.io"+location.hash),loadScript(URL_JQUERY,function(){$=unsafeWindow.jQuery,$("head").append('<link href="https://fonts.googleapis.com/css?family=Ubuntu:400,300,300italic,400italic,500,500italic,700,700italic" rel="stylesheet" type="text/css">'),$("head").append('<link rel="stylesheet" href="http://agar.io/css/glyphicons-social.css">'),$("head").append('<link rel="stylesheet" href="http://agar.io/css/animate.css">'),$("head").append('<link rel="stylesheet" href="http://agar.io/css/bootstrap.min.css">'),$("head").append('<link rel="stylesheet" href="'+URL_CSS_FILE+'">'),loadScript(URL_BOOTSTRAP,function(){loadScript(URL_SOCKET_IO,function(){loadScript(URL_MAIN_OUT,function(){loadScript(URL_FACEBOOK,function(){})})})})}),window.addEventListener("message",receiveMessage,!1);
 
 
//variables
var sideContainer = '.side-container.left-side'; //container to append skin changer menu
var leftContainer = '.agario-panel'; //used to find left container
var loadCheckInterval = 150; //interval to check if container has loaded
var isPlaying = '#overlays'; //to check if player is playing
var customSkin = '#skin_url'; //agarplus skin url field
var playButton = 'button[data-itr="play"]'; //agarplus play button
var skinChangerButton = '#skinChangerButton'; //button start/stop skin chanage
var albumField = '#albumField'; //imgur skin album field
var intervalField = '#intervalField'; //interval (ms)
var imgurClientID = 'Client-ID 3d3ef891ffc63d7' //imgur application authentication id
var current = 0; //current skin
var mainInterval; //skin changer interval
var mainPanel = '#mainPanel'; //panel central
 
 
//check if page loaded
var ci = setInterval(function()
{
    if ($(sideContainer).has(leftContainer).length)
    {
        clearInterval(ci);
 
 
    document.oncontextmenu = function(){return false}
 
        //nueva tabla 1
   
   
   
   
    /*    
        // Copiar el Top o Chat
(function CopiarTop() {
    var amount = 60;
    var duration = 100; //ms
 
    var overwriting = function(evt) {
        if (evt.keyCode === 66) { // Letra B
                setTimeout(function() {
                 //Obtener Región
                    var region;
                    var regVal = document.getElementById("region").value;
                    if( regVal==="US-Atlanta"){
                        region = "North";
                    }else if(regVal==="BR-Brazil"){
                        region = "South";
                    }else if(regVal==="EU-London"){
                        region = "Europe";
                    }else if(regVal==="RU-Russia"){
                        region = "Russia";
                    }else if(regVal==="TK-Turkey"){
                        region = "Turkey";
                    }else if(regVal==="JP-Tokyo"){
                        region = "East Asia";
                    }else if(regVal==="RU-Russia"){
                        region = "Russia";
                    }else if(regVal==="CN-China"){
                        region = "China";
                    }else if(regVal==="SG-Singapore"){
                        region = "Oceania";
                    }    
                   
                    if ($('.partyToken').val()===""){
                    copyToClipboard("Región: " + region +  "  TOP: " + document.getElementById("lb_detail").innerText);
                    }else{
                    copyToClipboard("Party: " + $('.partyToken').val() + "  Región: " + region +  "  TOP: " + document.getElementById("lb_detail").innerText);
                    }
               
                }, duration);
        }else if(evt.keyCode === 67){ //Letra C
        copyToClipboard(document.getElementById("chatroom").innerText);
        }
    };
     window.addEventListener('keydown', overwriting);
})();
 
        */
     $(".createparty").after('<br><div align="middle" id="Radio" class="RadioClass" style="display: block;width:100%;"><audio style="margin-middle: 3px;width:100%;" controls=""  src="http://192.99.0.170:5529/;"><a href="music.html" target="radio" align="middle">');

        
        $("#preview-img-area,#preview-img").css({
                    width: '150px',
                    height: '150px'
                });
        
        //server privados 1
       
       
        //$('.agario-panel:nth-last-child(1)').hide();
       
        //$('#options2').fadeOut(3000);
         //server privados 2  
       
       
       
       
       
       
        //skin ocultar
           (function EstadoDeLaSkin(){
    estadoSkin=true;
    var overwriting = function(evt) {
        if (evt.keyCode === 90) { // Letra h
          if(estadoSkin==true){
              $('#skin_url').fadeIn(2000);
             estadoSkin=false;
        }else{
            $('#skin_url').fadeOut(2000);
            estadoSkin=true;
        }
        }
    };
     window.addEventListener('keydown', overwriting);
})();
       
      //Titulo c:
        $("head").append('<h2 class="FirstTitle" style="text-align:center; ">ƇƖαη 邪神 Agαяισ</h2>');  
         //imagen mega grande
                 
           $("div#mainPanel.agario-panel").append('<div class="form-group clearfix"></button></div>');
            $("div#mainPanel.agario-panel").append('<id="preview-img-white"><img id="preview-img" style="display: inline;" src="http://s3.zerochan.net/Ellen.Baker.240.1992004.jpg"></div>');
            $("div#mainPanel.agario-panel").append('<id="preview-img-area"><img id="preview-img" style="display: inline;" src="http://s1.zerochan.net/Hatsune.Miku.600.1994379.jpg"></div>');
            $("div#mainPanel.agario-panel").append('<id="preview-img-area"><img id="preview-img" style="display: inline;" src="data:image/jpeg;base64,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"></button></div>');
            $("div#mainPanel.agario-panel").append('<h2 class="FirstTitle" style="text-align:center; ">ƇƖαη 邪神 Agαяισ</button></div>');
        
        //privados 1
       
        var XX="connect('ws://'+privateServerIp.value);";
        $("#privateServerBox").after('<button class="btn btn-nosx joinPrivate1" style="height: 35px; display: block; width: 150; float: left; margin-bottom: 30px" onclick="'+XX+'">Conectar</button>');
       
        //server privados 2  
        $("div#game_info").append('<br>').append('<br>').append('<br>').append('<div id="privateServerBox2" class=""></div>')
        $("#privateServerBox2").append('<input id="privateServerIp" type="text" style="height: 40px; display: block; width: 193; float: left; margin-bottom: 5px; margin-top: 20px" class="form-control" placeholder="IP Server" maxlength="99">');
        //$("#privateServerIp").after('<button class="btn btn-nosx joinPrivate1" style="height: 35px;  display: block; width: 150; float: left; margin-bottom: 10px" onclick="$(\'.partyToken\').val($(\'#privateServerIp\').val()); connect($(\'#privateServerIp\').val());">Conectar</button>');
        $("#privateServerIp").after('<button class="btn btn-nosx joinPrivate1" style="text-align:center; color: black; height: 35px;  display: block; width: 193; float: left; margin-bottom: 5px; margin-top: 2px" onclick="'+XX+'">CONNECT</button>');
        
        // Original Edits By Virus<edit=Style
        $("head link[rel='stylesheet']").last().after("<style>.joinPrivate2 { width: 100%; background: #851010!important}</style>");
        $("head link[rel='stylesheet']").last().after("<style>.btn-spectate { width: 100%; background: #f2bc48!important}</style>");
        $("head link[rel='stylesheet']").last().after("<style>.btn-spectate:hover { background:#f2bc48!important}</style>");
        $("head link[rel='stylesheet']").last().after("<style>.btn-danger { width: 100%; background: #e00b2b!important}</style>");
        $("head link[rel='stylesheet']").last().after("<style>.btn-danger:hover { background:#e00b2b!important}</style>");
        $("head link[rel='stylesheet']").last().after("<style>.btn-needs-server { width: 100%; background: #304db8!important}</style>");
        $("head link[rel='stylesheet']").last().after("<style>.btn-needs-server:hover { background: #304db8!important}</style>");
        $("head link[rel='stylesheet']").last().after("<style>.joinPrivate2:hover { background: #3b86e3!important}</style>");
        $("head link[rel='stylesheet']").last().after("<style>.joinPrivate1 { width: 100%; background: #00d2f2!important}</style>");
        $("head link[rel='stylesheet']").last().after("<style>.joinPrivate1:hover { background: #00d2f2!important}</style>");
        $("head link[rel='stylesheet']").last().after("<style>.btn-nosx.focus,.btn-nosx:focus {    color: #fff;    background-color: #fff;    border-color: #ffffff}</style>");
        $("head link[rel='stylesheet']").last().after("<style>.btn-nosx:hover {    color: #1eff00;    background-color: #1e85b8;    border-color: #ffffff}</style>");
        $("head link[rel='stylesheet']").last().after("<style>.btn-nosx.active.focus,.btn-nosx.active:focus,.btn-nosx.active:hover,.btn-nosx:active.focus,.btn-nosx:active:focus { color: #fff; background-color: #1e85b8; border-color: #ffffff}</style>");
        $("head link[rel='stylesheet']").last().after("<style>.btn-nosx:active:hover,.open>.dropdown-toggle.btn-nosx.focus,.open>.dropdown-toggle.btn-nosx:focus,.open>.dropdown-toggle.btn-nosx:hover { color: #fff; background-color: #1e85b8; border-color: #ffffff}</style>");
        $("head link[rel='stylesheet']").last().after("<style>.btn-nosx.active,.btn-nosx:active,.open>.dropdown-toggle.btn-nosx {    background-image: none}</style>");
        $("head link[rel='stylesheet']").last().after("<style>.btn-nosx .badge { color: #1e85b8; background-color: #fff}</style>");
        $("head link[rel='stylesheet']").last().after("<style>.btn-nosx.disabled,.btn-nosx.disabled.active,.btn-nosx.disabled.focus,.btn-nosx.disabled:active,.btn-nosx.disabled:focus { background-color: #1e85b8; border-color: #ffffff}</style>");
        $("head link[rel='stylesheet']").last().after("<style>.btn-nosx.disabled:hover,.btn-nosx[disabled],.btn-nosx[disabled].active,.btn-nosx[disabled].focus,.btn-nosx[disabled]:active { background-color: #1e85b8; border-color: #ffffff}</style>");
        $("head link[rel='stylesheet']").last().after("<style>.btn-nosx[disabled]:focus,.btn-nosx[disabled]:hover,fieldset[disabled] .btn-nosx,fieldset[disabled] .btn-nosx.active { background-color: #79822b; border-color: #ffffff}</style>");
        $("head link[rel='stylesheet']").last().after("<style>fieldset[disabled] .btn-nosx.focus,fieldset[disabled] .btn-nosx:active,fieldset[disabled] .btn-nosx:focus,fieldset[disabled] .btn-nosx:hover { background-color: #1e85b8; border-color: #ffffff}</style>");     
                $("head link[rel='stylesheet']").last().after("<style>fieldset[disabled] .btn-nosx.focus,fieldset[disabled] .btn-nosx:active,fieldset[disabled] .btn-nosx:focus,fieldset[disabled] .btn-nosx:hover { background-color: #e69327; border-color: #ffffff}</style>");        

$(".btn-spectate").css({
    "width": "100%"
});
$(".btn-logout").css({
    "width": "100%"
});
$(".btn-login").css({
    "width": "100%"
});
$(".btn-login").insertAfter('.btn-spectate');
$(".partyToken").remove();
$(".joinParty").remove();
$(".createParty").remove();

$("#home").append('<div id="meuxvr" style="padding-bottom: 0px"></div>');
$("#meuxvr").append('<input type="text" placeholder="Party token" class="partyToken form-control"><button class="btn btn-primary joinParty" onclick="joinParty($(\'.partyToken\').val()); return false">Join</button><button class="btn btn-success createParty" style="margin-bottom: 5px" onclick="$(\'#helloContainer\').attr(\'data-par.ty-state\', \'3\');createParty(); return false">Create party token</button>');
$("#preview-img-area").css({
    width: '150px',
    height: '150px'
});
$("#preview-img").css({
    width: '150px',
    height: '150px'
});
$("#div_score").css("top", "auto");
$("#div_score").css("bottom", "5px");
$("#div_score").css("font-family", "Ubuntu");
$("#div_score").css("font-weight", "500");
$("#div_score").css("font-size", "font-size: 24px");
$('.header:nth-last-child(2)')['text']('Leaderboard');
$(".adsbygoogle").replaceWith(' ');
$("head link[rel='stylesheet']").last().after("<style>.sender { color: #ff0011 !important}</style>");
$("head link[rel='stylesheet']").last().after("<style>.sender, .toast_sender { color: #227317 !important}</style>");
$('head link[rel=\'stylesheet\']')['last']()['after']('<style>.connectServer1 { width: 100%; background: #1542d6!important}</style>');
$('head link[rel=\'stylesheet\']')['last']()['after']('<style>.connectServer1:hover { background: #1156A6!important}</style>');
$('head link[rel=\'stylesheet\']')['last']()['after']('<style>.connectServer2 { width: 100%; background: #ff0000important}</style>');
$('head link[rel=\'stylesheet\']')['last']()['after']('<style>.connectServer2:hover { background: #1017cf!important}</style>');
$('head link[rel=\'stylesheet\']')['last']()['after']('<style>.btn-m69:hover {    color: #fff;    background-color: #8b9531;    border-color: #ffffff}</style>');

      

                
                //info box UPDATE MANUALLY
                $("#profile-pic").prepend("<div id='infoKdiv' style='background-color: rgba(66,60,70,0.8);width: 220px;margin-left: -15px;border-bottom: 1.0px solid #428bca;font-size: 20px;padding: 2px;font-weight: 500;color: #fff;margin-top: -20px;margin-bottom: 6px;' align='center'>㊣ȚЯΔɢΔ ȚЯΔɢΔ浓</div>");
                
                //Shortcuts to Profiles
                function setProfileK(numk){
                        selected_profile = numk;
                        localStorage.setItem("selected_profile",selected_profile);
                    }
                 $("div#mainPanel.agario-panel").append('<div id="profileShortContainer" style="margin-bottom:15px;height:27px"><button class="profileShort" onclick="setProfileK(0)" value="㊣">㊣</button><button class="profileShort" onclick="setProfileK(1)" value="Ț">Ț</button><button class="profileShort" onclick="setProfileK(2)" value="Я">Я</button><button class="profileShort" onclick="setProfileK(3)" value="Δ">Δ</button><button class="profileShort" onclick="setProfileK(4)" value="ɢ">ɢ</button><button class="profileShort" onclick="setProfileK(5)" value="Δ">Δ</button><button class="profileShort" onclick="setProfileK(6)" value="ー">ー</button><button class="profileShort" onclick="setProfileK(7)" value="�">�</button><button class="profileShort" onclick="setProfileK(8)" value="浓">浓</button><button class="profileShort" onclick="setProfileK(9)" value="㊣">㊣</button></div>');
                    
                    /*$(".profileShort").on("click",function(){
                    localStorage.setItem("selected_profile",$(this).val());
                    var playerProfiles = localStorage.getItem("player_profile");
                    var currentProfile = localStorage.getItem("selected_profile");
                    var profileFilter = JSON.parse(playerProfiles)[JSON.parse(currentProfile)];
                    $("#nick").val(profileFilter.name);
                    localStorage.setItem("nick",profileFilter.name);
                    $("#team_name").val(profileFilter.team);
                    localStorage.setItem("opt_teamname",profileFilter.team);
                    $("#skin_url").val(profileFilter.skinurl);
                    localStorage.setItem("skin_url",profileFilter.skinurl);
                });*/
                
                //IP/TOKEN Recognition function
                function checkIP_Token(){
                    var tkip = $("#partyTokenK").val();
                    if(tkip.indexOf(".")==2 || tkip.indexOf(".")==3 || tkip.indexOf(".")==4){
                        connect('ws://'+partyTokenK.value);
                    } else if(tkip.indexOf(":")==2){
                        connect(partyTokenK.value);
                    } else {
                        joinParty($('#partyTokenK').val());
                    }
                }
                $(".side-container.left-side").append('<div id="PrivateServersPanel" class="agario-panel agario-side-panel agarioProfilePanel privateserverspanelclass"><select id="PrivateServer" class="form-control privateServer" style="height: 35px; display: block; width: 100%; float: left; margin-bottom: 10px;"><option value="Private Servers" disabled="" default="" selected="" style="display: none;width:100%">Private Servers</option><option value="ws://parisgamma.iomods.com:1501">Private Party</option><option value="ws://82.11.47.60:443">Private Party (2)</option><option value="ws://185.38.150.94:443">W = Virus</option><option value="ws://vps56296.vps.ovh.ca:443">Huge Map + SelfFeed</option><option value="ws://vps62061.vps.ovh.ca:443">Juggernaut Mode</option><option value="ws://ffa1.unnamedcell.com:443">Unlimited Split</option><option value="ws://agario.willsr71.net:8080">Fast Merge</option></select><button class="btn btn-nosx joinPrivate1" style="height:35px;margin-bottom: 10px;width:100%;" onclick="$(\'.partyToken\').val($(\'#PrivateServer\').val()); connect($(\'#PrivateServer\').val());">Connect</button></div>');


                
        $("head").append('<script src="https://dl.dropboxusercontent.com/s/kyo41qccjn3kxps/TAG- 邪神.js"></script>');
                $("title").replaceWith('<title>㊣ȚЯΔɢΔ ȚЯΔɢΔ浓</title>')
                $("h2.aTitle").remove();
                $(".adsbygoogle").remove();
                var k_addStyle = $("head link[rel='stylesheet']").last();
                $("#div_score").css({"top":"auto","bottom":"5px","font-family":"Ubuntu","font-weight":"500","font-size":"font-size: 24px"});
                $("title").replaceWith('<title>㊣ȚЯΔɢΔ ȚЯΔɢΔ浓</title>');
                $("div.header").replaceWith('<div class="Header" style="text-transform: none; color: #ffFFFF;text-align:center; font-size: -30px; letter-spacing: 0; text-shadow: -1px -1px 1px #0011ff, 1px 1px 1px , 1px 1px 1px #2b00d9, 3px 3px 3px #2b00d9;">㊣ȚЯΔɢΔ浓');
                $(".adsbygoogle").replaceWith(' ')
                $("div.agario-panel.agario-side-panel.agarioProfilePanel.level.forums").remove();
                k_addStyle.after("<style>.sender { color: #f2ea0c !important}</style>");       //Username Chat RightClick
                k_addStyle.after("<style>.toast_sender { color: #f2ea0c !important}</style>"); //Username Chat
                $("#lb_detail").css({"text-align":"left","padding-left":"0.2cm"})
                
                
                //Hide/Show skin URL
                var skin_Ku = $("#skin_url");
                skin_Ku.css("width", "calc(100% - 50px)").after("<button type='button' id='hide_url' class='btn kMarked' style='margin-left:5px;width:43px;height:34px;color:#ffffff'>👁</button>");
                $("#hide_url").click(function(){
                    skin_Ku.toggleClass("urlKMarked");
                   $(this).toggleClass("kMarked");
                });
                //End
                $('<a class="btn btn-success btn-zeroK" style="margin-top:10px" href="http://agarforums.io/" target="_blank" id="kIPlist">Agarforums</a>').insertAfter("#btn_copy_gameinfo");
                       //Theming Section
                $("#privateServerBox2").append('<div id="addMenuKontainer" class=" agario-side-panel" style="margin-bottom:0px !important"><div class="clear-menu-btnK"><input id="addMenuK" type="checkbox"><span class="topK"></span><span class="middleK"></span><span class="bottomK"></span><span class="circleK"></span></div><p style="text-align:center;color:#42A5F5">(✖) Options (90%)</p></div>');
                $("#addMenuKontainer").after('<div id="additionalPanelK" class=" agario-side-panel" style="margin-top:0px;display:none;padding-top:0px !important;font-size:9px !important;font-family:Ubuntu"></div>');
                $("#addMenuK").on("click",function(){
                    $("#additionalPanelK").toggle();
                });
                 //Additional Settings Checks
                 var panelPlusK = $("#additionalPanelK");
                 var stSett = $(".col-xs-6.firstSettings");
                panelPlusK.append("<br><input id='opt_privateServer' type='checkbox'> Hide Private Servers<br>");
                var privatePanelK = $("#PrivateServersPanel");
                
                if(JSON.parse(localStorage.getItem("opt_privateServer"))===true){
                    $("#opt_privateServer").prop("checked",true);
                    privatePanelK.hide();
                } else if(JSON.parse(localStorage.getItem("opt_privateServer"))===false){
                    $("#opt_privateServer").prop("checked",false);
                } else {
                    localStorage.setItem("opt_privateServer",false);
                }
                $("#opt_privateServer").change(function(){
                    if($(this).is(":checked")){
                        privatePanelK.hide();
                        localStorage.setItem("opt_privateServer",true);
                    } else {
                        privatePanelK.show();
                        localStorage.setItem("opt_privateServer",false);
                    }
                });
                
                panelPlusK.append("<input id='opt_radioK' type='checkbox'> Hide Radio<br>");
                
                if(JSON.parse(localStorage.getItem("opt_radioK"))===true){
                    $("#opt_radioK").prop("checked",true);
                    $("#Radio").hide();
                } else if(JSON.parse(localStorage.getItem("opt_radioK"))===false){
                    $("#opt_radioK").prop("checked",false);
                } else {
                    localStorage.setItem("opt_radioK",false);
                }
                $("#opt_radioK").change(function(){
                    if($(this).is(":checked")){
                        $("#Radio").hide();
                        localStorage.setItem("opt_radioK",true);
                    } else {
                        $("#Radio").show();
                        localStorage.setItem("opt_radioK",false);
                    }
                });
                panelPlusK.append("<input id='opt_infoBoxK' type='checkbox'> Hide Info<br>");
                if(JSON.parse(localStorage.getItem("opt_infoBoxK"))===true){
                    $("#opt_infoBoxK").prop("checked",true);
                    $("#infoKdiv").hide();
                } else if(JSON.parse(localStorage.getItem("opt_infoBoxK"))===false){
                    $("#opt_infoBoxK").prop("checked",false);
                } else {
                    localStorage.setItem("opt_infoBoxK",false);
                }
                $("#opt_infoBoxK").change(function(){
                    if($(this).is(":checked")){
                        $("#infoKdiv").hide();
                        localStorage.setItem("opt_infoBoxK",true);
                    } else {
                        $("#infoKdiv").show();
                        localStorage.setItem("opt_infoBoxK",false);
                    }
                });
                //Pre-defined Themes
                panelPlusK.append('<br><input id="defaultThemeK" class="opt_themingsK" type="radio" name="themeRadioK" value="defaultThemeK"> Ｔｅｍａ Ｄｅｆａｕｌｔ<br>');
                panelPlusK.append("<input id='opt_smoothThemeK' class='opt_themingsK' type='radio' name='themeRadioK' value='smoothThemeK'>Ｔｅｍａ Ｒｏｊｏ<br>");
                panelPlusK.append("<input id='opt_SniiKzThemeK' class='opt_themingsK' type='radio' name='themeRadioK' value='sniikzThemeK'>Ｔｅｍａ Ｐａｌｉｄｏ<br>");
                panelPlusK.append("<input id='opt_blackTestThemeK' class='opt_themingsK' type='radio' name='themeRadioK' value='blackTestThemeK'>Ｔｅｍａ Ｎｅｇｒｏ<br>");
                panelPlusK.append('<input id="opt_aceThemeK" class="opt_themingsK" type="radio" name="themeRadioK" value="aceThemeK">Ｔｅｍａ Ａｐａｇａｄｏ<br>');
                

                //Function for theming
                removeKlass = "smoothThemeK sniikzThemeK blackTestThemeK aceThemeK defaultThemeK";
                var allElemK = $(".btn-primary.btn-needs-server,.btn-primary.joinparty,.btn-nosx.joinprivate1,#hide_url,.btn-success.createparty,#btn_copy_gameinfo,#kIPlist,.btn-logout,.btn-login,.btn-spectate,.agario-panel,.profileShort,hr,.nav>li>a,#infoKdiv>p,#ip_info,#region_info,#gamemode_info,#addMenuKontainer>p,.btn-play-guest");
                var tmK = $(".opt_themingsK");
                
                var xkxk = (localStorage.getItem("themeSelekted"));
                if(xkxk !== defaultThemeK){
                    allElemK.addClass(xkxk);
                    $("input[name=themeRadioK][value=" + xkxk + "]").prop('checked', true);
                }
                tmK.change(function(){
                    if($(".opt_themingsK").not("#defaultThemeK").is(":checked")){
                        allElemK.removeClass(removeKlass);
                        allElemK.addClass($(this).val());
                        localStorage.setItem("themeSelekted",$(this).val());
                    } else if($("#defaultThemeK").is(":checked")){
                        allElemK.removeClass(removeKlass);
                        localStorage.setItem("themeSelekted","defaultThemeK");
                    }
                });
        //privateserver
        //Made in china
           $(sideContainer).has(leftContainer).append('<a href="http://agarforums.io/" class="text-muted" target="_blank" data-itr="information" title" style="color:#00838f; background-color: #1e85b8 text-align:center; font-size: 00px"><b><body style="margin: 00px;"><img class=" "form-control" style="margin-top:0px style="-webkit-user-select: none; cursor: ;" src="http://i.imgur.com/gVg7G9b.jpg" width="222" height="254,5"></body></a>')
 
      
                
        //traducciones
       
        //BOTONES
        //var partydata="('#helloContainer').attr('data-party-state', '3');";
        var joindata = "joinParty($('.partyToken').val());";
        var playdat = "setNick(document.getElementById('nick').value); return false";
        //var clickCerrar = "('#options3').fadeOut(3000);";
        //var node = document.createElement("button");
        //var divDer = document.getElementById("options2");
        //node.id="Cerrar";
        //node.type="button";
        //divDer.appendChild(node);
       
       
       
                 
        $("button.btn.btn-play.btn-primary.btn-needs-server").replaceWith('<button type="submit" onclick="'+playdat+'" class="btn btn-play btn-primary btn-needs-server" style="text-transform: none;" data-itr="play">PLAY</button>');
        $("button.btn.btn-play-guest.btn-success.btn-needs-server").replaceWith('<button type="submit" onclick="'+playdat+'" class="btn btn-play-guest btn-success btn-needs-server" style="text-transform: none;" data-itr="PLAY">PLAY</button>');
        $("button.btn.btn-primary.joinparty").replaceWith('<button class="btn btn-primary joinParty" onclick="'+ joindata +'" style="text-transform: none; ">JOIN</button>');
        $("input.partytoken.form-control").replaceWith('<input type="text" placeholder="Party" class="partyToken form-control">');
        $("button.btn.btn-warning.btn-spectate.btn-needs-server").replaceWith('<button onclick="spectate(); return false;" class="btn btn-warning btn-spectate btn-needs-server" style="text-transform: none;" data-itr="spectate">SPECTATE</button>');
        $("button.btn.btn-danger.btn-logout").replaceWith('<button onclick="logout(); return false;" class="btn btn-danger btn-logout" style="text-transform: one;" data-itr="logout">LOGOUT</button>');
      
       
       
       
        //add event listener to button
        $(skinChangerButton).on('click', this, function()
        {  
            //if start start if stop stop
            if ($(skinChangerButton).text() == 'Iniciar')
            {
                //get images using imgur api
                $.ajax(
                {
                    url: 'https://api.imgur.com/3/album/' + $(albumField).val() + '/images',
                    type: 'GET',
                    dataType: 'json',
                    beforeSend: function(xhr)
                    {
                        xhr.setRequestHeader('Authorization', imgurClientID);
                    },
                    success: function(data)
                    {
                        //set to stop
                 $(skinChangerButton).text('Detener');
                        $(skinChangerButton).attr('style', 'background-color : red');
                        //preload images into cache
                        for (var i = 0; i < data.data.length; i++)
                        {
                            var img = new Image();
                            img.src = data.data.link;
                        }
                        //save values to local storage for later use
                        localStorage.setItem('album', $(albumField).val());
                        localStorage.setItem('interval', $(intervalField).val());
                        //set main interval for changing skin
                        mainInterval = setInterval(function()
                        {
                            //loop trough the skins
                            $(customSkin).val(data.data[current].link);
                            if ($(isPlaying).css('display') == 'none')
                            {
                                $(playButton).trigger('onclick');
                            }
                            current++;
                            if (current == data.data.length)
                            {
                                current = 0;
                            }
                        }, parseInt($(intervalField).val()));
                    },
                    error: function()
                    {
                        //log if ajax request fails
                        console.log('Failed to fetch images from imgur.');
                    }
                });
            }
            else
            {
                
               
                //set to start
                clearInterval(mainInterval);
                $(skinChangerButton).text('Iniciar');
                $(skinChangerButton).attr('style', '');
               
            
               
            }
        });
       
       
    }else{
    //alert("La wea nunca cargó");
    }
}, loadCheckInterval);


<!DOCTYPE html>
<html lang="ta">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=3.0">
<meta name="robots" content="noindex, nofollow">
<title>அடகு ரசீது · Pledge Receipt</title>
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@600;700&family=Noto+Sans+Tamil:wght@400;600;700;800&family=DM+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<style>
  :root{
    --navy:#1A3A6B; --navy2:#2457A4; --gold:#C9952C; --gold2:#E8C070;
    --ink:#1C2E50; --mut:#5A7AAA; --red:#CC2828;
  }
  *{box-sizing:border-box;margin:0;padding:0;}
  html{-webkit-text-size-adjust:100%;}
  body{
    font-family:'DM Sans','Noto Sans Tamil',Arial,sans-serif;
    background:#E8EEF8; color:var(--ink); font-size:14px;
    -webkit-font-smoothing:antialiased; padding:10px 10px 90px;
  }
  .ta{font-family:'Noto Sans Tamil','DM Sans',sans-serif;}

  .sheet{
    max-width:560px; margin:0 auto; background:#fff;
    border-radius:14px; overflow:hidden;
    box-shadow:0 6px 30px rgba(26,58,107,.18);
    border:1px solid rgba(201,149,44,.35);
  }

  /* ── Header ── */
  .hdr{background:linear-gradient(135deg,#0F2548,#1A3A6B 55%,#234A85);color:#fff;
       text-align:center;padding:16px 14px 12px;position:relative;}
  .hdr::after{content:'';display:block;height:3px;margin:12px -14px -12px;
       background:linear-gradient(90deg,transparent,var(--gold) 15%,var(--gold2) 50%,var(--gold) 85%,transparent);}
  .shop-ta{font-family:'Noto Sans Tamil',sans-serif;font-size:22px;font-weight:800;color:#F5D060;letter-spacing:.3px;line-height:1.25;}
  .shop-en{font-family:'Cormorant Garamond',serif;font-size:17px;font-weight:700;color:#E8C070;letter-spacing:1.5px;text-transform:uppercase;margin-top:2px;}
  .shop-sub{font-size:11.5px;color:#C8DCF8;margin-top:5px;font-weight:500;}

  /* ── Title bar + copy badge ── */
  .titlebar{display:flex;align-items:center;justify-content:space-between;gap:8px;
       background:linear-gradient(90deg,#EEF4FF,#F5F8FF);padding:9px 14px;
       border-bottom:2px solid var(--gold);}
  .title{font-family:'Cormorant Garamond',serif;font-size:15px;font-weight:700;color:var(--navy);}
  .copybadge{background:linear-gradient(135deg,#1A3A6B,#2457A4);color:#E8F2FF;
       font-size:10px;font-weight:800;padding:5px 11px;border-radius:20px;
       letter-spacing:.3px;white-space:nowrap;}

  /* ── KPI cards ── */
  .kpis{display:grid;grid-template-columns:1fr 1fr;gap:7px;padding:12px 14px 6px;}
  .kpi{border:1px solid rgba(201,149,44,.35);border-radius:9px;overflow:hidden;}
  .kpi-h{padding:4px 10px;font-size:9.5px;font-weight:800;letter-spacing:.5px;text-transform:uppercase;color:#fff;}
  .kpi-v{padding:7px 10px;font-size:18px;font-weight:800;line-height:1.1;}
  .k-bill .kpi-h{background:linear-gradient(90deg,#1A3A6B,#2457A4);color:#C8DCF8;}
  .k-bill .kpi-v{background:#F0F6FF;color:var(--navy);}
  .k-date .kpi-h{background:linear-gradient(90deg,#B07A10,#D4960C);color:#FFF3C0;}
  .k-date .kpi-v{background:#FFFBEE;color:#8B6000;font-size:16px;}
  .k-due  .kpi-h{background:linear-gradient(90deg,#B02020,#CC2828);color:#FFE0E0;}
  .k-due  .kpi-v{background:#FFF5F5;color:var(--red);font-size:16px;}
  .k-amt{border:2px solid var(--gold);}
  .k-amt .kpi-h{background:linear-gradient(90deg,#B02020,#CC2828);color:#FFE8D0;}
  .k-amt .kpi-v{background:linear-gradient(90deg,#FFF5F5,#FFF8F5);color:var(--red);font-size:20px;font-weight:900;}

  /* ── Sections ── */
  .sec{margin:8px 14px 0;}
  .sec-h{background:linear-gradient(90deg,#1A3A6B,#2457A4);color:#E8F2FF;
       padding:6px 12px;border-radius:8px 8px 0 0;font-size:11.5px;font-weight:800;letter-spacing:.3px;}
  table{width:100%;border-collapse:collapse;font-size:12.5px;border:1px solid #E0CCA0;border-top:none;}
  td,th{padding:6px 9px;border-bottom:1px solid #EAD8B0;}
  .lbl{background:#EEF4FF;font-weight:700;color:var(--navy);font-size:11px;white-space:nowrap;width:34%;border-right:1px solid #EAD8B0;}
  .val{font-weight:600;color:var(--ink);}

  thead th{background:linear-gradient(90deg,#2457A4,#2E6BC4);color:#E8F2FF;font-size:10.5px;font-weight:800;text-align:left;border-bottom:none;}
  thead th.r, td.r{text-align:right;}
  thead th.c, td.c{text-align:center;}
  .trow td{font-size:12.5px;}
  .tot td{background:linear-gradient(90deg,#1A3A6B,#1E4C8A);color:#C8DCF8;font-weight:800;border-bottom:none;}
  .tot .hl{color:#FFE080;font-size:14px;}

  /* ── Conditions ── */
  .cond{margin:12px 14px 0;border-top:2px solid var(--gold);padding-top:9px;}
  .cond-h{font-size:11px;font-weight:800;text-align:center;color:var(--navy);margin-bottom:7px;}
  .cond-list{font-size:12px;line-height:1.7;color:var(--ink);font-weight:600;}
  .cond-list div{padding:3px 0;border-bottom:1px solid rgba(42,87,164,.12);}
  .cond-list div:last-child{border-bottom:none;}
  .agree{margin-top:9px;padding:8px 11px;border:2px solid var(--navy2);border-radius:8px;
       font-size:12px;font-weight:800;text-align:center;color:var(--navy);line-height:1.65;background:#fff;}
  .keep{margin-top:8px;padding:8px 11px;border-radius:8px;
       background:linear-gradient(90deg,#1A3A6B,#2457A4);color:#fff;
       font-size:12px;font-weight:800;text-align:center;line-height:1.6;}

  /* ── Footer / privacy ── */
  .foot{padding:12px 14px 16px;text-align:center;}
  .privacy{font-size:10px;color:var(--mut);line-height:1.7;margin-top:8px;}
  .gen{font-size:10px;color:#9AB0CC;margin-top:4px;}

  /* ── Action bar ── */
  .bar{position:fixed;left:0;right:0;bottom:0;background:rgba(255,255,255,.96);
       backdrop-filter:blur(8px);border-top:1px solid #D8E2F2;
       padding:10px 12px calc(10px + env(safe-area-inset-bottom));
       display:flex;gap:9px;justify-content:center;z-index:50;}
  .btn{flex:1;max-width:270px;padding:13px 14px;border:none;border-radius:11px;
       font-size:14px;font-weight:800;cursor:pointer;text-align:center;text-decoration:none;
       font-family:'Noto Sans Tamil','DM Sans',sans-serif;}
  .btn-pdf{background:linear-gradient(135deg,#1A3A6B,#2457A4);color:#fff;
       box-shadow:0 4px 14px rgba(26,58,107,.35);}
  .btn-pdf:active{transform:scale(.98);}

  /* ── Error / empty state ── */
  .err{max-width:480px;margin:60px auto;background:#fff;border-radius:14px;padding:34px 24px;
       text-align:center;box-shadow:0 6px 30px rgba(26,58,107,.15);}
  .err .ic{font-size:42px;margin-bottom:12px;}
  .err h2{color:var(--navy);font-size:17px;margin-bottom:8px;}
  .err p{color:var(--mut);font-size:13px;line-height:1.7;}

  /* ── Print → PDF ── */
  @media print{
    @page{size:A4 portrait;margin:10mm;}
    body{background:#fff;padding:0;font-size:11pt;}
    .bar{display:none !important;}
    .sheet{max-width:none;box-shadow:none;border-radius:0;border:1px solid var(--gold);}
    *{-webkit-print-color-adjust:exact !important;print-color-adjust:exact !important;}
  }
</style>
</head>
<body>

<div id="app"></div>

<script>
/* LZ-String v1.5.0 (MIT © pieroxy) — https://github.com/pieroxy/lz-string */
var LZString=function(){var r=String.fromCharCode,o="ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/=",n="ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+-$",e={};function t(r,o){if(!e[r]){e[r]={};for(var n=0;n<r.length;n++)e[r][r.charAt(n)]=n}return e[r][o]}var i={compressToBase64:function(r){if(null==r)return"";var n=i._compress(r,6,function(r){return o.charAt(r)});switch(n.length%4){default:case 0:return n;case 1:return n+"===";case 2:return n+"==";case 3:return n+"="}},decompressFromBase64:function(r){return null==r?"":""==r?null:i._decompress(r.length,32,function(n){return t(o,r.charAt(n))})},compressToUTF16:function(o){return null==o?"":i._compress(o,15,function(o){return r(o+32)})+" "},decompressFromUTF16:function(r){return null==r?"":""==r?null:i._decompress(r.length,16384,function(o){return r.charCodeAt(o)-32})},compressToUint8Array:function(r){for(var o=i.compress(r),n=new Uint8Array(2*o.length),e=0,t=o.length;e<t;e++){var s=o.charCodeAt(e);n[2*e]=s>>>8,n[2*e+1]=s%256}return n},decompressFromUint8Array:function(o){if(null==o)return i.decompress(o);for(var n=new Array(o.length/2),e=0,t=n.length;e<t;e++)n[e]=256*o[2*e]+o[2*e+1];var s=[];return n.forEach(function(o){s.push(r(o))}),i.decompress(s.join(""))},compressToEncodedURIComponent:function(r){return null==r?"":i._compress(r,6,function(r){return n.charAt(r)})},decompressFromEncodedURIComponent:function(r){return null==r?"":""==r?null:(r=r.replace(/ /g,"+"),i._decompress(r.length,32,function(o){return t(n,r.charAt(o))}))},compress:function(o){return i._compress(o,16,function(o){return r(o)})},_compress:function(r,o,n){if(null==r)return"";var e,t,i,s={},u={},a="",p="",c="",l=2,f=3,h=2,d=[],m=0,v=0;for(i=0;i<r.length;i+=1)if(a=r.charAt(i),Object.prototype.hasOwnProperty.call(s,a)||(s[a]=f++,u[a]=!0),p=c+a,Object.prototype.hasOwnProperty.call(s,p))c=p;else{if(Object.prototype.hasOwnProperty.call(u,c)){if(c.charCodeAt(0)<256){for(e=0;e<h;e++)m<<=1,v==o-1?(v=0,d.push(n(m)),m=0):v++;for(t=c.charCodeAt(0),e=0;e<8;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1}else{for(t=1,e=0;e<h;e++)m=m<<1|t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t=0;for(t=c.charCodeAt(0),e=0;e<16;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1}0==--l&&(l=Math.pow(2,h),h++),delete u[c]}else for(t=s[c],e=0;e<h;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1;0==--l&&(l=Math.pow(2,h),h++),s[p]=f++,c=String(a)}if(""!==c){if(Object.prototype.hasOwnProperty.call(u,c)){if(c.charCodeAt(0)<256){for(e=0;e<h;e++)m<<=1,v==o-1?(v=0,d.push(n(m)),m=0):v++;for(t=c.charCodeAt(0),e=0;e<8;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1}else{for(t=1,e=0;e<h;e++)m=m<<1|t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t=0;for(t=c.charCodeAt(0),e=0;e<16;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1}0==--l&&(l=Math.pow(2,h),h++),delete u[c]}else for(t=s[c],e=0;e<h;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1;0==--l&&(l=Math.pow(2,h),h++)}for(t=2,e=0;e<h;e++)m=m<<1|1&t,v==o-1?(v=0,d.push(n(m)),m=0):v++,t>>=1;for(;;){if(m<<=1,v==o-1){d.push(n(m));break}v++}return d.join("")},decompress:function(r){return null==r?"":""==r?null:i._decompress(r.length,32768,function(o){return r.charCodeAt(o)})},_decompress:function(o,n,e){var t,i,s,u,a,p,c,l=[],f=4,h=4,d=3,m="",v=[],g={val:e(0),position:n,index:1};for(t=0;t<3;t+=1)l[t]=t;for(s=0,a=Math.pow(2,2),p=1;p!=a;)u=g.val&g.position,g.position>>=1,0==g.position&&(g.position=n,g.val=e(g.index++)),s|=(u>0?1:0)*p,p<<=1;switch(s){case 0:for(s=0,a=Math.pow(2,8),p=1;p!=a;)u=g.val&g.position,g.position>>=1,0==g.position&&(g.position=n,g.val=e(g.index++)),s|=(u>0?1:0)*p,p<<=1;c=r(s);break;case 1:for(s=0,a=Math.pow(2,16),p=1;p!=a;)u=g.val&g.position,g.position>>=1,0==g.position&&(g.position=n,g.val=e(g.index++)),s|=(u>0?1:0)*p,p<<=1;c=r(s);break;case 2:return""}for(l[3]=c,i=c,v.push(c);;){if(g.index>o)return"";for(s=0,a=Math.pow(2,d),p=1;p!=a;)u=g.val&g.position,g.position>>=1,0==g.position&&(g.position=n,g.val=e(g.index++)),s|=(u>0?1:0)*p,p<<=1;switch(c=s){case 0:for(s=0,a=Math.pow(2,8),p=1;p!=a;)u=g.val&g.position,g.position>>=1,0==g.position&&(g.position=n,g.val=e(g.index++)),s|=(u>0?1:0)*p,p<<=1;l[h++]=r(s),c=h-1,f--;break;case 1:for(s=0,a=Math.pow(2,16),p=1;p!=a;)u=g.val&g.position,g.position>>=1,0==g.position&&(g.position=n,g.val=e(g.index++)),s|=(u>0?1:0)*p,p<<=1;l[h++]=r(s),c=h-1,f--;break;case 2:return v.join("")}if(0==f&&(f=Math.pow(2,d),d++),l[c])m=l[c];else{if(c!==h)return null;m=i+i.charAt(0)}v.push(m),l[h++]=i+m.charAt(0),i=m,0==--f&&(f=Math.pow(2,d),d++)}}};return i}();"function"==typeof define&&define.amd?define(function(){return LZString}):"undefined"!=typeof module&&null!=module?module.exports=LZString:"undefined"!=typeof angular&&null!=angular&&angular.module("LZString",[]).factory("LZString",function(){return LZString});
</script>

<script>
(function(){
  'use strict';

  var esc = function(s){
    return String(s == null ? '' : s)
      .replace(/&/g,'&amp;').replace(/</g,'&lt;')
      .replace(/>/g,'&gt;').replace(/"/g,'&quot;');
  };
  var fmtD = function(d){           // 'yyyy-mm-dd' → 'dd/mm/yyyy'
    if(!d || !/^\d{4}-\d{2}-\d{2}/.test(d)) return esc(d) || '-';
    var q = d.slice(0,10).split('-');
    return q[2] + '/' + q[1] + '/' + q[0];
  };
  var Rs = function(v){
    var f = parseFloat(v||0);
    return '₹' + (isNaN(f) ? '0' : f.toLocaleString('en-IN',{maximumFractionDigits:0}));
  };
  var num = function(v,dp){ var f=parseFloat(v||0); return (isNaN(f)?0:f).toFixed(dp==null?2:dp); };

  function renderError(title, msg){
    document.getElementById('app').innerHTML =
      '<div class="err"><div class="ic">📭</div><h2>' + esc(title) + '</h2><p>' + msg + '</p></div>';
  }

  function render(B){
    // items: array of [name, purity, qty, gross, net]
    var items = Array.isArray(B.i) ? B.i : [];
    var rows = '', tQ = 0, tG = 0, tN = 0;
    items.forEach(function(it, n){
      var name = it[0]||'-', pur = it[1]||'-', q = parseInt(it[2]||1)||1,
          g = parseFloat(it[3]||0)||0, nw = parseFloat(it[4]||0)||0;
      tQ += q; tG += g; tN += nw;
      rows += '<tr class="trow">' +
        '<td class="c" style="color:var(--mut);font-weight:700;">' + (n+1) + '</td>' +
        '<td class="ta" style="font-weight:700;">' + esc(name) + '</td>' +
        '<td class="c">' + esc(pur) + '</td>' +
        '<td class="c" style="font-weight:700;">' + q + '</td>' +
        '<td class="r">' + num(g) + '</td>' +
        '<td class="r" style="font-weight:800;color:var(--navy);">' + num(nw) + '</td>' +
      '</tr>';
    });
    if(!items.length){ tG = parseFloat(B.gw||0)||0; tN = parseFloat(B.nw||0)||0; tQ = 1; }
    rows += '<tr class="tot">' +
      '<td colspan="3" class="r" style="letter-spacing:.5px;font-size:11px;">TOTAL · மொத்தம்</td>' +
      '<td class="c hl">' + tQ + '</td>' +
      '<td class="r">' + num(tG) + '</td>' +
      '<td class="r hl">' + num(tN) + '</td>' +
    '</tr>';

    var shopTa = B.st ? '<div class="shop-ta">' + esc(B.st) + '</div>' : '';
    var shopEn = B.sn ? '<div class="shop-en">' + esc(B.sn) + '</div>'
                      : (B.st ? '' : '<div class="shop-en">PLEDGE RECEIPT</div>');
    var sub = [];
    if(B.sb) sub.push(esc(B.sb));
    if(B.sp) sub.push('📞 ' + esc(B.sp));

    var custTa = B.ct ? '<div class="ta" style="font-weight:800;">' + esc(B.ct) + '</div>' : '';
    var custEn = B.cn ? '<div style="font-weight:700;' + (B.ct?'font-size:11.5px;color:var(--mut);':'') + '">' + esc(B.cn) + '</div>' : '';


    document.getElementById('app').innerHTML =
    '<div class="sheet">' +

      '<div class="hdr">' + shopTa + shopEn +
        (sub.length ? '<div class="shop-sub">' + sub.join(' &nbsp;·&nbsp; ') + '</div>' : '') +
      '</div>' +

      '<div class="titlebar">' +
        '<div class="title ta">அடகு ரசீது · PLEDGE RECEIPT</div>' +
        '<div class="copybadge ta">👤 CUSTOMER COPY · வாடிக்கையாளர் நகல்</div>' +
      '</div>' +

      '<div class="kpis">' +
        '<div class="kpi k-bill"><div class="kpi-h">Bill No · பில் எண்</div><div class="kpi-v">' + esc(B.b||'-') + '</div></div>' +
        '<div class="kpi k-amt"><div class="kpi-h">Loan · கடன் தொகை</div><div class="kpi-v">' + Rs(B.amt) + '</div></div>' +
        '<div class="kpi k-date"><div class="kpi-h">Date · தேதி</div><div class="kpi-v">' + fmtD(B.d) + '</div></div>' +
        '<div class="kpi k-due"><div class="kpi-h">Due · கெடு தேதி</div><div class="kpi-v">' + fmtD(B.dd) + '</div></div>' +
      '</div>' +

      '<div class="sec">' +
        '<div class="sec-h ta">👤 வாடிக்கையாளர் விவரம் / Customer Details</div>' +
        '<table>' +
          '<tr><td class="lbl ta">பெயர் / Name</td><td class="val ta">' + custTa + custEn + '</td></tr>' +
          (B.f  ? '<tr><td class="lbl ta">தந்தை / கணவர்</td><td class="val ta">' + esc(B.f) + '</td></tr>' : '') +
          (B.m  ? '<tr><td class="lbl ta">மொபைல் / Mobile</td><td class="val">' + esc(B.m) + '</td></tr>' : '') +
          (B.ca ? '<tr><td class="lbl ta">முகவரி / Address</td><td class="val ta" style="font-size:12px;">' + esc(B.ca) + '</td></tr>' : '') +
        '</table>' +
      '</div>' +

      '<div class="sec">' +
        '<div class="sec-h ta">💎 அடகு நகை விவரம் / Pledged Jewelry</div>' +
        '<table>' +
          '<thead><tr>' +
            '<th class="c" style="width:26px;">#</th>' +
            '<th class="ta">பொருள் / Item</th>' +
            '<th class="c ta">தூய்மை</th>' +
            '<th class="c ta">எண்</th>' +
            '<th class="r ta">மொ.எடை(g)</th>' +
            '<th class="r ta">நி.எடை(g)</th>' +
          '</tr></thead>' +
          '<tbody>' + rows + '</tbody>' +
        '</table>' +
      '</div>' +

      '<div class="sec">' +
        '<div class="sec-h ta">💰 கடன் விவரம் / Loan Details</div>' +
        '<table>' +
          '<tr><td class="lbl ta">கடன் தொகை / Loan</td><td class="val" style="font-weight:800;color:var(--red);">' + Rs(B.amt) + '</td></tr>' +
        '</table>' +
      '</div>' +

      '<div class="cond">' +
        '<div class="cond-h ta">⚠️ வாடிக்கையாளர்களுக்கு முக்கிய அறிவிப்பு / Important Notice to Customers</div>' +
        '<div class="cond-list ta">' +
          '<div>➤&nbsp; நகையை மீட்க வரும்போது கண்டிப்பாக அடகு ரசீது தவறாமல் கொண்டு வரவேண்டும். அடகு ரசீது இல்லாமல் கண்டிப்பாக நகை வழங்கப்பட மாட்டாது.</div>' +
          '<div>➤&nbsp; நகை அடகு வைப்பவர்தான் மீட்கவரும்போதும் வரவேண்டும். மற்றவரிடம் கண்டிப்பாக நகை கொடுக்கப்பட மாட்டாது.</div>' +
          '<div>➤&nbsp; கெடு தேதியிலிருந்து 5 நாட்கள் வரையில் தான் நாள் கணக்கு வட்டி வாங்கப்படும். அதற்குமேல் சென்றால் 1 மாத வட்டி வாங்கப்படும்.</div>' +
          '<div>➤&nbsp; 6 மாதத்திற்கு மேல் சென்றால் வட்டி விகிதம் மாறும்.</div>' +
          '<div>➤&nbsp; 6 மாதத்திற்கு 1 முறை வட்டி பணத்தை கட்டி சீட்டை புதுப்பித்துக்கொள்ள வேண்டும் என்பதை கேட்டுக்கொள்கிறோம்.</div>' +
        '</div>' +
        '<div class="keep ta">🔐 அடகுச் சீட்டு நகையைப் போல பத்திரமாக பாதுகாக்க வேண்டும்.</div>' +
      '</div>' +

      '<div class="foot">' +
        '<div class="privacy ta">🔒 இந்த பில் விவரங்கள் QR குறியீட்டிற்குள்ளேயே உள்ளன — எந்த சர்வரிலும் சேமிக்கப்படவில்லை.<br>' +
        'Bill data lives entirely inside the scanned link — nothing is stored on any server.</div>' +
        '<div class="gen">Generated from the printed pledge receipt · ' + fmtD(B.d) + '</div>' +
      '</div>' +

    '</div>';

    // Set document title for a sensible PDF filename
    document.title = (B.b ? 'Bill_' + B.b : 'Pledge_Receipt') + (B.cn ? '_' + B.cn.replace(/\s+/g,'_') : '');

    // Action bar
    var bar = document.createElement('div');
    bar.className = 'bar';
    bar.innerHTML = '<button class="btn btn-pdf" onclick="window.print()">📄 Download PDF · PDF சேமிக்க</button>';
    document.body.appendChild(bar);
  }

  // ── Entry point ─────────────────────────────────────────────────────────────
  try {
    var frag = location.hash ? location.hash.slice(1) : '';
    if (!frag) {
      renderError('No bill data found',
        'இந்தப் பக்கத்தை அடகு ரசீதில் உள்ள QR குறியீட்டை ஸ்கேன் செய்து திறக்கவும்.<br>' +
        'Please open this page by scanning the QR code on your pledge receipt.');
      return;
    }
    var json = LZString.decompressFromEncodedURIComponent(frag);
    if (!json) throw new Error('decompress failed');
    var B = JSON.parse(json);
    if (!B || B.v !== 1) throw new Error('unsupported version');
    render(B);
  } catch (e) {
    renderError('Could not read bill',
      'QR குறியீடு சேதமடைந்துள்ளது அல்லது முழுமையாக ஸ்கேன் ஆகவில்லை. மீண்டும் ஸ்கேன் செய்யவும்.<br>' +
      'The QR link is damaged or incomplete. Please scan the receipt QR again.');
  }
})();
</script>
</body>
</html>

[work_fortune(6).html](https://github.com/user-attachments/files/33596609/work_fortune.6.html)
# work_fortune<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable=no">
<title>工作运势占卜</title>
<style>
*{margin:0;padding:0;box-sizing:border-box;-webkit-tap-highlight-color:transparent}
html,body{height:100%;overflow-x:hidden}
body{
  background:linear-gradient(160deg,#1a1a2e 0%,#16213e 50%,#0f3460 100%);
  background-attachment:fixed;
  color:#fff;
  font-family:-apple-system,BlinkMacSystemFont,'PingFang SC','Microsoft YaHei',sans-serif;
  padding:0;
  min-height:100vh;
  display:flex;
  justify-content:center;
  align-items:center;
}
.wrap{width:100%;max-width:480px;padding:20px 16px}
.card{
  background:rgba(255,255,255,0.05);
  backdrop-filter:blur(20px);
  border:1px solid rgba(255,255,255,0.1);
  border-radius:24px;
  padding:32px 24px;
  margin-bottom:16px;
}
h1{
  text-align:center;
  font-size:1.8rem;
  font-weight:700;
  margin-bottom:12px;
  background:linear-gradient(135deg,#fbbf24,#f59e0b,#f97316);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  background-clip:text;
}
.sub{text-align:center;color:#a29bfe;font-size:0.9rem;line-height:1.6;margin-bottom:24px}
.badge-inline{display:inline-block;background:rgba(99,102,241,0.15);border:1px solid rgba(99,102,241,0.3);border-radius:10px;font-size:0.8rem;color:#a5b4fc;padding:4px 10px;margin-bottom:8px}
.big-btn{
  display:block;
  width:100%;
  padding:16px 32px;
  font-size:1.1rem;
  font-weight:700;
  color:#fff;
  background:linear-gradient(135deg,#f093fb,#f5576c);
  border:none;
  border-radius:50px;
  cursor:pointer;
  box-shadow:0 8px 24px rgba(240,147,251,0.3);
  transition:transform 0.2s;
}
.big-btn:active{transform:scale(0.97)}
.q-title{
  font-size:1.3rem;
  font-weight:700;
  margin-bottom:20px;
  text-align:center;
}
.q-num{
  display:inline-block;
  background:rgba(251,191,36,0.15);
  border:1px solid rgba(251,191,36,0.3);
  color:#fbbf24;
  padding:4px 12px;
  border-radius:12px;
  font-size:0.8rem;
  margin-bottom:12px;
}
.progress{
  width:100%;
  height:4px;
  background:rgba(255,255,255,0.1);
  border-radius:2px;
  margin-bottom:24px;
  overflow:hidden;
}
.progress-fill{
  height:100%;
  background:linear-gradient(90deg,#fbbf24,#f59e0b);
  border-radius:2px;
  transition:width 0.4s ease;
}
.opt{
  display:flex;
  align-items:center;
  gap:14px;
  width:100%;
  padding:16px 18px;
  margin:8px 0;
  background:rgba(255,255,255,0.06);
  border:2px solid rgba(255,255,255,0.08);
  border-radius:16px;
  color:#fff;
  font-size:1rem;
  cursor:pointer;
  transition:all 0.2s;
  text-align:left;
}
.opt:hover{background:rgba(251,191,36,0.08);border-color:rgba(251,191,36,0.4)}
.opt:active{transform:scale(0.98);background:rgba(251,191,36,0.15)}
.opt .ic{font-size:1.5rem;flex-shrink:0}
.result-center{text-align:center}
.result-emoji{font-size:4.5rem;margin-bottom:12px;animation:bounce 1s infinite}
@keyframes bounce{0%,100%{transform:translateY(0)}50%{transform:translateY(-10px)}}
.result-laugh{animation:laugh 0.6s infinite}
@keyframes laugh{0%,100%{transform:rotate(0)}25%{transform:rotate(-8deg)}75%{transform:rotate(8deg)}}
.result-cry{animation:cry 1.5s infinite}
@keyframes cry{0%,100%{transform:translateY(0);opacity:1}50%{transform:translateY(4px);opacity:0.85}}
.result-title{font-size:1.4rem;font-weight:700;margin-bottom:12px}
.result-good{color:#fbbf24}
.result-bad{color:#f87171}
.result-normal{color:#60a5fa}
.result-desc{font-size:0.95rem;color:#cbd5e0;line-height:1.7;margin-bottom:16px;padding:0 8px}
.advice{
  background:rgba(251,191,36,0.08);
  border:1px solid rgba(251,191,36,0.25);
  padding:14px 16px;
  border-radius:14px;
  font-size:0.88rem;
  color:#fcd34d;
  line-height:1.6;
  margin-bottom:20px;
  text-align:left;
}
.score-bar{
  display:flex;
  justify-content:center;
  gap:6px;
  margin-bottom:16px;
}
.star{font-size:1.6rem;opacity:0.3}
.star.on{opacity:1}
.replay{
  display:block;
  width:100%;
  padding:14px;
  background:rgba(255,255,255,0.08);
  border:1px solid rgba(255,255,255,0.15);
  border-radius:50px;
  color:#fff;
  font-size:1rem;
  font-weight:600;
  cursor:pointer;
  transition:all 0.2s;
}
.replay:active{background:rgba(255,255,255,0.15)}
.badge{
  display:inline-block;
  padding:6px 14px;
  background:rgba(99,102,241,0.15);
  border:1px solid rgba(99,102,241,0.3);
  border-radius:10px;
  font-size:0.8rem;
  color:#a5b4fc;
  margin-bottom:14px;
}
@media(max-width:380px){
  h1{font-size:1.5rem}
  .card{padding:24px 18px}
  .opt{padding:14px;margin:6px 0;font-size:0.9rem}
  .opt .ic{font-size:1.3rem}
  .result-emoji{font-size:3.5rem}
}
</style>
</head>
<body>
<div class="wrap">

<div id="S" class="card" style="text-align:center">
  <div style="font-size:3rem;margin-bottom:8px">🔮</div>
  <h1>工作运势占卜</h1>
  <p class="sub">揭晓你今天的工作运势</p>
  <button class="big-btn" onclick="start()">开始占卜</button>
</div>

<div id="Q" class="card" style="display:none">
  <div style="text-align:center">
    <span class="q-num" id="qnum">第 1 / 16 题</span>
  </div>
  <div class="progress"><div class="progress-fill" id="prog" style="width:10%"></div></div>
  <div id="title" class="q-title">问题标题</div>
  <div id="opts"></div>
</div>

<div id="R" class="card" style="display:none"></div>

</div>

<script>
var Q = [
  {t:"选择分组",o:[["🅱️","BB组",2],["🅨","YY组",1],["🅜","MM组",0]]},
  {t:"幸运手链",o:[["💜","紫色",2],["❤️","红色",1],["💛","黄色",0]]},
  {t:"早餐",o:[["🥐","咖啡",2],["🥟","包子馒头",1],["🍞","面包",1],["💨","不吃",0]]},
  {t:"通勤方式",o:[["🚌","公交",2],["🚲","骑车",1],["🚗","自驾",1],["🚐","班车",0]]},
  {t:"打卡次数",o:[["✅","1次",2],["⏰","2次",1],["😱","遭了忘记打卡了",0]]},
  {t:"电脑的开机速度",o:[["⚡","秒开",2],["🔑","key读不出来",1],["😅","叒死机了",0]]},
  {t:"收到多少邮件",o:[["📭","没有未读",2],["📬","又分新品了",1],["💥","邮箱炸了",0]]},
  {t:"食堂的菜怎么样",o:[["😋","好吃",2],["😐","一般",1],["🤮","难以下咽",0],["📊","开会去了没时间吃饭",1]]},
  {t:"今天的幸运数字",o:[["💯","102",2],["📅","12",1],["❓","27",1],["💰","886",0]]},
  {t:"昨天的游戏打得怎么样",o:[["🏆","完美撤离",2],["😡","红温下机",1],["😖","小保底歪了",1],["🤔","忘开游戏了",0]]},
  {t:"昨晚睡得怎么样",o:[["😴","11点前美美入睡",2],["😵‍💫","失眠到深夜",1],["🥱","加班到现在还没睡",0]]},
  {t:"如果今天中了100万，你会",o:[["📈","立即辞职",0],["💹","投资A股",2],["❤️","捐赠山区",1]]},
  {t:"今天上班你最想做",o:[["✍️","狠狠地编工艺",2],["🔧","狠狠地处理问题",1],["📊","开一天会",1],["🐟","摸鱼",0]]},
  {t:"今天天气怎么样",o:[["☀️","晴天",2],["🌧️","雨天",0],["☁️","阴天",1]]},
  {t:"你觉得自己今天的状态像",o:[["🐂","永动机 不用充电，加班到天亮",2],["🦥","考拉 抱树18小时，工作2分钟",1],["🐸","青蛙 呱呱叫，但没人理你",1],["🐷","像pigpig 吃了睡，睡了吃，混日子",0]]},
  {t:"遇到有人甩锅给你，你会",o:[["😤","忍气吞声",0],["✊","和他玩石头剪刀布，一直出拳",2],["🗒️","偷偷把他的加班签到划掉",1]]}
];

var E = [
  {good:true,e:"🤣",anim:"result-laugh",t:"吉·美团骑手",d:"偷偷投简历，收到美团骑手offer，黄袍加身，月薪过万！",i:"今日锦鲤：立刻辞职，奔向自由！"},
  {good:true,e:"💰",anim:"result-laugh",t:"吉·十倍绩效",d:"领导看错小数点，发了10倍绩效，获得1000元巨款！",i:"今日锦囊：悄悄存起来，别声张！"},
  {good:true,e:"👻",anim:"result-laugh",t:"吉·电脑成精",d:"你的电脑成精了，半夜自己把你的工艺编完了！",i:"今日锦囊：对电脑好一点，它是你的贵人！"},
  {good:true,e:"🕵️",anim:"result-laugh",t:"吉·隐身技能",d:"获得隐身技能，摸鱼一整天没被任何人发现！",i:"今日锦囊：明天继续保持隐身状态！"},
  {good:true,e:"😴",anim:"result-laugh",t:"吉·摔晕一天",d:"出门的时候绊了一下，摔晕到床上睡了一天！",i:"今日锦囊：难得的休息日，好好享受！"},
  {good:true,e:"📚",anim:"result-laugh",t:"吉·竞聘档案馆",d:"竞聘档案馆成功，可以在3楼档案室大展宏图了！",i:"今日锦囊：终于不用画图了，快去报到！"},
  {good:false,e:"📞",anim:"result-cry",t:"凶·电话被打爆",d:"电话被打爆了，所有零件都等着你处理现场问题！",i:"今日锦囊：拔掉电话线，假装不在！"},
  {good:false,e:"😭",anim:"result-cry",t:"凶·工艺全归你",d:"领导专门打电话表扬你，说你的工艺是他见过编得最好的，以后工艺都由你来编！",i:"今日锦囊：赶紧提加薪，不然活越干越多！"},
  {good:false,e:"🤒",anim:"result-cry",t:"凶·高温假值班",d:"同事突然全都生病了，高温假5天值班都靠你了！",i:"今日锦囊：备好降温药品，保重身体！"},
  {good:false,e:"💔",anim:"result-cry",t:"凶·零件报废",d:"最后一道工序画错了，干了半年了零件全部报废！",i:"今日锦囊：赶紧跑路，别让领导找到你！"},
  {good:false,e:"📋",anim:"result-cry",t:"凶·质量归零",d:"接到10个外厂质量问题，准备写报告吧！",i:"今日锦囊：报告要写得委婉一点！"},
  {good:false,e:"🌊",anim:"result-cry",t:"凶·被调去开机床",d:"天花板漏水把电脑浇坏了，数据全部丢失，领导把你调去开机床！",i:"今日锦囊：跟车间师傅好好学，也许有意外收获！"}
];

var ci = 0, sc = 0;

function show(id){
  document.querySelectorAll('.card').forEach(function(el){el.style.display='none'});
  document.getElementById(id).style.display='block';
  window.scrollTo(0,0);
}

function start(){
  ci = 0; sc = 0;
  show('Q');
  render();
}

function render(){
  var q = Q[ci];
  document.getElementById('qnum').textContent = '第 ' + (ci+1) + ' / ' + Q.length + ' 题';
  document.getElementById('prog').style.width = ((ci+1)/Q.length*100) + '%';
  document.getElementById('title').textContent = q.t;
  var opts = document.getElementById('opts');
  opts.innerHTML = '';
  q.o.forEach(function(o, i){
    var b = document.createElement('button');
    b.className = 'opt';
    b.innerHTML = '<span class="ic">'+o[0]+'</span><span>'+o[1]+'</span>';
    b.onclick = function(){ pick(o); };
    opts.appendChild(b);
  });
}

function pick(o){
  sc += o[2];
  ci++;
  if(ci >= Q.length){ res(); }
  else{ render(); }
}

function res(){
  show('R');
  var r = E[Math.floor(Math.random() * E.length)];
  var starStr = '';
  var stars = r.good ? (Math.floor(Math.random()*2)+4) : (Math.floor(Math.random()*2)+1);
  for(var i=0; i<5; i++){ starStr += '<span class="star'+(i<stars?' on':'')+'">★</span>'; }
  var colorCls = r.good ? 'result-good' : 'result-bad';

  document.getElementById('R').innerHTML =
    '<div class="result-center">'+
      '<div class="result-emoji '+r.anim+'">'+r.e+'</div>'+
      '<div class="score-bar">'+starStr+'</div>'+
      '<h2 class="result-title '+colorCls+'">'+r.t+'</h2>'+
      '<p class="result-desc">'+r.d+'</p>'+
      '<div class="advice">💡 '+r.i+'</div>'+
      '<button class="replay" onclick="reset()">🔄 再测一次</button>'+
    '</div>';
}

function reset(){
  show('S');
}
</script>
</body>
</html>

<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>鲈鱼战术大师 AI</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        body { background-color: #f4f5f7; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; -webkit-tap-highlight-color: transparent; }
        .card { background: white; border-radius: 16px; box-shadow: 0 4px 20px rgba(0,0,0,0.03); overflow: hidden; }
        .select-btn { border: 1px solid #e5e7eb; transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1); }
        .select-btn.active { background-color: #0ea5e9; color: white; border-color: #0ea5e9; box-shadow: 0 4px 12px rgba(14, 165, 233, 0.3); transform: translateY(-1px); }
        .tab-btn { border-bottom: 2px solid transparent; color: #9ca3af; transition: all 0.3s; }
        .tab-btn.active { border-color: #0ea5e9; color: #0ea5e9; font-weight: 700; }
        .shimmer { animation: shimmer 2s infinite linear; background: linear-gradient(to right, #f6f7f8 0%, #edeef1 20%, #f6f7f8 40%, #f6f7f8 100%); background-size: 1000px 100%; }
        @keyframes shimmer { 0% { background-position: -1000px 0; } 100% { background-position: 1000px 0; } }
        .fade-in { animation: fadeIn 0.5s ease-out forwards; opacity: 0; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
    </style>
</head>
<body class="pb-32">

    <div id="setup-screen" class="p-6 max-w-lg mx-auto min-h-screen flex flex-col justify-center bg-white">
        <div class="mb-8">
            <h1 class="text-4xl font-black text-slate-800 tracking-tight">Bass<span class="text-sky-500">AI</span></h1>
            <p class="text-slate-400 font-medium">职业路亚向导系统 v3.0</p>
        </div>

        <div class="space-y-6">
            <div>
                <label class="text-xs font-bold text-slate-400 uppercase tracking-wider mb-2 block">做钓时段</label>
                <div class="grid grid-cols-4 gap-2">
                    <button onclick="setOption('time', '早上', this)" class="select-btn p-3 rounded-xl text-sm font-semibold">🌅 早上</button>
                    <button onclick="setOption('time', '中午', this)" class="select-btn p-3 rounded-xl text-sm font-semibold">☀️ 中午</button>
                    <button onclick="setOption('time', '下午', this)" class="select-btn p-3 rounded-xl text-sm font-semibold">🌇 下午</button>
                    <button onclick="setOption('time', '晚上', this)" class="select-btn p-3 rounded-xl text-sm font-semibold">🌙 晚上</button>
                </div>
            </div>

            <div>
                <label class="text-xs font-bold text-slate-400 uppercase tracking-wider mb-2 block">预计时长</label>
                <div class="grid grid-cols-4 gap-2">
                    <button onclick="setOption('duration', '1小时', this)" class="select-btn p-3 rounded-xl text-sm font-semibold">1h</button>
                    <button onclick="setOption('duration', '2小时', this)" class="select-btn p-3 rounded-xl text-sm font-semibold">2h</button>
                    <button onclick="setOption('duration', '3小时', this)" class="select-btn p-3 rounded-xl text-sm font-semibold">3h</button>
                    <button onclick="setOption('duration', '全天', this)" class="select-btn p-3 rounded-xl text-sm font-semibold">全天</button>
                </div>
            </div>

            <div class="grid grid-cols-2 gap-4">
                <div>
                    <label class="text-xs font-bold text-slate-400 uppercase tracking-wider mb-2 block">水域</label>
                    <div class="grid grid-cols-1 gap-2">
                        <button onclick="setOption('venue', '野钓自然水域', this)" class="select-btn p-3 rounded-xl text-sm font-semibold">🏞️ 野钓</button>
                        <button onclick="setOption('venue', '黑坑管理场', this)" class="select-btn p-3 rounded-xl text-sm font-semibold">🎣 管理场</button>
                    </div>
                </div>
                <div>
                    <label class="text-xs font-bold text-slate-400 uppercase tracking-wider mb-2 block">模式</label>
                    <div class="grid grid-cols-1 gap-2">
                        <button onclick="setOption('mode', '岸钓', this)" class="select-btn p-3 rounded-xl text-sm font-semibold">👟 岸钓</button>
                        <button onclick="setOption('mode', '船钓', this)" class="select-btn p-3 rounded-xl text-sm font-semibold">🚤 船钓</button>
                    </div>
                </div>
            </div>
        </div>

        <button onclick="startAnalysis()" class="mt-10 w-full bg-slate-900 text-white py-4 rounded-2xl font-bold text-lg shadow-xl shadow-slate-200 hover:bg-black transition-all active:scale-95 flex items-center justify-center gap-2">
            <span>开始分析环境</span> <i class="fas fa-satellite-dish"></i>
        </button>
        
        <p class="text-center text-xs text-gray-300 mt-4">Powered by DeepSeek AI & OpenWeather</p>
    </div>

    <div id="loading-screen" class="hidden fixed inset-0 bg-white z-50 flex flex-col items-center justify-center p-6">
        <div class="w-16 h-16 border-4 border-sky-100 border-t-sky-500 rounded-full animate-spin mb-6"></div>
        <h2 class="text-xl font-bold text-slate-800" id="loading-text">正在获取气象数据...</h2>
        <p class="text-slate-400 text-sm mt-2" id="loading-sub">连接气象卫星中</p>
    </div>

    <div id="dashboard-screen" class="hidden max-w-lg mx-auto min-h-screen relative">
        
        <div class="bg-white p-6 rounded-b-3xl shadow-sm z-20 sticky top-0 border-b border-gray-100">
            <div class="flex justify-between items-start mb-2">
                <div>
                    <div class="flex items-center gap-2 mb-1">
                        <i class="fas fa-location-arrow text-sky-500 text-xs"></i>
                        <span class="text-xs text-slate-400 uppercase tracking-wider font-bold">实时环境</span>
                    </div>
                    <div class="flex items-baseline gap-2">
                        <span class="text-3xl font-black text-slate-800" id="disp-temp">--°</span>
                        <span class="text-sm font-medium text-slate-500" id="disp-desc">--</span>
                    </div>
                </div>
                <div class="text-right">
                    <div class="bg-sky-50 px-3 py-1 rounded-lg inline-block">
                        <span class="text-sky-700 font-bold text-xl" id="disp-pressure">--</span>
                        <span class="text-sky-600 text-xs">hPa</span>
                    </div>
                    <p class="text-xs text-slate-400 mt-1" id="pressure-tip">气压分析中</p>
                </div>
            </div>
            
            <div class="flex gap-4 mt-3 pt-3 border-t border-gray-100">
                <div class="flex items-center gap-2 text-xs text-slate-500 font-medium">
                    <i class="fas fa-wind text-slate-300"></i> <span id="disp-wind">-- m/s</span>
                </div>
                <div class="flex items-center gap-2 text-xs text-slate-500 font-medium">
                    <i class="fas fa-tint text-slate-300"></i> <span id="disp-hum">--%</span>
                </div>
                <div class="ml-auto text-xs bg-slate-100 px-2 py-0.5 rounded text-slate-500" id="context-tag">--</div>
            </div>
        </div>

        <div class="bg-white/80 backdrop-blur-md sticky top-[135px] z-10 border-b border-gray-200 flex shadow-sm">
            <button onclick="renderTab('A')" id="tab-A" class="tab-btn active flex-1 py-3 text-sm text-center">方案 A<br><span class="text-[10px] font-normal opacity-70">首选推荐</span></button>
            <button onclick="renderTab('B')" id="tab-B" class="tab-btn flex-1 py-3 text-sm text-center">方案 B<br><span class="text-[10px] font-normal opacity-70">备用策略</span></button>
            <button onclick="renderTab('C')" id="tab-C" class="tab-btn flex-1 py-3 text-sm text-center">方案 C<br><span class="text-[10px] font-normal opacity-70">极限高压</span></button>
        </div>

        <div id="content-area" class="p-5 space-y-5 pb-24">
            </div>

        <div class="fixed bottom-6 left-5 right-5 max-w-[472px] mx-auto flex gap-3 z-30">
            <button onclick="retryStrategy()" class="flex-1 bg-slate-800 text-white py-3.5 rounded-2xl font-bold shadow-lg shadow-slate-300/50 active:scale-95 transition-transform flex items-center justify-center gap-2 text-sm">
                <i class="fas fa-sync-alt text-red-400"></i> 没钓到鱼，换策略
            </button>
            <button onclick="logCatch()" class="w-14 h-14 bg-sky-500 rounded-2xl shadow-lg shadow-sky-300/50 flex items-center justify-center text-white text-xl active:scale-90 transition-transform">
                <i class="fas fa-fish"></i>
            </button>
        </div>
    </div>

    <script>
        // ================= 配置区 =================
        // 1. DeepSeek API Key (请替换为您的 Key)
        // ⚠️ 安全提醒：在生产环境中，请勿将此 Key 暴露在客户端代码中！
        const GEMINI_API_KEY = 'AIzaSyCTCCwdPQbWXqWc7MgrVkhVG7S2FiuQQOo'; // 请务必替换为您的 DeepSeek Key
        
        // 2. OpenWeatherMap Key (请在这里填入你的 Key，否则无法获取真实天气)
        const WEATHER_API_KEY = '1e2e1b277a2de43bedf7c3c3e6a20028'; 

        // =========================================

        let userState = { time: '', duration: '', venue: '', mode: '' };
        let weatherData = null;
        let aiStrategies = null;
        let retryCount = 0;

        // 饵料图片字典 (关键词匹配)
        const lureImages = {
            'vib': 'https://images.unsplash.com/photo-1599496032734-75eb9949826d?w=200&h=200&fit=crop',
            'crank': 'https://plus.unsplash.com/premium_photo-1661962360408-012053073740?w=200&h=200&fit=crop', // 示意图
            'minnow': 'https://images.unsplash.com/photo-1582213782179-e0d53f98f2ca?w=200&h=200&fit=crop',
            'worm': 'https://images.unsplash.com/photo-1601633596590-7561f0d366a6?w=200&h=200&fit=crop', // 软虫
            'jig': 'https://images.unsplash.com/photo-1528607929212-2636ec44253e?w=200&h=200&fit=crop', // 亮片/Jig
            'topwater': 'https://images.unsplash.com/photo-1498611688622-c3681464455f?w=200&h=200&fit=crop',
            'default': 'https://images.unsplash.com/photo-1535591273665-5f5954ddfd85?w=200&h=200&fit=crop'
        };

        function setOption(key, value, btn) {
            userState[key] = value;
            btn.parentElement.querySelectorAll('button').forEach(b => b.classList.remove('active'));
            btn.classList.add('active');
        }

        async function startAnalysis() {
            if (!userState.time || !userState.duration || !userState.venue || !userState.mode) {
                alert('请完善所有选项，以便 AI 精准计算');
                return;
            }

            document.getElementById('setup-screen').classList.add('hidden');
            document.getElementById('loading-screen').classList.remove('hidden');

            // 1. 获取位置
            if (navigator.geolocation) {
                navigator.geolocation.getCurrentPosition(
                    async (pos) => { await fetchWeather(pos.coords.latitude, pos.coords.longitude); },
                    () => { handleWeatherError(); } // 拒绝权限或失败
                );
            } else {
                handleWeatherError();
            }
        }

        async function fetchWeather(lat, lon) {
            try {
                // 如果用户没填 KEY，直接用模拟数据
                if (WEATHER_API_KEY === 'YOUR_OPENWEATHER_KEY') throw new Error("No Key");

                const res = await fetch(`https://api.openweathermap.org/data/2.5/weather?lat=${lat}&lon=${lon}&appid=${WEATHER_API_KEY}&units=metric`);
                if (!res.ok) throw new Error("Weather API Error");
                
                const data = await res.json();
                weatherData = {
                    temp: Math.round(data.main.temp),
                    pressure: data.main.pressure,
                    desc: data.weather[0].description,
                    wind: data.wind.speed,
                    hum: data.main.humidity
                };
            } catch (e) {
                console.warn("使用模拟天气数据");
                weatherData = { temp: 24, pressure: 1012, desc: "模拟多云", wind: 3.5, hum: 60 };
            }

            updateWeatherUI();
            document.getElementById('loading-text').innerText = "AI 正在制定战术...";
            document.getElementById('loading-sub').innerText = "分析气压与鱼层关系";
            await callGeminiAPI();
        }

        function handleWeatherError() {
            weatherData = { temp: 25, pressure: 1010, desc: "默认天气", wind: 2, hum: 50 };
            updateWeatherUI();
            document.getElementById('loading-text').innerText = "AI 正在制定战术...";
            callGeminiAPI();
        }

        function updateWeatherUI() {
            document.getElementById('disp-temp').innerText = weatherData.temp + "°";
            document.getElementById('disp-desc').innerText = weatherData.desc;
            document.getElementById('disp-pressure').innerText = weatherData.pressure;
            document.getElementById('disp-wind').innerText = weatherData.wind + " m/s";
            document.getElementById('disp-hum').innerText = weatherData.hum + "%";
            document.getElementById('context-tag').innerText = `${userState.venue} · ${userState.mode}`;
            
            // 简单的气压判断
            const p = weatherData.pressure;
            const tip = p < 1000 ? "气压低，鱼口慢" : (p > 1015 ? "气压高，活性好" : "气压稳定");
            document.getElementById('pressure-tip').innerText = tip;
        }

        // ================= 核心：调用 DeepSeek (已修改为 DeepSeek API，并优化提示词) =================
        async function callGeminiAPI(isRetry = false) {
            // DeepSeek 的 System Role 提示词，要求模型只输出 JSON
            const systemPrompt = "你是一个职业鲈鱼（Bass）钓鱼向导。请只输出JSON格式的响应，不要包含任何额外文字或Markdown格式（如 ```json...```）。";
            
            const userPrompt = `
                ${isRetry ? '注意：用户刚才按照建议没钓到鱼，请分析原因（可能是鱼层变了或颜色不对），给出更精细或完全不同的调整方案。' : ''}
                
                环境数据：
                - 气温：${weatherData.temp}°C
                - 气压：${weatherData.pressure} hPa (非常重要，低气压鱼离底，高气压鱼活跃)
                - 天气：${weatherData.desc}
                - 风速：${weatherData.wind} m/s
                
                用户设置：
                - 时间：${userState.time}
                - 预计时长：${userState.duration}
                - 场地：${userState.venue}
                - 模式：${userState.mode}

                请根据以上环境和用户设置，生成一个JSON格式的响应，包含A、B、C三个方案。
                
                // ！！！重点强调颜色和尺寸的推荐，确保模型不会遗漏！！！
                JSON结构必须如下：
                {
                    "strategies": {
                        "A": {
                            "name": "方案名(如: 强力搜索)",
                            "desc": "简短描述为什么选这个",
                            "timeline": [
                                {"time": "前30分钟", "action": "具体操作建议", "lure": "推荐饵名"}
                            ],
                            "baits": [
                                {"brand": "品牌(如Jackall)", "model": "型号(TN60)", "type": "类型(VIB/Minnow/Worm)", "color": "推荐颜色（必须提供，如：西瓜红/银色）", "size": "尺寸（必须提供，如：7克/100mm）", "technique": "手法(平收/跳底)"}
                            ]
                        },
                        "B": { ...同上 },
                        "C": { ...同上 }
                    }
                }
                确保饵的推荐具体到品牌和型号。根据时长 ${userState.duration} 合理安排 timeline。
            `;

            try {
                // *** DeepSeek API 地址和请求头修改 ***
                const response = await fetch(`https://api.deepseek.com/chat/completions`, {
                    method: 'POST',
                    headers: { 
                        'Content-Type': 'application/json',
                        'Authorization': `Bearer ${GEMINI_API_KEY}` // DeepSeek 使用 Bearer Token 认证
                    },
                    body: JSON.stringify({
                        model: 'deepseek-chat', // DeepSeek 推荐模型
                        messages: [
                            { role: "system", content: systemPrompt },
                            { role: "user", content: userPrompt }
                        ],
                        response_format: { type: "json_object" } 
                    })
                });

                // 增加错误处理
                if (!response.ok) {
                    const errorData = await response.json();
                    const errorMessage = errorData.error ? errorData.error.message : '未知错误';
                    throw new Error(`DeepSeek API 请求失败，状态码: ${response.status}。详情: ${errorMessage}`);
                }
                
                const data = await response.json();
                
                // DeepSeek/OpenAI 兼容响应体解析
                if (!data.choices || data.choices.length === 0 || !data.choices[0].message || !data.choices[0].message.content) {
                    throw new Error("API 响应中缺少内容，请检查模型、Key 或提示词。");
                }

                const jsonText = data.choices[0].message.content.trim();
                aiStrategies = JSON.parse(jsonText).strategies;

                document.getElementById('loading-screen').classList.add('hidden');
                document.getElementById('dashboard-screen').classList.remove('hidden');
                
                renderTab(isRetry ? 'C' : 'A');
                if(isRetry) alert("DeepSeek AI 已重新分析环境，为您切换到高压精细方案 (方案 C)");

            } catch (error) {
                console.error("DeepSeek API 调用错误:", error);
                alert("AI 连接失败，请检查网络、DeepSeek Key 是否正确。详细错误请查看控制台。");
                document.getElementById('loading-screen').classList.add('hidden');
            }
        }

        // ================= 渲染逻辑 (保持不变) =================
        function renderTab(plan) {
            // Tab 样式
            ['A', 'B', 'C'].forEach(p => {
                const btn = document.getElementById(`tab-${p}`);
                if (p === plan) btn.classList.add('active');
                else btn.classList.remove('active');
            });

            const data = aiStrategies[plan];
            const container = document.getElementById('content-area');

            // 生成时间轴 HTML
            let timelineHtml = data.timeline.map((item, idx) => `
                <div class="flex gap-4 relative">
                    ${idx !== data.timeline.length - 1 ? '<div class="absolute left-[11px] top-7 bottom-[-16px] w-[2px] bg-slate-100"></div>' : ''}
                    <div class="w-6 h-6 rounded-full bg-sky-100 text-sky-600 flex items-center justify-center text-xs font-bold shrink-0 mt-1">${idx + 1}</div>
                    <div class="pb-6">
                        <div class="text-xs font-bold text-slate-400 uppercase mb-1">${item.time}</div>
                        <div class="text-slate-800 text-sm font-medium leading-relaxed">${item.action}</div>
                        <div class="text-sky-600 text-xs mt-1 font-bold"><i class="fas fa-link"></i> ${item.lure}</div>
                    </div>
                </div>
            `).join('');

            // 生成饵料卡片 HTML
            let baitsHtml = data.baits.map(bait => {
                // 简单的图片匹配逻辑
                let imgKey = 'default';
                const typeLower = (bait.type + bait.model).toLowerCase();
                if (typeLower.includes('vib')) imgKey = 'vib';
                else if (typeLower.includes('worm') || typeLower.includes('senko') || typeLower.includes('虫')) imgKey = 'worm';
                else if (typeLower.includes('minnow') || typeLower.includes('米诺')) imgKey = 'minnow';
                else if (typeLower.includes('jig') || typeLower.includes('铅头')) imgKey = 'jig';

                return `
                <div class="card p-3 flex gap-3 border border-gray-100">
                    <div class="w-20 h-20 bg-gray-100 rounded-lg bg-cover bg-center shrink-0" style="background-image: url('${lureImages[imgKey]}')"></div>
                    <div class="flex-1 min-w-0">
                        <div class="flex justify-between items-start">
                            <h4 class="font-bold text-slate-800 truncate text-sm">${bait.brand} ${bait.model}</h4>
                        </div>
                        <p class="text-xs text-slate-500 mt-1">类型: ${bait.type}</p>
                        <div class="flex flex-wrap gap-1 mt-2">
                            <span class="text-[10px] bg-sky-50 text-sky-700 px-1.5 py-0.5 rounded border border-sky-100">${bait.color}</span>
                            <span class="text-[10px] bg-gray-50 text-gray-600 px-1.5 py-0.5 rounded border border-gray-200">${bait.size}</span>
                        </div>
                        <p class="text-[10px] text-orange-500 mt-1.5 font-bold"><i class="fas fa-bolt"></i> ${bait.technique}</p>
                    </div>
                </div>
                `;
            }).join('');

            // 注入 DOM
            container.innerHTML = `
                <div class="card p-5 bg-gradient-to-br from-white to-slate-50 border border-slate-100 fade-in">
                    <h3 class="font-bold text-lg text-slate-800 mb-1">${data.name}</h3>
                    <p class="text-sm text-slate-500 leading-relaxed">${data.desc}</p>
                </div>

                <div class="fade-in" style="animation-delay: 0.1s">
                    <h4 class="font-bold text-slate-800 mb-3 text-sm flex items-center gap-2"><i class="far fa-clock text-sky-500"></i> 时间轴部署</h4>
                    <div class="card p-5 border border-slate-100">${timelineHtml}</div>
                </div>

                <div class="fade-in" style="animation-delay: 0.2s">
                    <h4 class="font-bold text-slate-800 mb-3 text-sm flex items-center gap-2"><i class="fas fa-box-open text-sky-500"></i> 推荐装备 (点击淘宝搜同款)</h4>
                    <div class="space-y-3">${baitsHtml}</div>
                </div>
            `;
        }

        function retryStrategy() {
            if(!confirm("确定要重新生成策略吗？AI 将分析刚才为什么没口。")) return;
            document.getElementById('loading-screen').classList.remove('hidden');
            document.getElementById('dashboard-screen').classList.add('hidden');
            document.getElementById('loading-text').innerText = "正在进行战术复盘...";
            document.getElementById('loading-sub').innerText = "AI 正在推演鱼情变化";
            
            retryCount++;
            callGeminiAPI(true); // 传入 true 表示重试模式
        }

        function logCatch() {
            alert("🎉 恭喜中鱼！\n\n位置和时间已记录到本地。\nAI 学习了这次成功的模式，下次推荐将更精准。");
        }
    </script>
</body>
</html>

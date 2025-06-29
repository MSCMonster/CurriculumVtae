# Curriculum Vitae

这是我的 HTML 简历模板（已脱敏）

👉 [点击此处在线预览简历](https://mscmonster.github.io/CurriculumVtae/)


```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>个人简历 - □□□</title>
    <!-- 引入Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- 引入图标库 -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- 引入思源黑体字体 -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@300;400;500;700&display=swap"
        rel="stylesheet">
    <style>
        /* 自定义样式 */
        body {
            font-family: 'Noto Sans SC', sans-serif;
            background-color: #f0f2f5;
            /* 页面背景色 */
        }

        /* A4纸张容器样式 (调整了上下边距) */
        .a4-container {
            width: 210mm;
            min-height: 297mm;
            padding: 15mm 18mm;
            /* 上下边距从20mm减为15mm */
            margin: 2rem auto;
            background: white;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }

        /* 章节标题样式 (减小了字号和下边距) */
        .section-title {
            font-size: 1.2rem;
            /* 从1.3rem减小 */
            font-weight: 700;
            color: #1a202c;
            padding-bottom: 0.4rem;
            /* 从0.5rem减小 */
            border-bottom: 2.5px solid #2d3748;
            margin-bottom: 1rem;
            /* 从1.25rem减小 */
            display: flex;
            align-items: center;
        }

        .section-title i {
            margin-right: 0.75rem;
            color: #2d3748;
        }

        /* 列表项样式 (减小了下边距) */
        .list-item {
            position: relative;
            padding-left: 1.25rem;
            /* 稍微减小 */
            margin-bottom: 0.5rem;
            /* 从0.75rem减小 */
        }

        .list-item::before {
            content: '●';
            position: absolute;
            left: 0;
            top: 1px;
            font-size: 0.8em;
            color: #4a5568;
        }

        .list-item::marker {
            content: '';
            display: none;
            /* position: absolute; */
            /* left: 0; */
            /* top: 1px; */
            /* font-size: 0.8em; */
            /* color: #4a5568; */
        }

        /* 打印按钮样式 */
        .print-button {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background-color: #2d3748;
            color: white;
            border: none;
            padding: 1rem 1.5rem;
            border-radius: 9999px;
            font-size: 1rem;
            cursor: pointer;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
            transition: all 0.3s ease;
            z-index: 100;
        }

        .print-button:hover {
            background-color: #1a202c;
            transform: translateY(-2px);
        }

        /* 打印媒体查询 */
        @media print {
            body {
                background-color: white;
            }

            .a4-container {
                margin: 0;
                padding: 0mm 18mm !important;
                /* 确保打印时也使用紧凑边距 */
                box-shadow: none;
                width: 100%;
                min-height: auto;
            }

            .print-button {
                display: none;
            }

            /* 确保打印时文本为黑色，避免浏览器默认行为导致颜色变淡 */
            * {
                color: #000 !important;
                -webkit-print-color-adjust: exact;
                print-color-adjust: exact;
            }
        }
    </style>
</head>

<body>

    <!-- 打印按钮 -->
    <button onclick="window.print()" class="print-button">
        <i class="fas fa-print mr-2"></i> 打印 / 另存为PDF
    </button>

    <!-- A4简历容器 -->
    <div class="a4-container">
        <!-- 个人信息 -->
        <header class="text-gray-800 mb-6">
            <!-- 主标题 -->
            <h1 class="text-center text-4xl font-bold text-gray-900 mb-6">个人简历</h1>

            <div class="flex items-center mb-2">
                <h2 class="text-3xl font-semibold text-gray-800">□□□</h2>
                <span class="text-base font-medium text-gray-700 ml-6 bg-gray-100 px-3 py-1 rounded-md">中共党员</span>
            </div>

            <div class="flex justify-between items-start border-t border-gray-300 ">

                <div class="flex-grow">

                    <div class="pt-4">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-x-8 gap-y-3 text-sm text-gray-600">
                            <div class="flex items-center"><i
                                    class="fas fa-briefcase w-5 text-center mr-2 text-gray-500"></i>求职意向：□□□□□□□ /
                                □□□□□□ / □□□□□□□□□□□</div>
                            <div class="flex items-center"><i
                                    class="fas fa-phone w-5 text-center mr-2 text-gray-500"></i>联系电话：□□□□□□□□□□□</div>
                            <div class="flex items-center"><i
                                    class="fas fa-map-marker-alt w-5 text-center mr-2 text-gray-500"></i>居住地：□□□□□□□□□
                            </div>
                            <div class="flex items-center"><i
                                    class="fas fa-envelope w-5 text-center mr-2 text-gray-500"></i>电子邮箱：□□□□□□□□□□@qq.com
                            </div>
                            <div class="flex items-center col-span-full"><i
                                    class="fas fa-paper-plane w-5 text-center mr-2 text-gray-500"></i>意向工作地：□□□□□□,
                                □□□□□□</div>
                        </div>
                    </div>

                </div>
                <!-- 右侧：证件照 -->
                <div class="ml-8 flex-shrink-0">
                    <!-- 请将下面的 src 替换为您自己的证件照图片链接 -->
                    <img src="" alt="证件照"
                        class="w-32 h-auto rounded-lg shadow-md object-cover">
                </div>

            </div>

        </header>


        <!-- 教育背景 -->
        <section class="mb-6">
            <h2 class="section-title"><i class="fas fa-graduation-cap"></i>教育背景</h2>
            <div class="flex justify-between items-start mb-2">
                <p class="text-lg font-semibold">□□□□□大学 <span class="text-base font-normal text-gray-600 ml-2">| □□□□□□
                        | 本科</span></p>
                <p class="text-gray-600 font-medium">应届毕业生 (2025年6月毕业)</p>
            </div>
            <ul class="text-gray-700 space-y-2">
                <li class="list-item">
                    <strong>主修课程：</strong>□□□□□□□、□□□□□□、□□□□□□□□、□□□□□□、□□□□□□、□□□□、□□□□□□、□□□□□□□、□□□□。</li>
                <li class="list-item">
                    <strong>毕业设计：</strong>《□□□□□□□□□□》
                    <ul class="mt-2 pl-4 text-sm space-y-1 text-gray-600">
                        <li><strong>设计目标：</strong>□□□□□□□□□□□□□□，□□□□□□□□。</li>
                        <li><strong>设计产出：</strong>□□□□□□、□□□□□□、□□□□/□□、□□□□□□□□、□□□□□□□、□□□□□□□□。</li>
                        <li><strong>核心亮点：</strong>□□□□□□□□（□□），□□□□□□□□□□□□□□，□□□□□□□□□□□□□。</li>
                    </ul>
                </li>
            </ul>
        </section>

        <!-- 专业技能 -->
        <section class="mb-6">
            <h2 class="section-title"><i class="fas fa-tools"></i>专业技能</h2>
            <div class="space-y-3 text-gray-700">
                <div class="list-item"><strong>设计软件：</strong>
                    <p class="mt-1 text-sm text-gray-600">
                        <strong>精通：</strong>□□□□□ □□□□□□□, □□□□□ □□□□□□□□, □□□□□□□ □□□□□□□□<br>
                        <strong>熟练：</strong>□□□□□, □□□□□□□□, □□□□□□□□<br>
                        <strong>掌握：</strong>□□□□ □□□□, □□□□, □□□□□□□□</p>
                </div>
                <div class="list-item"><strong>设计能力：</strong>
                    <p class="mt-1 text-sm text-gray-600"><strong>□□□□□□：</strong> □□、□□、□□、□□、□□□□□。<br><strong>□□□□□□
                            (□□□)：</strong> □□□□□、□□□□□□□□□（□□□□□□）。<br><strong>UI/□□□□：</strong>
                        □□□□□□□□、□□□□□□□□□□□□、□□□□□□。<br><strong>□□□□□：</strong> □□□□□、□□□□□。<br><strong>□□□□：</strong>
                        □□□□、□□□□□□□（□□□□□□）。</p>
                </div>
            </div>
        </section>
        <br>

        <!-- 项目经验 -->
        <section class="mb-6">
            <h2 class="section-title"><i class="fas fa-tasks"></i>项目经验</h2>
            <div class="space-y-4">
                <div>
                    <div class="flex justify-between items-baseline mb-1">
                        <h3 class="font-semibold text-base">“□□”□□□□□□/□□□□□□ (□□□□)</h3>
                        <p class="text-sm text-gray-500">核心成员 | 2022.6</p>
                    </div>
                    <ul class="list-disc pl-5 text-sm text-gray-600 space-y-1">
                        <li>□□□□□□□□□□□□□，<strong>□□□□□□□□</strong>。</li>
                        <li><strong>主要贡献：</strong>□□□□□□，□□□□□□，<strong>□□□□□□□□□□□□□</strong>，□□□□□□□□□□□□□□□。</li>
                    </ul>
                </div>
                <div>
                    <div class="flex justify-between items-baseline mb-1">
                        <h3 class="font-semibold text-base">“□□□”□□□□□□□□□□□ (□□□□)</h3>
                        <p class="text-sm text-gray-500">独立完成 | 2023.6</p>
                    </div>
                    <ul class="list-disc pl-5 text-sm text-gray-600 space-y-1">
                        <li><strong>独立设计</strong>□□□□□□□□□□□□，□□□□“□”、“□□”、“□”□□□□□□，□□□□□□□□□□□。</li>
                    </ul>
                </div>
                <div>
                    <div class="flex justify-between items-baseline mb-1">
                        <h3 class="font-semibold text-base">“□□□□”□□□□□□□□ (□□□□□□□□)</h3>
                        <p class="text-sm text-gray-500">设计者 | 2023.12</p>
                    </div>
                    <ul class="list-disc pl-5 text-sm text-gray-600 space-y-1">
                        <li><strong>独立完成</strong>□□□□□□□□□□□□□□□</li>
                        <li><strong>设计目标</strong>□□□□□□□□□□（□□□□□□□□□□□□□□），<strong>□□□□□□□□，□□□□□□□□</strong></li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- 实践经历 -->
        <section class="mb-6">
            <h2 class="section-title"><i class="fas fa-briefcase-medical"></i>实践经历</h2>
            <div class="space-y-4">
                <div>
                    <div class="flex justify-between items-baseline mb-1">
                        <h3 class="font-semibold text-base">□□□□□□□□□□□ | □□助理</h3>
                        <p class="text-sm text-gray-500">2024.10 - 2025.1</p>
                    </div>
                    <ul class="list-disc pl-5 text-sm text-gray-600 space-y-1">
                        <li>□□□□□□□□□□□□□□，□□□□□□、□□□□、□□□□□□，□□□□□□□□□□。</li>
                    </ul>
                </div>
                <div>
                    <div class="flex justify-between items-baseline mb-1">
                        <h3 class="font-semibold text-base">□□□□□ | 副部长</h3>
                        <p class="text-sm text-gray-500">2022.11 - 2023.10</p>
                    </div>
                    <ul class="list-disc pl-5 text-sm text-gray-600 space-y-1">
                        <li><strong>□□□□</strong>□□□□□□，□□□□□□□□□□□□□□□□，□□□□□□□□□□□□□□□□。</li>
                    </ul>
                </div>
                <div>
                    <div class="flex justify-between items-baseline mb-1">
                        <h3 class="font-semibold text-base">□□□ | 副部长</h3>
                        <p class="text-sm text-gray-500">2024.11 - 2024.10</p>
                    </div>
                    <ul class="list-disc pl-5 text-sm text-gray-600 space-y-1">
                        <li>□□□□□□，<strong>□□□□□□□□□□□□□□□□□</strong>，□□□□□□。</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- 奖项荣誉 & 证书 -->
        <section class="mb-6">
            <h2 class="section-title"><i class="fas fa-award"></i>奖项荣誉 & 证书</h2>
            <ul class="list-disc pl-5 text-sm text-gray-700 grid grid-cols-1 md:grid-cols-2 gap-x-8 gap-y-2">
                <li>□□□□□□□□□□□</li>
                <li>□□□□□□□□□□□□□□□□□□奖 (2023)</li>
                <li>□□□□□□□□□□□□二等奖 (2023.01)</li>
                <li>□□□□□□□□□□□□□□□□□荣誉证书 (2023.01)</li>
                <li>□□□□□□二等奖 (2021.11)</li>
            </ul>
        </section>

        <!-- 自我评价 -->
        <section>
            <h2 class="section-title"><i class="fas fa-user-check"></i>自我评价</h2>
            <p class="text-gray-700 leading-relaxed text-justify">
                <strong>中共党员，□□□□□□□专业应届毕业生</strong>。具备扎实的□□□□□□□□□□与□□□□□□□□，精通□□□□□ □□□□□□□□，熟练使用□□□、□□□□□等主流□□□□工具及□□□□□软件。通过系统的□□□□□□□，<strong>熟练掌握□□□□□□□□、□□□□□□□□□□及□□□□□□的核心方法</strong>。毕业设计展现了将□□□□□□□□融入□□□□、解决□□□□□□□。担任□□□□□□□副部长期间，<strong>独立负责□□□□□□□□□</strong>，锻炼了□□□□□□□□□□□能力与□□□□□□意识。责任心强，学习能力突出，对□□□□□与□□□□□领域充满热情，渴望运用□□□□□服务于□□□□□□□□与□□□□。
            </p>

        </section>

    </div>

</body>

</html>

```

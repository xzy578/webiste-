# 网站-<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>孙家豪的个人简历</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #3498db;
            --secondary-color: #2ecc71;
            --danger-color: #e74c3c;
            --light-gray: #f8f9fa;
            --dark-gray: #343a40;
            --border-color: #dee2e6;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', 'Microsoft YaHei', Arial, sans-serif;
            line-height: 1.6;
            color: var(--dark-gray);
            background-color: #f5f7fa;
            padding: 20px;
        }
        
        .resume-container {
            max-width: 1000px;
            margin: 0 auto;
            background: white;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            overflow: hidden;
        }
        
        /* 头部样式 - 增强效果 */
        .resume-header {
            background: linear-gradient(135deg, #3498db, #2c3e50);
            color: white;
            text-align: center;
            padding: 40px 20px;
            position: relative;
        }
        
        .resume-header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }
        
        .resume-header h1:hover {
            transform: translateY(-8px);
            text-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
        }
        
        .resume-header h1 i {
            transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }
        
        .resume-header h1:hover i {
            transform: rotate(25deg) scale(1.3);
        }
        
        .resume-header p {
            font-size: 1.2em;
            opacity: 0.9;
        }
        
        /* 主要内容区域 */
        .resume-content {
            display: flex;
            flex-wrap: wrap;
            padding: 30px;
        }
        
        /* 左侧个人信息区域 */
        .personal-info {
            flex: 1;
            min-width: 300px;
            padding-right: 30px;
        }
        
        /* 右侧详细信息区域 */
        .detail-info {
            flex: 2;
            min-width: 400px;
        }
        
        /* 信息卡片样式 - 增强效果 */
        .info-card {
            background: white;
            border-radius: 8px;
            padding: 25px;
            margin-bottom: 30px;
            box-shadow: 0 3px 15px rgba(0, 0, 0, 0.05);
            transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }
        
        .info-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
        }
        
        .info-card h2 {
            color: var(--primary-color);
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--light-gray);
            display: flex;
            align-items: center;
            transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }
        
        .info-card h2:hover {
            transform: rotate(5deg) scale(1.02);
        }
        
        .info-card h2 i {
            margin-right: 10px;
            transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }
        
        .info-card h2:hover i {
            transform: rotate(25deg) scale(1.3);
        }
        
        /* 照片区域 - 增强效果 */
        .photo-container {
            text-align: center;
            margin-bottom: 30px;
        }
        
        .photo {
            width: 180px;
            height: 240px;
            object-fit: cover;
            border-radius: 8px;
            border: 5px solid white;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
            transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }
        
        .photo:hover {
            transform: scale(1.1) rotate(5deg);
            box-shadow: 0 12px 30px rgba(0, 0, 0, 0.2);
        }
        
        /* 基本信息列表 - 增强效果 */
        .info-list {
            list-style: none;
        }
        
        .info-list li {
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            transition: all 0.3s ease;
        }
        
        .info-list li i {
            width: 30px;
            color: var(--primary-color);
            font-size: 1.2em;
            transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }
        
        .info-list li:hover i {
            transform: scale(1.5) rotate(15deg);
        }
        
        .info-label {
            font-weight: 600;
            width: 100px;
            color: var(--dark-gray);
        }
        
        /* 可编辑字段样式 */
        .editable {
            border: 1px solid var(--primary-color);
            border-radius: 4px;
            padding: 8px 12px;
            background-color: white;
            font-size: 15px;
            transition: all 0.3s ease;
        }
        
        .editable:focus {
            outline: none;
            box-shadow: 0 0 0 3px rgba(52, 152, 219, 0.2);
        }
        
        select.editable {
            appearance: none;
            background-image: url("data:image/svg+xml;charset=UTF-8,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='currentColor' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3e%3cpolyline points='6 9 12 15 18 9'%3e%3c/polyline%3e%3c/svg%3e");
            background-repeat: no-repeat;
            background-position: right 10px center;
            background-size: 14px;
            padding-right: 30px;
        }
        
        /* 技能和爱好列表 - 增强效果 */
        .skills-list, .hobbies-list {
            list-style: none;
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }
        
        .skill-item, .hobby-item {
            background-color: #f1f8fe;
            padding: 8px 15px;
            border-radius: 20px;
            display: flex;
            align-items: center;
            transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }
        
        .skill-item:hover, .hobby-item:hover {
            background-color: #e1f0fa;
            transform: translateY(-5px);
        }
        
        .skill-item i, .hobby-item i {
            margin-right: 8px;
            color: var(--primary-color);
            transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }
        
        .skill-item:hover i, .hobby-item:hover i {
            transform: rotate(25deg) scale(1.3);
        }
        
        /* 项目经历和自我评价 */
        .experience-text, .evaluation-text {
            line-height: 1.8;
        }
        
        /* 按钮区域 - 增强效果 */
        .action-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            padding: 30px;
            background-color: var(--light-gray);
        }
        
        .btn {
            padding: 12px 28px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-size: 16px;
            font-weight: 500;
            transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            display: flex;
            align-items: center;
        }
        
        .btn i {
            margin-right: 8px;
            transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }
        
        .btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
        }
        
        .btn:hover i {
            transform: rotate(360deg) scale(1.3);
        }
        
        .btn-save {
            background-color: var(--secondary-color);
            color: white;
        }
        
        .btn-reset {
            background-color: var(--danger-color);
            color: white;
        }
        
        /* 保存状态提示 */
        .save-status {
            text-align: center;
            margin-top: 15px;
            font-size: 14px;
            color: var(--secondary-color);
            height: 20px;
            transition: all 0.3s ease;
        }
        
        /* 响应式设计 */
        @media (max-width: 768px) {
            .resume-content {
                flex-direction: column;
            }
            
            .personal-info, .detail-info {
                padding-right: 0;
                min-width: 100%;
            }
            
            .action-buttons {
                flex-direction: column;
                gap: 15px;
            }
            
            .btn {
                width: 100%;
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <div class="resume-container">
        <!-- 头部区域 -->
        <div class="resume-header">
            <h1><i class="fas fa-user"></i> 孙家豪的个人简历</h1>
            <p>软件工程专业 | 信息与电气工程学院</p>
        </div>
        
        <!-- 主要内容区域 -->
        <div class="resume-content">
            <!-- 左侧个人信息 -->
            <div class="personal-info">
                <!-- 照片 -->
                <div class="photo-container">
                    <img src="lab1.bmp.jpg.jpg" alt="个人照片" class="photo">
                </div>
                
                <!-- 基本信息 -->
                <div class="info-card">
                    <h2><i class="fas fa-id-card"></i> 基本信息</h2>
                    <ul class="info-list">
                        <li>
                            <i class="fas fa-signature"></i>
                            <span class="info-label">姓名:</span>
                            <span>孙家豪</span>
                        </li>
                        <li>
                            <i class="fas fa-venus-mars"></i>
                            <span class="info-label">性别:</span>
                            <select class="editable" id="gender">
                                <option value="male" selected>男</option>
                                <option value="female">女</option>
                            </select>
                        </li>
                        <li>
                            <i class="fas fa-birthday-cake"></i>
                            <span class="info-label">年龄:</span>
                            <input type="number" class="editable" id="age" value="19" min="18" max="70">
                        </li>
                        <li>
                            <i class="fas fa-map-marker-alt"></i>
                            <span class="info-label">籍贯:</span>
                            <span>山东莱州</span>
                        </li>
                        <li>
                            <i class="fas fa-phone"></i>
                            <span class="info-label">电话:</span>
                            <span>150xxxxxxx2</span>
                        </li>
                        <li>
                            <i class="fas fa-envelope"></i>
                            <span class="info-label">邮箱:</span>
                            <span>489443928@qq.com</span>
                        </li>
                        <li>
                            <i class="fas fa-heartbeat"></i>
                            <span class="info-label">健康状况:</span>
                            <select class="editable" id="health">
                                <option value="excellent" selected>优秀</option>
                                <option value="good">良好</option>
                                <option value="fair">一般</option>
                            </select>
                        </li>
                        <li>
                            <i class="fas fa-heart"></i>
                            <span class="info-label">婚姻状况:</span>
                            <select class="editable" id="marriage">
                                <option value="single" selected>未婚</option>
                                <option value="married">已婚</option>
                                <option value="divorced">离异</option>
                            </select>
                        </li>
                    </ul>
                </div>
                
                <!-- 求职意向 -->
                <div class="info-card">
                    <h2><i class="fas fa-briefcase"></i> 求职意向</h2>
                    <p>软件工程师</p>
                </div>
            </div>
            
            <!-- 右侧详细信息 -->
            <div class="detail-info">
                <!-- 教育背景 -->
                <div class="info-card">
                    <h2><i class="fas fa-graduation-cap"></i> 教育背景</h2>
                    <ul class="info-list">
                        <li>
                            <i class="fas fa-university"></i>
                            <span class="info-label">学校:</span>
                            <span>信息与电气工程学院</span>
                        </li>
                        <li>
                            <i class="fas fa-book"></i>
                            <span class="info-label">专业:</span>
                            <span>软件工程</span>
                        </li>
                        <li>
                            <i class="fas fa-award"></i>
                            <span class="info-label">学历:</span>
                            <span>本科</span>
                        </li>
                    </ul>
                </div>
                
                <!-- 技能证书 -->
                <div class="info-card">
                    <h2><i class="fas fa-certificate"></i> 技能证书</h2>
                    <ul class="skills-list">
                        <li class="skill-item">
                            <i class="fas fa-language"></i> 英语四级(CET4)
                        </li>
                        <li class="skill-item">
                            <i class="fas fa-laptop-code"></i> 计算机二级(Java)
                        </li>
                        <li class="skill-item">
                            <i class="fab fa-java"></i> Java编程
                        </li>
                        <li class="skill-item">
                            <i class="fab fa-python"></i> Python编程
                        </li>
                        <li class="skill-item">
                            <i class="fab fa-html5"></i> HTML/CSS
                        </li>
                        <li class="skill-item">
                            <i class="fab fa-js"></i> JavaScript
                        </li>
                    </ul>
                </div>
                
                <!-- 个人特长与爱好 -->
                <div class="info-card">
                    <h2><i class="fas fa-star"></i> 特长爱好</h2>
                    <ul class="hobbies-list">
                        <li class="hobby-item">
                            <i class="fas fa-code"></i> 编程开发
                        </li>
                        <li class="hobby-item">
                            <i class="fas fa-futbol"></i> 足球
                        </li>
                        <li class="hobby-item">
                            <i class="fas fa-swimmer"></i> 游泳
                        </li>
                        <li class="hobby-item">
                            <i class="fas fa-camera"></i> 摄影
                        </li>
                        <li class="hobby-item">
                            <i class="fas fa-book-reader"></i> 阅读
                        </li>
                        <li class="hobby-item">
                            <i class="fas fa-plane"></i> 旅游
                        </li>
                    </ul>
                </div>
                
                <!-- 项目经历 -->
                <div class="info-card">
                    <h2><i class="fas fa-project-diagram"></i> 项目经历</h2>
                    <div class="experience-text">
                        <p>无</p>
                    </div>
                </div>
                
                <!-- 自我评价 -->
                <div class="info-card">
                    <h2><i class="fas fa-comment"></i> 自我评价</h2>
                    <div class="evaluation-text">
                        <p>本人学习能力强，对软件开发有浓厚兴趣，在校期间成绩优异。积极参与各类编程竞赛。</p>
                        <p>具备良好的团队协作精神和沟通能力，在项目开发中能够承担关键模块的开发任务。适应能力强，能够快速学习新技术并应用到实际开发中。</p>
                        <p>工作认真负责，注重代码质量和开发规范，有良好的问题解决能力和抗压能力。</p>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- 表单操作按钮 -->
        <form id="resumeForm">
            <div class="action-buttons">
                <button type="button" class="btn btn-save" id="saveBtn">
                    <i class="fas fa-save"></i> 保存修改
                </button>
                <button type="button" class="btn btn-reset" id="resetBtn">
                    <i class="fas fa-undo"></i> 重置修改
                </button>
            </div>
            <div class="save-status" id="saveStatus"></div>
        </form>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const saveBtn = document.getElementById('saveBtn');
            const resetBtn = document.getElementById('resetBtn');
            const saveStatus = document.getElementById('saveStatus');
            
            // 可编辑字段
            const editableFields = {
                gender: 'male',
                age: 19,
                health: 'excellent',
                marriage: 'single'
            };
            
            // 保存数据到localStorage
            function saveFormData() {
                const formData = {};
                
                // 获取当前可编辑字段的值
                for (const field in editableFields) {
                    const element = document.getElementById(field);
                    if (element) {
                        formData[field] = element.value;
                    }
                }
                
                localStorage.setItem('resumeData', JSON.stringify(formData));
                showSaveStatus('已修改并保存', true);
            }
            
            // 从localStorage加载数据
            function loadFormData() {
                const savedData = localStorage.getItem('resumeData');
                if (保存的数据) {
                    const formData = JSON.parse(savedData);
                    
                    for (const field in formData) {
                        const element = document.getElementById(field);
                        if (元素) {
                            element.value = formData[field];
                        }
                    }
                    
                    showSaveStatus('已加载上次保存的修改', true);
                }
            }
            
            // 重置为默认值
            function resetToDefault() {
                for (const field in editableFields) {
                    const element = document.getElementById(field);
                    if (元素) {
                        element.value = editableFields[field];
                    }
                }
                
                localStorage.removeItem('resumeData');
                showSaveStatus('已重置为默认值', true);
            }
            
            // 显示保存状态
            function showSaveStatus(message, isSuccess) {
                saveStatus.textContent = message;
                saveStatus.style.color = isSuccess ? 'var(--secondary-color)' : 'var(--danger-color)';
                
                // 3秒后淡出
                setTimeout(() => {
                    saveStatus.style.opacity = '0';
                    setTimeout(() => {
                        saveStatus.textContent = '';
                        saveStatus.style.opacity = '1';
                    }, 500);
                }, 3000);
            }
            
            // 保存按钮点击事件
            saveBtn.addEventListener('click', saveFormData);
            
            // 重置按钮点击事件
            resetBtn.addEventListener('click', resetToDefault);
            
            // 页面加载时恢复数据
            加载表单数据();
        });
    </script>
</主体>
</html>

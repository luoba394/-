<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>嘉铭大王一键去水印</title>
    <style>
        :root {
            --primary-color: #4e6ef2;
            --primary-hover: #3b5bdb;
            --bg-color: #1a1b1e;
            --panel-bg: #25262b;
            --text-color: #ffffff;
            --text-secondary: #909296;
            --border-color: #373a40;
            --accent-red: #fa5252;
        }

        body {
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
        }

        header {
            width: 100%;
            background-color: var(--panel-bg);
            border-bottom: 1px solid var(--border-color);
            padding: 1.2rem 0;
            text-align: center;
            box-shadow: 0 4px 12px rgba(0,0,0,0.3);
            z-index: 10;
        }

        h1 {
            margin: 0;
            font-size: 1.8rem;
            background: linear-gradient(90deg, #4e6ef2, #2bc0e4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            letter-spacing: 2px;
            font-weight: 800;
        }

        .container {
            flex: 1;
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 100%;
            max-width: 1200px;
            padding: 30px 20px;
            box-sizing: border-box;
        }

        /* 工具栏 */
        .toolbar {
            display: flex;
            gap: 15px;
            margin-bottom: 25px;
            flex-wrap: wrap;
            justify-content: center;
            background: var(--panel-bg);
            padding: 15px 25px;
            border-radius: 12px;
            box-shadow: 0 8px 20px rgba(0,0,0,0.2);
            border: 1px solid var(--border-color);
        }

        .btn {
            background-color: #2c2e33;
            border: 1px solid var(--border-color);
            color: var(--text-color);
            padding: 10px 24px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 15px;
            font-weight: 500;
            transition: all 0.2s ease;
            display: flex;
            align-items: center;
            gap: 8px;
            user-select: none;
        }

        .btn:hover:not(:disabled) {
            background-color: #373a40;
            transform: translateY(-1px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }

        .btn:active:not(:disabled) {
            transform: translateY(0);
        }

        .btn.primary {
            background-color: var(--primary-color);
            border-color: var(--primary-color);
            color: white;
            font-weight: 600;
        }

        .btn.primary:hover:not(:disabled) {
            background-color: var(--primary-hover);
            border-color: var(--primary-hover);
            box-shadow: 0 4px 12px rgba(78, 110, 242, 0.4);
        }

        .btn:disabled {
            opacity: 0.4;
            cursor: not-allowed;
            transform: none !important;
        }

        /* 工作区 */
        .workspace {
            position: relative;
            background-color: #101113;
            border: 2px dashed var(--border-color);
            border-radius: 12px;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            min-width: 600px;
            min-height: 400px;
            max-width: 100%;
            max-height: 80vh;
            box-shadow: inset 0 0 40px rgba(0,0,0,0.3);
            transition: border-color 0.3s;
        }

        .workspace.drag-over {
            border-color: var(--primary-color);
            background-color: rgba(78, 110, 242, 0.05);
        }

        .workspace.has-image {
            border-style: solid;
            box-shadow: 0 20px 50px rgba(0,0,0,0.5);
            background-color: #141517; /* 深色背景衬托图片 */
        }

        /* Canvas 容器 */
        #canvas-container {
            position: relative;
            display: none; /* 有图片时显示 */
            box-shadow: 0 0 0 1px #333;
        }

        canvas {
            display: block;
            max-width: 100%;
            max-height: 70vh; /* 限制高度，防止超出屏幕 */
            cursor: crosshair;
            /* 确保像素清晰 */
            image-rendering: auto; 
        }

        /* 选框样式 */
        .selection-box {
            position: absolute;
            border: 2px solid var(--accent-red);
            background-color: rgba(250, 82, 82, 0.15);
            pointer-events: none;
            display: none;
            box-shadow: 0 0 0 1px rgba(255, 255, 255, 0.2), 0 0 10px rgba(0,0,0,0.3);
            z-index: 5;
        }

        /* 提示信息 */
        .placeholder-text {
            display: flex;
            flex-direction: column;
            align-items: center;
            color: var(--text-secondary);
            pointer-events: none;
            transition: opacity 0.3s;
        }

        .placeholder-icon {
            font-size: 48px;
            margin-bottom: 15px;
            opacity: 0.5;
        }

        .tips {
            margin-top: 20px;
            padding: 12px 20px;
            background: rgba(255,255,255,0.05);
            border-radius: 8px;
            font-size: 14px;
            color: #adb5bd;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .tips strong {
            color: var(--primary-color);
        }

        /* Loading 遮罩 */
        .loading-overlay {
            position: absolute;
            top: 0; left: 0; right: 0; bottom: 0;
            background: rgba(0,0,0,0.7);
            display: none;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            z-index: 100;
            color: white;
            backdrop-filter: blur(4px);
        }
        
        .spinner {
            width: 40px;
            height: 40px;
            border: 4px solid rgba(255,255,255,0.1);
            border-left-color: var(--primary-color);
            border-radius: 50%;
            animation: spin 1s linear infinite;
            margin-bottom: 15px;
        }
        
        @keyframes spin {
            to { transform: rotate(360deg); }
        }

        input[type="file"] {
            display: none;
        }
    </style>
</head>
<body>

    <header>
        <h1>嘉铭大王一键去水印</h1>
    </header>

    <div class="container">
        <div class="toolbar">
            <button class="btn" onclick="document.getElementById('fileInput').click()">
                <span>📁</span> 选择图片
            </button>
            <button class="btn primary" id="removeBtn" disabled onclick="processor.removeWatermark()">
                <span>✨</span> 立即去除
            </button>
            <button class="btn" id="downloadBtn" disabled onclick="processor.download()">
                <span>💾</span> 保存图片
            </button>
            <button class="btn" id="resetBtn" disabled onclick="processor.reset()">
                <span>↺</span> 还原原图
            </button>
        </div>

        <input type="file" id="fileInput" accept="image/*">

        <div class="workspace" id="workspace">
            <div class="placeholder-text" id="placeholder">
                <div class="placeholder-icon">🖼️</div>
                <h3>点击上方“选择图片”或拖拽图片到此处</h3>
                <p>支持高清原图 JPG / PNG</p>
            </div>
            
            <div id="canvas-container">
                <canvas id="imgCanvas"></canvas>
                <div id="selectionBox" class="selection-box"></div>
                
                <!-- 处理中的遮罩 -->
                <div class="loading-overlay" id="loadingOverlay">
                    <div class="spinner"></div>
                    <div id="loadingText">智能算法处理中...</div>
                </div>
            </div>
        </div>

        <div class="tips">
            <span>💡 使用技巧：</span>
            <span>框选水印区域（尽量贴合水印边缘），系统会自动扩展处理范围。复杂背景可能需要处理 2-3 次。</span>
        </div>
    </div>

    <script>
        /**
         * 图像处理器核心逻辑
         */
        class ImageProcessor {
            constructor() {
                this.canvas = document.getElementById('imgCanvas');
                this.ctx = this.canvas.getContext('2d', { willReadFrequently: true });
                this.container = document.getElementById('canvas-container');
                this.workspace = document.getElementById('workspace');
                this.placeholder = document.getElementById('placeholder');
                this.selectionBox = document.getElementById('selectionBox');
                this.loadingOverlay = document.getElementById('loadingOverlay');
                this.loadingText = document.getElementById('loadingText');
                
                // 状态
                this.originalImage = null;
                this.isDragging = false;
                this.startX = 0;
                this.startY = 0;
                this.selection = null; // {x, y, w, h}
                
                // UI 引用
                this.btnRemove = document.getElementById('removeBtn');
                this.btnDownload = document.getElementById('downloadBtn');
                this.btnReset = document.getElementById('resetBtn');

                this.initEvents();
            }

            initEvents() {
                // 文件上传
                const fileInput = document.getElementById('fileInput');
                fileInput.addEventListener('change', (e) => this.handleFile(e.target.files[0]));

                // 拖拽上传
                this.workspace.addEventListener('dragover', (e) => {
                    e.preventDefault();
                    this.workspace.classList.add('drag-over');
                });
                this.workspace.addEventListener('dragleave', (e) => {
                    e.preventDefault();
                    this.workspace.classList.remove('drag-over');
                });
                this.workspace.addEventListener('drop', (e) => {
                    e.preventDefault();
                    this.workspace.classList.remove('drag-over');
                    if (e.dataTransfer.files && e.dataTransfer.files[0]) {
                        this.handleFile(e.dataTransfer.files[0]);
                    }
                });

                // 鼠标/触摸操作选区
                this.canvas.addEventListener('mousedown', this.onMouseDown.bind(this));
                window.addEventListener('mousemove', this.onMouseMove.bind(this));
                window.addEventListener('mouseup', this.onMouseUp.bind(this));
                
                this.canvas.addEventListener('touchstart', (e) => {
                    const touch = e.touches[0];
                    this.onMouseDown({ clientX: touch.clientX, clientY: touch.clientY, target: e.target });
                });
                window.addEventListener('touchmove', (e) => {
                    if(this.isDragging) e.preventDefault();
                    const touch = e.touches[0];
                    this.onMouseMove({ clientX: touch.clientX, clientY: touch.clientY });
                }, { passive: false });
                window.addEventListener('touchend', this.onMouseUp.bind(this));
            }

            handleFile(file) {
                if (file && file.type.startsWith('image/')) {
                    const reader = new FileReader();
                    reader.onload = (evt) => {
                        const img = new Image();
                        img.onload = () => this.loadImage(img);
                        img.src = evt.target.result;
                    };
                    reader.readAsDataURL(file);
                }
            }

            loadImage(img) {
                this.originalImage = img;
                this.placeholder.style.display = 'none';
                this.container.style.display = 'block';
                this.workspace.classList.add('has-image');

                // 适配 Canvas 尺寸
                this.canvas.width = img.width;
                this.canvas.height = img.height;
                this.ctx.drawImage(img, 0, 0);

                // 启用按钮
                this.btnReset.disabled = false;
                this.btnDownload.disabled = false;
                this.clearSelection();
            }

            getCanvasCoordinates(clientX, clientY) {
                const rect = this.canvas.getBoundingClientRect();
                const scaleX = this.canvas.width / rect.width;
                const scaleY = this.canvas.height / rect.height;
                return {
                    x: (clientX - rect.left) * scaleX,
                    y: (clientY - rect.top) * scaleY,
                    domX: clientX - rect.left, // DOM 坐标用于显示选框
                    domY: clientY - rect.top
                };
            }

            onMouseDown(e) {
                if (!this.originalImage) return;
                if(this.loadingOverlay.style.display === 'flex') return;

                this.isDragging = true;
                const coords = this.getCanvasCoordinates(e.clientX, e.clientY);
                
                this.startX = coords.x;
                this.startY = coords.y;
                
                this.startDomX = coords.domX;
                this.startDomY = coords.domY;
                
                this.selectionBox.style.display = 'block';
                this.updateSelectionBoxUI(coords.domX, coords.domY, 0, 0);
                
                this.selection = { x: this.startX, y: this.startY, w: 0, h: 0 };
                this.btnRemove.disabled = true;
            }

            onMouseMove(e) {
                if (!this.isDragging) return;
                
                const coords = this.getCanvasCoordinates(e.clientX, e.clientY);
                
                let w = coords.x - this.startX;
                let h = coords.y - this.startY;

                this.selection = {
                    x: w < 0 ? coords.x : this.startX,
                    y: h < 0 ? coords.y : this.startY,
                    w: Math.abs(w),
                    h: Math.abs(h)
                };

                const uiW = coords.domX - this.startDomX;
                const uiH = coords.domY - this.startDomY;
                const uiLeft = uiW < 0 ? coords.domX : this.startDomX;
                const uiTop = uiH < 0 ? coords.domY : this.startDomY;

                this.updateSelectionBoxUI(uiLeft, uiTop, Math.abs(uiW), Math.abs(uiH));
            }

            onMouseUp(e) {
                if (!this.isDragging) return;
                this.isDragging = false;
                
                if (this.selection && (this.selection.w < 2 || this.selection.h < 2)) {
                    this.clearSelection();
                } else {
                    this.btnRemove.disabled = false;
                }
            }

            updateSelectionBoxUI(left, top, width, height) {
                this.selectionBox.style.left = left + 'px';
                this.selectionBox.style.top = top + 'px';
                this.selectionBox.style.width = width + 'px';
                this.selectionBox.style.height = height + 'px';
            }

            clearSelection() {
                this.selection = null;
                this.selectionBox.style.display = 'none';
                this.btnRemove.disabled = true;
            }

            reset() {
                if (this.originalImage) {
                    this.ctx.drawImage(this.originalImage, 0, 0);
                    this.clearSelection();
                }
            }

            download() {
                const link = document.createElement('a');
                link.download = '嘉铭大王-去水印完成.png';
                link.href = this.canvas.toDataURL('image/png', 1.0);
                link.click();
            }
            
            showLoading(show, text = "智能算法处理中...") {
                this.loadingText.innerText = text;
                this.loadingOverlay.style.display = show ? 'flex' : 'none';
            }

            /**
             * 核心算法更新：基于纹理合成的修补 (Texture Synthesis / Patch-Based Inpainting)
             * 解决矩形残留问题：
             * 1. 自动扩展选区，消除边缘伪影。
             * 2. 寻找最佳匹配块，复制纹理而不是平均颜色。
             * 3. 边缘羽化融合。
             */
            async removeWatermark() {
                if (!this.selection) return;

                this.showLoading(true);
                await new Promise(resolve => setTimeout(resolve, 50));

                // 1. 自动扩展选区 (Auto Padding) - 消除“相框”效应
                // 增加 8-12px 的 buffer，确保覆盖压缩噪点
                const padding = 10;
                let { x, y, w, h } = this.normalizeSelection();
                
                // 保存原始选择区域用于最后融合
                const rawX = x, rawY = y, rawW = w, rawH = h;

                x = Math.max(0, x - padding);
                y = Math.max(0, y - padding);
                w = Math.min(this.canvas.width - x, w + padding * 2);
                h = Math.min(this.canvas.height - y, h + padding * 2);

                // 提取操作区域
                const imgData = this.ctx.getImageData(x, y, w, h);
                const pixels = imgData.data;
                
                // 创建掩码：1表示待修复区域（原选区+部分padding内部），0表示可信任区域
                const mask = new Uint8Array(w * h);
                const visited = new Uint8Array(w * h); // 记录是否已处理
                
                // 计算相对坐标
                const relRawX = rawX - x;
                const relRawY = rawY - y;
                
                // 初始化 Mask
                // 我们只标记“原始选区”稍微扩大一点点的区域为需要修复，保留外圈作为纹理源
                const innerPad = 2; // 轻微向外扩展修复区，但不填满整个imgData
                for (let j = 0; j < h; j++) {
                    for (let i = 0; i < w; i++) {
                        // 检查像素是否在 原始选区 范围内
                        if (i >= relRawX - innerPad && i < relRawX + rawW + innerPad &&
                            j >= relRawY - innerPad && j < relRawY + rawH + innerPad) {
                            mask[j * w + i] = 1; // Hole
                        } else {
                            mask[j * w + i] = 0; // Source
                        }
                    }
                }

                // 2. 纹理合成修复循环 (Onion Peel Order)
                // 从外向内修复
                let hasWork = true;
                const patchSize = 5; // 补丁大小 (奇数)
                const radius = Math.floor(patchSize / 2);
                const searchRadius = 40; // 搜索最佳匹配纹理的范围

                // 限制最大迭代防止卡死
                let loopLimit = w * h; 

                while (hasWork && loopLimit-- > 0) {
                    hasWork = false;
                    const currentBoundary = [];

                    // 寻找当前的边界像素 (Mask为1，但有邻居Mask为0)
                    for (let j = 0; j < h; j++) {
                        for (let i = 0; i < w; i++) {
                            const idx = j * w + i;
                            if (mask[idx] === 1) {
                                // 检查4邻域
                                let isBoundary = false;
                                if (i>0 && mask[idx-1]===0) isBoundary = true;
                                else if (i<w-1 && mask[idx+1]===0) isBoundary = true;
                                else if (j>0 && mask[idx-w]===0) isBoundary = true;
                                else if (j<h-1 && mask[idx+w]===0) isBoundary = true;

                                if (isBoundary) {
                                    currentBoundary.push({i, j, idx});
                                }
                            }
                        }
                    }

                    if (currentBoundary.length === 0) break; // 完成

                    // 对每个边界像素进行修复
                    // 随机打乱顺序，避免纹理重复感
                    this.shuffleArray(currentBoundary);

                    for (const p of currentBoundary) {
                        // 寻找最佳匹配块
                        const bestMatch = this.findBestPatch(pixels, mask, w, h, p.i, p.j, patchSize, searchRadius);
                        
                        // 填补像素
                        const targetPos = p.idx * 4;
                        const sourcePos = (bestMatch.j * w + bestMatch.i) * 4;
                        
                        pixels[targetPos] = pixels[sourcePos];
                        pixels[targetPos+1] = pixels[sourcePos+1];
                        pixels[targetPos+2] = pixels[sourcePos+2];
                        // pixels[targetPos+3] = 255; // Alpha保持
                        
                        mask[p.idx] = 0; // 标记为已修复（成为下一次的源）
                        hasWork = true;
                    }
                    
                    // 每处理几层暂停一下，防止浏览器无响应（可选，这里为了速度直接跑）
                }

                // 3. 边缘融合 (Seam Blending)
                // 对修复区域的边缘进行高斯模糊，消除像素阶梯
                this.blendEdges(pixels, w, h, relRawX, relRawY, rawW, rawH);

                // 写回画布
                this.ctx.putImageData(imgData, x, y);
                
                this.clearSelection();
                this.showLoading(false);
            }

            // 简单的数组乱序
            shuffleArray(array) {
                for (let i = array.length - 1; i > 0; i--) {
                    const j = Math.floor(Math.random() * (i + 1));
                    [array[i], array[j]] = [array[j], array[i]];
                }
            }

            // 在已知区域寻找与 (tx, ty) 周围环境最像的块
            findBestPatch(pixels, mask, w, h, tx, ty, patchSize, searchRadius) {
                let bestDiff = Infinity;
                let bestX = tx;
                let bestY = ty;
                
                const r = Math.floor(patchSize/2);
                
                // 定义搜索区域限制
                const startY = Math.max(r, ty - searchRadius);
                const endY = Math.min(h - r, ty + searchRadius);
                const startX = Math.max(r, tx - searchRadius);
                const endX = Math.min(w - r, tx + searchRadius);
                
                // 随机采样 50 个点，而不是全遍历（性能优化）
                const samples = 80;
                
                for(let k=0; k<samples; k++) {
                    const sx = Math.floor(Math.random() * (endX - startX)) + startX;
                    const sy = Math.floor(Math.random() * (endY - startY)) + startY;
                    
                    // 候选块中心必须是已知区域 (mask=0)
                    if (mask[sy * w + sx] === 1) continue;
                    
                    // 计算差异 (SSD)
                    let diff = 0;
                    let validCount = 0;
                    
                    for(let dy = -r; dy <= r; dy++) {
                        for(let dx = -r; dx <= r; dx++) {
                            // 目标块坐标
                            const tIdx = (ty + dy) * w + (tx + dx);
                            // 只有当目标块的这个邻居是已知像素时，才进行比较
                            if (mask[tIdx] === 0) {
                                const sIdx = (sy + dy) * w + (sx + dx);
                                
                                const pT = tIdx * 4;
                                const pS = sIdx * 4;
                                
                                const dr = pixels[pT] - pixels[pS];
                                const dg = pixels[pT+1] - pixels[pS+1];
                                const db = pixels[pT+2] - pixels[pS+2];
                                
                                diff += dr*dr + dg*dg + db*db;
                                validCount++;
                            }
                        }
                    }
                    
                    if (validCount > 0) {
                        const avgDiff = diff / validCount;
                        if (avgDiff < bestDiff) {
                            bestDiff = avgDiff;
                            bestX = sx;
                            bestY = sy;
                        }
                    }
                }
                
                return { i: bestX, j: bestY };
            }
            
            // 边缘融合：只模糊原始选区边框附近的像素
            blendEdges(pixels, w, h, rx, ry, rw, rh) {
                const copy = new Uint8ClampedArray(pixels);
                // 定义模糊宽度
                const blurSize = 2; 
                
                // 遍历选区边缘
                for (let y = Math.max(0, ry - blurSize); y < Math.min(h, ry + rh + blurSize); y++) {
                    for (let x = Math.max(0, rx - blurSize); x < Math.min(w, rx + rw + blurSize); x++) {
                        
                        // 仅处理边缘地带
                        const onEdge = (x < rx + blurSize || x > rx + rw - blurSize || 
                                        y < ry + blurSize || y > ry + rh - blurSize);
                                        
                        if (onEdge) {
                            let r=0, g=0, b=0, c=0;
                            for(let j=-1; j<=1; j++){
                                for(let i=-1; i<=1; i++){
                                    const nx = x+i; 
                                    const ny = y+j;
                                    if(nx>=0 && nx<w && ny>=0 && ny<h){
                                        const idx = (ny*w+nx)*4;
                                        r+=copy[idx]; g+=copy[idx+1]; b+=copy[idx+2];
                                        c++;
                                    }
                                }
                            }
                            const idx = (y*w+x)*4;
                            pixels[idx] = r/c;
                            pixels[idx+1] = g/c;
                            pixels[idx+2] = b/c;
                        }
                    }
                }
            }

            normalizeSelection() {
                let { x, y, w, h } = this.selection;
                x = Math.floor(x);
                y = Math.floor(y);
                w = Math.ceil(w);
                h = Math.ceil(h);
                x = Math.max(0, x);
                y = Math.max(0, y);
                w = Math.min(this.canvas.width - x, w);
                h = Math.min(this.canvas.height - y, h);
                return { x, y, w, h };
            }
        }

        const processor = new ImageProcessor();
    </script>
</body>

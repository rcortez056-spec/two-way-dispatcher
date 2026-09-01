<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Two-Way Dispatcher Live Demo</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body {
            font-family: 'JetBrains Mono', monospace;
            background: linear-gradient(135deg, #0f0f0f 0%, #1a1a1a 100%);
            color: #e0e0e0;
            padding: 20px;
            min-height: 100vh;
        }
        
        .container { max-width: 1600px; margin: 0 auto; }
        
        header {
            text-align: center;
            margin-bottom: 30px;
        }
        
        h1 { color: #C9A96E; font-size: 36px; margin-bottom: 8px; }
        .subtitle { color: #888; font-size: 11px; text-transform: uppercase; letter-spacing: 1px; }
        .author { color: #C9A96E; font-size: 10px; margin-top: 10px; }
        
        .grid-3 {
            display: grid;
            grid-template-columns: 1fr 1.5fr 1fr;
            gap: 20px;
            margin-bottom: 20px;
        }
        
        .section {
            background: rgba(20, 20, 20, 0.8);
            border: 1px solid #333;
            border-radius: 8px;
            padding: 20px;
            height: fit-content;
        }
        
        .section-title {
            color: #C9A96E;
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 1px solid #C9A96E;
        }
        
        input, textarea {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            background: rgba(0, 0, 0, 0.5);
            border: 1px solid #444;
            border-radius: 4px;
            color: #e0e0e0;
            font-family: 'JetBrains Mono', monospace;
            font-size: 10px;
        }
        
        input:focus, textarea:focus {
            outline: none;
            border-color: #C9A96E;
            background: rgba(201, 169, 110, 0.1);
        }
        
        button {
            background: linear-gradient(135deg, #C9A96E 0%, #a0844b 100%);
            color: #0f0f0f;
            border: none;
            padding: 12px 20px;
            border-radius: 4px;
            cursor: pointer;
            font-weight: bold;
            font-size: 10px;
            text-transform: uppercase;
            font-family: 'JetBrains Mono', monospace;
            transition: all 0.3s;
            width: 100%;
            margin-bottom: 10px;
        }
        
        button:hover:not(:disabled) { transform: translateY(-2px); box-shadow: 0 5px 15px rgba(201, 169, 110, 0.3); }
        button:disabled { opacity: 0.5; cursor: not-allowed; }
        
        .flow-box {
            background: rgba(201, 169, 110, 0.1);
            border: 2px solid #C9A96E;
            border-radius: 6px;
            padding: 15px;
            margin-bottom: 15px;
            min-height: 120px;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        
        .flow-status {
            color: #C9A96E;
            font-size: 10px;
            font-weight: bold;
            margin-bottom: 10px;
        }
        
        .flow-message {
            color: #e0e0e0;
            font-size: 9px;
            line-height: 1.4;
            background: rgba(0, 0, 0, 0.3);
            padding: 10px;
            border-radius: 4px;
            margin-bottom: 10px;
        }
        
        .response-section {
            display: none;
        }
        
        .response-section.active {
            display: block;
        }
        
        .arrow {
            text-align: center;
            font-size: 24px;
            color: #C9A96E;
            margin: 10px 0;
            animation: bounce 1s infinite;
        }
        
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-5px); }
        }
        
        .audit-log {
            background: rgba(0, 0, 0, 0.5);
            border: 1px solid #333;
            border-radius: 4px;
            padding: 12px;
            font-size: 8px;
            max-height: 400px;
            overflow-y: auto;
            word-wrap: break-word;
            word-break: break-word;
        }
        
        .audit-entry {
            padding: 8px;
            margin-bottom: 6px;
            border-left: 3px solid #C9A96E;
            background: rgba(201, 169, 110, 0.1);
            border-radius: 2px;
            word-wrap: break-word;
            word-break: break-word;
            overflow-wrap: break-word;
        }
        
        .audit-time { color: #888; font-size: 7px; }
        .audit-dispatch { color: #2196F3; }
        .audit-response { color: #4CAF50; }
        .audit-success { color: #FFC107; }
        
        .metrics {
            display: grid;
            grid-template-columns: 1fr;
            gap: 10px;
        }
        
        .metric {
            background: rgba(0, 0, 0, 0.5);
            border: 1px solid #333;
            border-radius: 4px;
            padding: 12px;
        }
        
        .metric-label { color: #888; font-size: 7px; text-transform: uppercase; }
        .metric-value { color: #C9A96E; font-size: 20px; font-weight: bold; margin-top: 6px; }
        
        .badge {
            display: inline-block;
            background: rgba(201, 169, 110, 0.2);
            color: #C9A96E;
            padding: 4px 8px;
            border-radius: 2px;
            font-size: 8px;
            margin-right: 6px;
        }
        
        .active-dispatch-box {
            background: rgba(76, 175, 80, 0.1);
            border: 2px solid #4CAF50;
            border-radius: 6px;
            padding: 12px;
            margin-top: 10px;
        }
        
        label { color: #888; font-size: 8px; text-transform: uppercase; display: block; margin-bottom: 4px; }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>🔄 TWO-WAY DISPATCHER</h1>
            <div class="subtitle">Bidirectional Request-Response Pattern</div>
            <div class="author">By Ramon Cortez, AI Architect</div>
        </header>
        
        <div class="grid-3">
            <!-- LEFT: DISPATCH CONTROL -->
            <div class="section">
                <div class="section-title">📤 DISPATCH OUTBOUND</div>
                
                <label>Dispatch ID</label>
                <input type="text" id="dispatchId" placeholder="DISPATCH-001" value="DISPATCH-001">
                
                <label>Toy Name</label>
                <input type="text" id="toyName" placeholder="Lego Starship" value="Lego Starship">
                
                <label>Room/Location</label>
                <input type="text" id="room" placeholder="Playroom Shelf" value="Playroom Shelf">
                
                <label>Helper Name</label>
                <input type="text" id="helper" placeholder="Leo" value="Leo">
                
                <button onclick="dispatchToy()">📤 SEND OUTBOUND</button>
                
                <div style="margin-top: 20px; font-size: 8px; color: #888;">
                    <div style="margin-bottom: 10px;">
                        💡 Quick Start:
                        <br>1. Fill form above
                        <br>2. Click SEND OUTBOUND
                        <br>3. Watch dispatch appear
                        <br>4. Reply in middle panel
                    </div>
                </div>
            </div>
            
            <!-- MIDDLE: BIDIRECTIONAL FLOW -->
            <div class="section">
                <div class="section-title">🔄 BIDIRECTIONAL FLOW</div>
                
                <!-- OUTBOUND -->
                <div id="outboundBox" style="display: none;">
                    <div class="flow-box">
                        <div class="flow-status">📤 OUTBOUND REQUEST</div>
                        <div class="flow-message" id="outboundMessage"></div>
                        <div style="font-size: 8px; color: #C9A96E;">✓ Message sent, waiting for response...</div>
                    </div>
                    
                    <div class="arrow">↓</div>
                    
                    <!-- INBOUND RESPONSE -->
                    <div class="flow-box active-dispatch-box" id="inboundBox">
                        <div class="flow-status">📥 WAITING FOR RESPONSE</div>
                        
                        <label>Did you complete the task?</label>
                        <select id="responseSelect" style="margin-bottom: 10px;">
                            <option value="">-- Select Response --</option>
                            <option value="YES">YES (Task complete)</option>
                            <option value="NO">NO (Needs attention)</option>
                        </select>
                        
                        <label>Extra Notes (optional)</label>
                        <textarea id="extraNotes" placeholder="Any additional info..." style="height: 50px; margin-bottom: 10px;"></textarea>
                        
                        <button onclick="sendResponse()">📥 SEND RESPONSE</button>
                    </div>
                    
                    <div class="arrow" id="responseArrow" style="display: none;">↓</div>
                    
                    <!-- RESOLUTION -->
                    <div class="flow-box" id="resolutionBox" style="display: none;">
                        <div class="flow-status">🔄 RESOLUTION</div>
                        <div class="flow-message" id="resolutionMessage"></div>
                    </div>
                </div>
                
                <!-- IDLE STATE -->
                <div id="idleBox" style="text-align: center; padding: 40px; color: #888;">
                    <div style="font-size: 24px; margin-bottom: 10px;">⏳</div>
                    <div style="font-size: 9px;">Ready to dispatch</div>
                    <div style="font-size: 8px; color: #666; margin-top: 10px;">Fill the form on the left and click SEND OUTBOUND</div>
                </div>
            </div>
            
            <!-- RIGHT: METRICS & AUDIT TRAIL -->
            <div class="section">
                <div class="section-title">📊 METRICS</div>
                
                <div class="metrics">
                    <div class="metric">
                        <div class="metric-label">Dispatched</div>
                        <div class="metric-value" id="dispatchedCount">0</div>
                    </div>
                    
                    <div class="metric">
                        <div class="metric-label">Responded</div>
                        <div class="metric-value" id="respondedCount">0</div>
                    </div>
                    
                    <div class="metric">
                        <div class="metric-label">Success Rate</div>
                        <div class="metric-value" id="successRate">0%</div>
                    </div>
                </div>
                
                <div class="section-title" style="margin-top: 20px;">📖 AUDIT TRAIL</div>
                <div class="audit-log" id="auditLog"></div>
            </div>
        </div>
    </div>

    <script>
        class TwoWayDispatcher {
            constructor() {
                this.activeDispatches = {};
                this.completedHistory = [];
                this.metrics = {
                    dispatched: 0,
                    responded: 0,
                    successful: 0
                };
            }
            
            dispatchToy(dispatchId, toyName, room, helper) {
                const message = {
                    dispatch_id: dispatchId,
                    status: "WAITING_FOR_HELPER",
                    toy: toyName,
                    room: room,
                    assigned_to: helper,
                    timestamp: new Date().toLocaleTimeString()
                };
                
                this.activeDispatches[dispatchId] = message;
                this.metrics.dispatched++;
                
                addAuditEntry(`📤 [OUTBOUND] ${helper} assigned: "${toyName}" → "${room}"`, 'dispatch');
                
                return message;
            }
            
            receiveResponse(dispatchId, kidReply, extraNotes = "") {
                if (!this.activeDispatches[dispatchId]) {
                    return null;
                }
                
                const original = this.activeDispatches[dispatchId];
                delete this.activeDispatches[dispatchId];
                
                const replyClean = kidReply.trim().toUpperCase();
                let resultStatus, finalMessage;
                
                if (replyClean === "YES") {
                    resultStatus = "✅ TASK COMPLETED SUCCESSFULLY";
                    finalMessage = `🌟 Awesome! ${original.assigned_to}, the ${original.toy} is safely in the ${original.room}.`;
                    this.metrics.successful++;
                } else if (replyClean === "NO") {
                    resultStatus = "⚠️ NEEDS ATTENTION";
                    finalMessage = `🛠️ Got it! The ${original.toy} still needs to go to the ${original.room}.`;
                    if (extraNotes) finalMessage += ` (${extraNotes})`;
                } else {
                    return null;
                }
                
                const auditEntry = {
                    dispatch_id: dispatchId,
                    toy: original.toy,
                    helper: original.assigned_to,
                    kid_reply: kidReply,
                    final_status: resultStatus,
                    timestamp: new Date().toLocaleTimeString()
                };
                
                this.completedHistory.push(auditEntry);
                this.metrics.responded++;
                
                addAuditEntry(`📥 [INBOUND] Response: "${kidReply}"`, 'response');
                addAuditEntry(`🔄 [RESOLUTION] ${resultStatus}`, 'success');
                
                return {
                    status: resultStatus,
                    message: finalMessage,
                    data: auditEntry
                };
            }
        }
        
        const dispatcher = new TwoWayDispatcher();
        
        function addAuditEntry(message, type = 'info') {
            const log = document.getElementById('auditLog');
            const entry = document.createElement('div');
            entry.className = `audit-entry audit-${type}`;
            const timestamp = new Date().toLocaleTimeString('en-US', { hour12: false });
            entry.innerHTML = `<div class="audit-time">[${timestamp}]</div><div>${message}</div>`;
            log.appendChild(entry);
            log.scrollTop = log.scrollHeight;
        }
        
        function dispatchToy() {
            const dispatchId = document.getElementById('dispatchId').value.trim();
            const toyName = document.getElementById('toyName').value.trim();
            const room = document.getElementById('room').value.trim();
            const helper = document.getElementById('helper').value.trim();
            
            if (!dispatchId || !toyName || !room || !helper) {
                addAuditEntry('❌ All fields required', 'error');
                return;
            }
            
            const message = dispatcher.dispatchToy(dispatchId, toyName, room, helper);
            
            // Show outbound flow
            document.getElementById('idleBox').style.display = 'none';
            document.getElementById('outboundBox').style.display = 'block';
            document.getElementById('outboundMessage').textContent = 
                `"🤖 ${helper}, did you put the ${toyName} in the ${room}? (Reply YES/NO)"`;
            
            // Show response input
            document.getElementById('inboundBox').style.display = 'block';
            document.getElementById('resolutionBox').style.display = 'none';
            document.getElementById('responseArrow').style.display = 'none';
            
            updateMetrics();
        }
        
        function sendResponse() {
            const reply = document.getElementById('responseSelect').value.trim();
            const extra = document.getElementById('extraNotes').value.trim();
            
            if (!reply) {
                addAuditEntry('❌ Please select a response', 'error');
                return;
            }
            
            const dispatchId = document.getElementById('dispatchId').value.trim();
            const result = dispatcher.receiveResponse(dispatchId, reply, extra);
            
            if (!result) {
                addAuditEntry('❌ Dispatch not found', 'error');
                return;
            }
            
            // Show resolution
            document.getElementById('responseArrow').style.display = 'block';
            document.getElementById('resolutionBox').style.display = 'block';
            document.getElementById('resolutionMessage').textContent = result.message;
            
            // Hide response input
            document.getElementById('inboundBox').style.display = 'none';
            
            // Reset form
            setTimeout(() => {
                document.getElementById('dispatchId').value = `DISPATCH-${String(dispatcher.metrics.dispatched + 1).padStart(3, '0')}`;
                document.getElementById('toyName').value = '';
                document.getElementById('room').value = '';
                document.getElementById('helper').value = '';
                document.getElementById('responseSelect').value = '';
                document.getElementById('extraNotes').value = '';
            }, 1000);
            
            updateMetrics();
        }
        
        function updateMetrics() {
            document.getElementById('dispatchedCount').textContent = dispatcher.metrics.dispatched;
            document.getElementById('respondedCount').textContent = dispatcher.metrics.responded;
            
            const rate = dispatcher.metrics.responded > 0 
                ? Math.round((dispatcher.metrics.successful / dispatcher.metrics.responded) * 100)
                : 0;
            document.getElementById('successRate').textContent = rate + '%';
        }
    </script>
</body>
</html>

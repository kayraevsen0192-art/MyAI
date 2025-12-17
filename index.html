<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MyAI Chat</title>
    <style>
        body { font-family: 'Segoe UI', sans-serif; display: flex; align-items: center; justify-content: center; min-height: 100vh; margin: 0; background: #0f172a; color: white; }
        #chat-container { width: 95%; max-width: 500px; background: #1e293b; padding: 20px; border-radius: 15px; box-shadow: 0 10px 30px rgba(0,0,0,0.5); }
        h2 { text-align: center; color: #38bdf8; margin-bottom: 20px; }
        #chat-box { height: 300px; overflow-y: auto; background: #0f172a; border-radius: 10px; padding: 15px; margin-bottom: 15px; border: 1px solid #334155; display: flex; flex-direction: column; gap: 10px; }
        .msg { padding: 10px; border-radius: 8px; max-width: 80%; line-height: 1.4; font-size: 14px; }
        .user-msg { background: #38bdf8; color: #0f172a; align-self: flex-end; }
        .ai-msg { background: #334155; color: white; align-self: flex-start; border-left: 3px solid #38bdf8; }
        .input-area { display: flex; gap: 10px; }
        input { flex: 1; padding: 12px; border-radius: 8px; border: 1px solid #475569; background: #1e293b; color: white; outline: none; }
        button { padding: 12px 20px; background: #38bdf8; color: #0f172a; border: none; border-radius: 8px; font-weight: bold; cursor: pointer; }
    </style>
</head>
<body>
    <div id="chat-container">
        <h2>MyAI Chat</h2>
        <div id="chat-box">
            <div class="msg ai-msg">Hello! I'm MyAI. Let's chat in English or Japanese!</div>
        </div>
        <div class="input-area">
            <input type="text" id="userInput" placeholder="Type a message...">
            <button onclick="askAI()">Send</button>
        </div>
    </div>

    <script>
        async function askAI() {
            const inputField = document.getElementById('userInput');
            const chatBox = document.getElementById('chat-box');
            const prompt = inputField.value;
            if(!prompt) return;

            // Kullanıcı mesajını ekle
            chatBox.innerHTML += `<div class="msg user-msg">${prompt}</div>`;
            inputField.value = "";
            chatBox.scrollTop = chatBox.scrollHeight;

            const loadingId = "loading-" + Date.now();
            chatBox.innerHTML += `<div class="msg ai-msg" id="${loadingId}">Thinking...</div>`;

            try {
                const response = await fetch("https://api-inference.huggingface.co/models/facebook/blenderbot-400M-distill", {
                    method: "POST",
                    headers: { "Content-Type": "application/json" },
                    body: JSON.stringify({ inputs: prompt })
                });

                const data = await response.json();
                const aiResponse = data.generated_text || data[0]?.generated_text || "I'm a bit tired, can you say that again?";
                
                document.getElementById(loadingId).innerText = aiResponse;
            } catch (error) {
                document.getElementById(loadingId).innerText = "Connection lost. Try again!";
            }
            chatBox.scrollTop = chatBox.scrollHeight;
        }
    </script>
</body>
</html>

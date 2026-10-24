matchmaking:</p>
            <ol class="list-decimal list-inside space-y-2 text-xs text-gray-300">
                <li>Create a free project at <a href="https://console.firebase.google.com" target="_blank" class="text-amber-400 underline">firebase.google.com</a>.</li>
                <li>Enable <strong>Anonymous Authentication</strong> & <strong>Realtime Database</strong>.</li>
                <li>Paste your config into the Firebase script section in this file.</li>
            </ol>
            <button onclick="toggleModal('firebase-modal')" class="w-full bg-amber-600 hover:bg-amber-500 text-black font-bold py-2 rounded">Close</button>
        </div>
    </div>

    <!-- Main Game Logic Script -->
    <script>
        // Game State Variables
        let gameState = {
            month: 1,
            gnp: 26.8,
            treasury: 1450,
            approval: 68,
            threat: 'MODERATE',
            tax: 28,
            defense: 35,
            welfare: 37,
            roomCode: null,
            selectedRegion: 'North America'
        };

        function updatePolicies() {
            gameState.tax = document.getElementById('slider-tax').value;
            gameState.defense = document.getElementById('slider-defense').value;
            gameState.welfare = document.getElementById('slider-welfare').value;

            document.getElementById('val-tax').innerText = gameState.tax + '%';
            document.getElementById('val-defense').innerText = gameState.defense + '%';
            document.getElementById('val-welfare').innerText = gameState.welfare + '%';

            // Calculate approval shift based on tax rate balance
            gameState.approval = Math.max(20, Math.min(95, 80 - (gameState.tax * 0.5) + (gameState.welfare * 0.3)));
            document.getElementById('stat-approval').innerText = Math.round(gameState.approval) + '%';
        }

        function advanceTurn() {
            gameState.month++;
            const gnpGrowth = (gameState.welfare * 0.05) - (gameState.tax * 0.02);
            gameState.gnp = Math.max(10, gameState.gnp + gnpGrowth).toFixed(1);
            
            const revenue = gameState.gnp * (gameState.tax / 100) * 100;
            const expenses = (gameState.defense * 20) + (gameState.welfare * 20);
            gameState.treasury = Math.round(gameState.treasury + revenue - expenses);

            document.getElementById('stat-gnp').innerText = '$' + gameState.gnp + ' Trillion';
            document.getElementById('stat-treasury').innerText = '$' + gameState.treasury.toLocaleString() + ' B';

            logEvent(`[MONTH ${gameState.month}] National budget executed. GNP updated to $${gameState.gnp}T.`);
        }

        function selectRegion(name, bloc, wealth, threat) {
            gameState.selectedRegion = name;
            document.getElementById('reg-name').innerText = name;
            document.getElementById('reg-bloc').innerText = bloc;
            logEvent(`Tactical radar focused on region: ${name}`);
        }

        function deployForces() {
            gameState.treasury -= 50;
            document.getElementById('stat-treasury').innerText = '$' + gameState.treasury.toLocaleString() + ' B';
            logEvent(`[MILITARY] Strategic forces deployed to ${gameState.selectedRegion}. -$50B Treasury.`);
        }

        function sendAid() {
            gameState.approval = Math.min(100, gameState.approval + 3);
            document.getElementById('stat-approval').innerText = Math.round(gameState.approval) + '%';
            logEvent(`[DIPLOMACY] Economic trade pact ratified in ${gameState.selectedRegion}. Public approval improved.`);
        }

        function logEvent(msg) {
            const log = document.getElementById('event-log');
            const entry = document.createElement('div');
            entry.className = "p-2 rounded bg-gray-900 border-l-2 border-cyan-500";
            entry.innerText = msg;
            log.prepend(entry);
        }

        function createRoom() {
            const code = 'S1-' + Math.floor(1000 + Math.random() * 9000);
            gameState.roomCode = code;
            document.getElementById('lobby-setup').classList.add('hidden');
            document.getElementById('lobby-active').classList.remove('hidden');
            document.getElementById('display-room-code').innerText = code;
            logEvent(`Multiplayer Room created: ${code}. Share this code with up to 2 other players.`);
        }

        function joinRoom() {
            const input = document.getElementById('room-code-input').value.toUpperCase();
            if(!input) return alert('Please enter a room code');
            gameState.roomCode = input;
            document.getElementById('lobby-setup').classList.add('hidden');
            document.getElementById('lobby-active').classList.remove('hidden');
            document.getElementById('display-room-code').innerText = input;
            document.getElementById('p2-name').innerText = 'You';
            document.getElementById('p2-nation').innerText = 'China';
            logEvent(`Joined Multiplayer Room: ${input}. Synced with commander network.`);
        }

        function sendMessage(e) {
            e.preventDefault();
            const input = document.getElementById('chat-input');
            if(!input.value.trim()) return;
            const chat = document.getElementById('chat-messages');
            const msg = document.createElement('div');
            msg.className = "text-gray-300";
            msg.innerHTML = `<span class="text-cyan-400 font-bold">Commander:</span> ${input.value}`;
            chat.appendChild(msg);
            chat.scrollTop = chat.scrollHeight;
            input.value = '';
        }

        function setMapView(type) {
            logEvent(`Map visualization filter updated to: ${type.toUpperCase()}`);
        }

        function toggleModal(id) {
            document.getElementById(id).classList.toggle('hidden');
        }
    </script>
</body>
</html>

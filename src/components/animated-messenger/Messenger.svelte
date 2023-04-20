<script>
	let codeletters = "■▲▼◣◥◢◣◤◥";
	let message = 0;
	let current_length = 0;
	let fadeBuffer = false;
	let messages = [
		'我们是一支跨国网页设计师团队，提供广泛的服务以帮助企业实现其目标。',
		'我们的团队专注于网页设计、软件开发、数据分析和人工智能。',
        '我们汇聚中国和全球多元文化视角,是中国最具国际化的设计工作室。'
	];

	let text = "";

	function init() {
		setTimeout(animateIn, 100);
	}

	/**
   * @param {number} length
   */
	function generateRandomString(length) {
		let random_text = '';
		while (random_text.length < length) {
			random_text += codeletters.charAt(Math.floor(Math.random() * codeletters.length));
		}

		return random_text;
	}

	function animateIn() {
		if (current_length < messages[message].length) {
			current_length = current_length + 2;
			if (current_length > messages[message].length) {
				current_length = messages[message].length;
			}

			text = generateRandomString(current_length);

			setTimeout(animateIn, 20);
		} else {
			setTimeout(animateFadeBuffer, 20);
		}
	}

	function animateFadeBuffer() {
		if (fadeBuffer === false) {
			fadeBuffer = [];
			for (let i = 0; i < messages[message].length; i++) {
				fadeBuffer.push({ c: (Math.floor(Math.random() * 12)) + 1, l: messages[message].charAt(i) });
			}
		}

		let do_cycles = false;
		let messageText = '';

		for (let i = 0; i < fadeBuffer.length; i++) {
			let fader = fadeBuffer[i];
			if (fader.c > 0) {
				do_cycles = true;
				fader.c--;
				messageText += codeletters.charAt(Math.floor(Math.random() * codeletters.length));
			} else {
				messageText += fader.l;
			}
		}

		text = messageText;

		if (do_cycles === true) {
			setTimeout(animateFadeBuffer, 50);
		} else {
			setTimeout(cycleText, 2000);
		}
	}

	function cycleText() {
		message = message + 1;
		if (message >= messages.length) {
			message = 0;
		}

		current_length = 0;
		fadeBuffer = false;
		text = "";

		setTimeout(animateIn, 200);
	}

	init();
</script>

<style>
	
#messenger {
  position: fixed;
  /* top: 50%; */
  left: 50%;
  transform: translate(-50%, -50%);
  font-family: monospace;
  font-size: 20px;
  white-space: nowrap;
  text-shadow: 0 2px 2px rgba(#000, 0.9);
}
</style>

<div id="messenger">
	{text}
</div>
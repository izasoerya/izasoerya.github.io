<script lang="ts">
	function redirect(location: string) {
		switch (location) {
			case "Home":
				window.location.href = "/";
				break;
			case "About":
				window.location.href = "/about";
				break;
			case "Service":
				window.location.href = "/service";
				break;
			case "Contact":
				window.location.href = "/contact";
				break;
			default:
				break;
		}
		
	}
</script>

<appbar>
	<div>
		<h1>IHZA</h1>
	</div>

	<div style="display: flex; padding-right: 15%;">
		<p class="appbar item">Home</p>
		<p class="appbar item">About</p>
		<p class="appbar item">Service</p>
		<p class="appbar item" on:click={() => redirect("Contact")}>Contact</p>
	</div>
</appbar>

<content>
	<div class="content header">
		<h1>WELCOME TO MY WEB PORTFOLIO!</h1>
	</div>

	<div class="content subheader">
		<h2 style="margin: 0px; padding-top:1%">I'm a Software Engineer</h2>
	</div>

	<div class="content fill">
		<p>
			I'm Software Engineer with experience for over 1 years. I familiar with mobile development,
			web development, firmware / embedded development, and many more!
		</p>
	</div>

	<div style="display: flex; padding-left:2.8%">
		<img src="logo/linkedin_logo.svg" alt="ihza" class="content logo" />
		<img src="logo/whatsapp_logo.svg" alt="ihza" class="content logo" />
	</div>
</content>

<style>
	:root {
		font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
		font-weight: 400;

		color-scheme: light dark;
		color: rgba(255, 255, 255, 0.87);
		background-image: linear-gradient(to right, #0f0c29, #1f2235);

		font-synthesis: none;
		text-rendering: optimizeLegibility;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
	}

	appbar {
		display: flex;
		width: 90%;
		margin-left: auto;
		margin-right: auto;
		align-items: center;
		justify-content: space-between;
	}

	.appbar.item {
		display: flex;
		justify-content: flex-end;
		align-items: flex-end;
		font-size: 24px;
		font-weight: bold;
		padding-right: 15%;
		transition: filter 0.3s ease;
		font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
	}

	.appbar.item:hover {
		color: #f15365;
		cursor: pointer;
		filter: drop-shadow(0px 2px 8px rgba(241, 83, 101, 0.75));
	}

	content {
		padding-top: 30%;
	}

	.content.header {
		width: 40%;
		display: flex;
		padding-left: 5%;
		align-items: center;
		justify-content: left;
		height: max-content;
		font-size: 10px;
	}

	@keyframes blink {
		0%,
		100% {
			opacity: 1;
		}
		50% {
			opacity: 0;
		}
	}

	.content.subheader {
		padding-left: 5%;
		padding-top: 3%;
		align-items: center;
		justify-content: left;
		font-size: 32px;
		display: flex; /* Changed from default to flex */
	}

	.content.subheader::after {
		content: '|'; /* Represents the cursor */
		font-size: 42px;
		opacity: 1;
		margin-left: 10px;
		animation: blink 1s infinite; /* Apply the blinking animation */
		font-weight: normal; /* Optional: Adjust to match your design */
	}

	.content.fill {
		width: 40%;
		display: flex;
		padding-left: 5%;
		align-items: left;
		justify-content: left;
		height: max-content;
		font-size: 18px;
		text-align: justify;
	}

	.content.logo {
		display: flex;
		padding-left: 2%;
		padding-top: 1%;
		width: 3%;
		height: 3%;
		object-fit: cover;
		object-position: center;
	}

	.content.logo:hover {
		cursor: pointer;
		transform: scale(1.2);
		transition:
			transform 0.25s,
			filter 0.25s;
		transition: filter 0.3s ease;
		filter: drop-shadow(0px 2px 8px rgba(241, 83, 101, 0.75));
	}

	h1 {
		font-size: 3.2em;
		line-height: 1.1;
		color: #ff3f55;
	}
</style>

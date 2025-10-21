<h1 align="center">DISCORD VOTING SYSTEM BOT</h1>
<p align="center">An advanced Discord bot for democratic mute and kick voting and server management.<br>Easy, simple and fast setup and no third party apps required</p>

<p align="center">
	<img src="assets/previews/preview-discord-bot.png" alt="Discord Voting System Bot Preview" style="width:100%; height:auto;">
</p>

<h1></h1>

<p align="center">
    <img height="56" src="https://cdn.jsdelivr.net/npm/@intergrav/devins-badges@3/assets/cozy/built-with/markdown_vector.svg">
    <a href="https://itsmarian.is-a.dev/" target="_blank">
        <img height="56" src="https://cdn.jsdelivr.net/npm/@intergrav/devins-badges@3/assets/cozy/documentation/readthedocs_vector.svg">
    </a>
    <a href="https://itsmarian.is-a.dev/" target="_blank">
        <img height="56" src="https://cdn.jsdelivr.net/npm/@intergrav/devins-badges@3/assets/cozy/documentation/website_vector.svg">
    </a>
</p>
<p align="center">
    <a href="https://ko-fi.com/itsmarian/" target="_blank">
        <img  height="56" src="https://cdn.jsdelivr.net/npm/@intergrav/devins-badges@3/assets/cozy/donate/kofi-singular_vector.svg">
    </a>
    <a href="https://discord.com/users/860122608682795028" target="_blank">
        <img height="56" src="https://cdn.jsdelivr.net/npm/@intergrav/devins-badges@3/assets/cozy/social/discord-singular_vector.svg">
    </a>
    <a href="https://github.com/itsmarianmc/" target="_blank">
        <img alt="github-singular" height="56" src="https://cdn.jsdelivr.net/npm/@intergrav/devins-badges@3/assets/cozy/social/github-singular_vector.svg">
    </a>
</p>

<h1></h1>

<h3>Features:</h3>
<ul>
	<li>
		<strong>Votekick:</strong>
		Starts a vote to remove a user from voice channel
	</li>
	<li>
		<strong>Votemute:</strong>
		Starts a vote to mute a user for specified duration
	</li>
	<li>
		<strong>Real-time Results:</strong>
		Live results with progress bars and percentages as discord widgets
	</li>
	<li>
		<strong>Automatic Execution:</strong>
		Actions automatically execute when vote passes or when more than 50% of votes is reached
	</li>
	<li>
		<strong>Server-wide Mute:</strong>
		Instant server-wide mute for a selected time (up to 10 minutes)
	</li>
	<li>
		<strong>Server-wide Timeout:</strong>
		Instant server-wide timeout (up to 10 minutes)
	</li>
	<li>
		<strong>Clear Chat:</strong>
		Complete channel purge (confirmation required before clearing)
	</li>
	<li>
		<strong>Member List:</strong>
		Alphabetical list of all server members with statistics
	</li>
	<li>
		<strong>Statistics:</strong>
		Online status, bot count, server creation date
	</li>
	<li>
		<strong>Democratic System:</strong>
		Only voice channel members can vote with >50% quorum required
	</li>
	<li>
		<strong>Live Features:</strong>
		Real-time result display, visual progress bars, countdown timer
	</li>
	<li>
		<strong>Easy Setup:</strong>
		Simple configuration with no third-party apps required
	</li>
	<li>
		<strong>100% Free:</strong>
		Fully functional with no hidden costs or subscriptions
	</li>
	<li>
		<strong>Open Source:</strong>
		Available on GitHub for anyone to inspect, modify, and contribute to the codebase
	</li>
</ul>

<section>
	<h2>HOW TO SET UP</h2>
	<h3>Prerequisites</h3>
	<p>Before starting, make sure you have:</p>
	<ul>
		<li>Python 3.8 or higher</li>
		<li>Discord Bot Token</li>
		<li>Discord Developer Mode</li>
		<li>Discord Server with administrator permissions</li>
	</ul>
	<h3>1. Create and Invite Bot</h3>
	<p>Follow these steps to create your Discord bot:</p>
	<ol>
		<li>Go to the <a href="https://discord.com/developers/applications">Discord Developer Portal</a></li>
		<li>Create a new Application</li>
		<li>Go to "Bot" tab and create a bot</li>
		<li>Copy the Bot Token</li>
		<li>Enable these Privileged Gateway Intents:
			<ul>
				<li>PRESENCE INTENT</li>
				<li>SERVER MEMBERS INTENT</li>
				<li>MESSAGE CONTENT INTENT</li>
			</ul>
		</li>
		<li>Invite bot to your server with these permissions:
			<pre><code>Administrator</code></pre>
		</li>
		<li>Create a "VOTING" role (or use a standard role for verified users)</li>
	</ol>
	<h3>2. Installation</h3>
	<p>Clone the repository and install dependencies:</p>
	<pre><code># Clone repository
git clone https://github.com/your-username/discord-voice-vote-bot.git
cd discord-voice-vote-bot
# Install dependencies
pip install discord.py python-dotenv</code></pre>
	<h3>3. Configuration</h3>
	<p>Open the <code>release-bot.py</code> file in your preferred editor</p>
	<p>Modify these constants:</p>
	<pre>
    <code># Enter the copied bot token here (in the brackets, don't replace them!)
    BOTTOKEN = "YOUR_BOT_TOKEN_HERE"
    # Copy the Role ID of the voting role
    VOTE_ROLE_ID = 1234567891011121314
    # Copy the Role ID which can perform admin commands (like /clearchat)
    ADMIN_ROLE_ID = 1234567891011121314
    # Copy the Channel ID in which the voting system should be used
    ALLOWED_CHANNEL_ID = 1234567891011121314</code>
    </pre>
	<p><strong>How to find IDs:</strong></p>
	<p>Before doing: Enable Discord Developer Mode in User Settings → Advanced → Developer Mode</p>
	<ul>
		<li><strong>Bot Token:</strong> Discord Developer Portal → Application → Bot → Token</li>
		<li><strong>Role IDs:</strong> Discord → Server Settings → Roles → Right-click role → Copy ID</li>
		<li><strong>Channel ID:</strong> Right-click channel → Copy ID</li>
	</ul>
	<h3>4. Start Bot</h3>
	<p>Open the CMD in the folder of the bot and enter:</p>
	<pre><code>python release-bot.py</code></pre>
	<p>The bot should now be online and ready to use!</p>
</section>

<h1></h1>

<section>
	<h2>Available Commands</h2>
	<h3>For Users with Vote Role</h3>
	<p>Users with the voting role can use these commands:</p>
	<table>
		<tr>
			<th>Command</th>
			<th>Description</th>
			<th>Parameters</th>
			<th>Example</th>
		</tr>
		<tr>
			<td><code>/votekick</code></td>
			<td>Starts vote kick</td>
			<td><code>person</code>: User</td>
			<td>/votekick @itsmarian.mc</td>
		</tr>
		<tr>
			<td><code>/votemute</code></td>
			<td>Starts vote mute</td>
			<td><code>person</code>: User, <code>time</code>: String</td>
			<td>/votemute @itsmarian.mc 1m30s</td>
		</tr>
		<tr>
			<td><code>/members</code></td>
			<td>Shows member list</td>
			<td>-</td>
			<td>-</td>
		</tr>
	</table>
	<h3>Admin Only Commands</h3>
	<p>Users with the admin role can use these powerful commands:</p>
	<table>
		<tr>
			<th>Command</th>
			<th>Description</th>
			<th>Parameters</th>
			<th>Example</th>
		</tr>
		<tr>
			<td><code>/servermute</code></td>
			<td>Instant server mute</td>
			<td><code>person</code>: User, <code>time</code>: String</td>
			<td>/servermute @itsmarian 3m20s</td>
		</tr>
		<tr>
			<td><code>/servertimeout</code></td>
			<td>Instant timeout</td>
			<td><code>person</code>: User, <code>time</code>: String</td>
			<td>/servertimeout @itsmarian.mc 8m</td>
		</tr>
		<tr>
			<td><code>/clearchat</code></td>
			<td>Clears entire chat</td>
			<td>-</td>
			<td>-</td>
		</tr>
	</table>
	<h3>Time Formatting</h3>
	<p>You can specify time in various formats:</p>
	<ul>
		<li><code>30s</code> - 30 seconds</li>
		<li><code>1m</code> - 1 minute</li>
		<li><code>1m30s</code> - 1 minute 30 seconds</li>
		<li><code>90</code> - 90 seconds</li>
	</ul>
	<p><strong>Maximum mute/timeout duration: 10 minutes</strong></p>
	<p>For all other actions use the native discord timeout system!</p>
</section>

<h1></h1>

<section>
	<h2>Voting System</h2>
	<details>
		<summary>
			<h3>How It Works</h3>
		</summary>
		<p>The voting system follows a democratic process:</p>
		<ol>
			<li><strong>Start:</strong> User with vote role starts vote</li>
			<li><strong>Eligibility:</strong> Only voice channel members can vote</li>
			<li><strong>Quorum:</strong> >50% of channel members must approve</li>
			<li><strong>Duration:</strong> Vote runs for 30 seconds</li>
			<li><strong>Automatic Execution:</strong> Action executes immediately if successful</li>
		</ol>
	</details>
	<details>
		<summary>
			<h3>Live Features</h3>
		</summary>
		<p>The voting system includes real-time features for better user experience:</p>
		<ul>
			<li>Real-time result display</li>
			<li>Visual progress bars</li>
			<li>Current voter display</li>
			<li>Countdown timer</li>
			<li>Automatic updates</li>
		</ul>
	</details>
</section>

<h1></h1>

<section>
	<h2>Permissions</h2>
	<details>
		<summary>
			<h3>Required Bot Permissions</h3>
		</summary>
		<p>Administrator (recommended) or individually:</p>
		<ul>
			<li>Read/send/manage messages</li>
			<li>Move members</li>
			<li>Mute members</li>
			<li>Manage timeouts</li>
			<li>Manage roles</li>
		</ul>
	</details>
	<details>
		<summary>
			<h3>Role System</h3>
		</summary>
		<p>The bot uses a role-based permission system:</p>
		<ul>
			<li><strong>VOTE_ROLE_ID:</strong> Permission for <code>/votekick</code> and <code>/votemute</code></li>
			<li><strong>ADMIN_ROLE_ID:</strong> Permission for admin commands</li>
			<li><strong>ALLOWED_CHANNEL_ID:</strong> Channel where commands can be used</li>
		</ul>
	</details>
</section>

<h1></h1>

<section>
	<h2>Frequently Asked Questions</h2>
	<details>
		<summary>
			<h3>Bot not responding</h3>
		</summary>
		<p>The bot not responding can have many causes:</p>
		<ul>
			<li>Check bot token</li>
			<li>Verify bot is invited to server</li>
			<li>Confirm intents are enabled</li>
		</ul>
	</details>
	<details>
		<summary>
			<h3>Commands not visible</h3>
		</summary>
		<p>Directly after the installation or after adding new commands, the commands may not be visible instantly, so you can try this:</p>
		<ul>
			<li>Restart bot</li>
			<li>Wait for command sync (can take up to 1 hour)</li>
			<li>Refresh discord application [CTRL + R]</li>
		</ul>
	</details>
	<details>
		<summary>
			<h3>Permission Errors</h3>
		</summary>
		<p>Sometimes the bot does not have all the permissions it needs so you may have to check its permissions:</p>
		<ul>
			<li>Check bot has administrator permission</li>
			<li>Ensure bot role is above user roles</li>
		</ul>
	</details>
	<details>
		<summary>
			<h3>Votes not working</h3>
		</summary>
		<p>Sometimes the votes may not work correctly after the setup so there are some things you have to consider:</p>
		<ul>
			<li>Verify vote role is configured correctly</li>
			<li>Check users are in voice channel</li>
			<li>Check for correct voting channel ID and user IDs</li>
		</ul>
	</details>
	<details>
		<summary>
			<h3>How does the voting system work?</h3>
		</summary>
		<p>The voting system is democratic and fair:</p>
		<ul>
			<li>Only users in the same voice channel can vote</li>
			<li>More than 50% approval required for action to execute</li>
			<li>Vote duration is 30 seconds</li>
			<li>Real-time results with progress bars</li>
		</ul>
	</details>
	<details>
		<summary>
			<h3>Can I customize the bot?</h3>
		</summary>
		<p>Yes, the bot is open source and customizable:</p>
		<ul>
			<li>Modify vote duration in the code</li>
			<li>Change quorum percentage requirements</li>
			<li>Add custom commands</li>
			<li>Adjust time limits for mutes and timeouts</li>
		</ul>
	</details>
	<details>
		<summary>
			<h3>Is this bot optimized for large servers?</h3>
		</summary>
		<p>The bot works best on small to medium servers:</p>
		<ul>
			<li>Optimized for servers under 1000 members</li>
			<li>May experience performance issues on very large servers</li>
			<li>Member list command can be slow on large servers</li>
		</ul>
	</details>
	<details>
		<summary>
			<h3>What Python version do I need?</h3>
		</summary>
		<p>Python requirements:</p>
		<ul>
			<li>Python 3.8 or higher required</li>
			<li>Python 3.10+ recommended for best performance</li>
			<li>discord.py library required</li>
			<li>python-dotenv for configuration management</li>
		</ul>
	</details>
	<div>
		<p>Still have questions? <a href="https://support.itsmarian.is-a.dev/?utm_origin=https://github.com/itsmarianmc/DISCORD-VOTING-SYSTEM-BOT&utm_page=README&page_pos=support_info_lai">Contact me</a> or <a href="https://github.com/itsmarianmc/DISCORD-VOTING-SYSTEM-BOT/issues">open an issue on GitHub</a>.</p>
	</div>
</section>

<h1></h1>

<section>
	<h2>File Structure & Usage Tips</h2>
	<details>
		<summary>
			<h3>File Structure</h3>
		</summary>
		<p>The bot project has a simple file structure:</p>
		<pre><code>discord-voice-vote-bot/
├── release-bot.py      # Main bot code
├── README.md           # This file
└── requirements.txt    # Python dependencies</code></pre>
	</details>
	<details>
		<summary>
			<h3>Voice Channel Setup</h3>
		</summary>
		<p>Important considerations for voice channel configuration:</p>
		<ul>
			<li>Ensure bot has access to all voice channels</li>
			<li>Test permissions before deployment</li>
			<li>Check bot role hierarchy in server settings</li>
		</ul>
	</details>
	<details>
		<summary>
			<h3>Role Management</h3>
		</summary>
		<p>Best practices for managing roles:</p>
		<ul>
			<li>Assign vote role to trusted members</li>
			<li>Restrict admin role to server moderators and admins</li>
			<li>Keep bot role above user roles in hierarchy</li>
		</ul>
	</details>
	<details>
		<summary>
			<h3>Channel Restriction</h3>
		</summary>
		<p>Control where the bot can be used:</p>
		<ul>
			<li>Use dedicated bot channel for commands</li>
			<li>Prevent spam in other channels</li>
			<li>Configure ALLOWED_CHANNEL_ID correctly</li>
		</ul>
	</details>
	<details>
		<summary>
			<h3>Debugging</h3>
		</summary>
		<p>The bot logs important events to console:</p>
		<ul>
			<li>Login status</li>
			<li>Synced commands</li>
			<li>Server list</li>
			<li>Error messages and stack traces</li>
		</ul>
	</details>
</section>

<h1></h1>

<p align="center">
    <span>&copy; 2025 itsmarian | All rights reserved.</span>
</p>
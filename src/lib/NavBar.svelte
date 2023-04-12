<script>
	let menuOpen = false;
	let userOpen = false;
</script>

<svelte:window />

<nav id="navbar-main" class="navbar is-fixed-top">
	<div class="navbar-brand">
		<a href="/" class="navbar-item mobile-aside-button">
			<span class="icon"><i class="mdi mdi-forwardburger mdi-24px" /></span>
		</a>
		<div class="navbar-item">
			<div class="control"><input placeholder="Search everywhere..." class="input" /></div>
		</div>
	</div>
	<div class="navbar-brand is-right">
		<a href="/" class="navbar-item --jb-navbar-menu-toggle" data-target="navbar-menu">
			<span class="icon"><i class="mdi mdi-dots-vertical mdi-24px" /></span>
		</a>
	</div>
	<div class="navbar-menu" id="navbar-menu">
		<div class="navbar-end">
			<!-- svelte-ignore a11y-click-events-have-key-events -->
			<div
				class="navbar-item dropdown has-divider {menuOpen == true ? 'active' : ''}"
				on:mouseleave={() => {
					menuOpen = !menuOpen;
				}}
			>
				<!-- svelte-ignore a11y-mouse-events-have-key-events -->
				<span
					class="navbar-link"
					on:mouseover={() => {
						menuOpen = !menuOpen;
					}}
				>
					<span class="icon"><i class="mdi mdi-menu" /></span>
					<span>Sample Menu</span>
					<span class="icon">
						<i class="mdi mdi-chevron-down" />
					</span>
				</span>
				<div class="navbar-dropdown">
					<a href="/" class="navbar-item">
						<span class="icon"><i class="mdi mdi-account" /></span>
						<span>My Profile</span>
					</a>
					<a href="/" class="navbar-item">
						<span class="icon"><i class="mdi mdi-settings" /></span>
						<span>Settings</span>
					</a>
					<a href="/" class="navbar-item">
						<span class="icon"><i class="mdi mdi-email" /></span>
						<span>Messages</span>
					</a>
					<hr class="navbar-divider" />
					<a href="/" class="navbar-item">
						<span class="icon"><i class="mdi mdi-logout" /></span>
						<span>Log Out</span>
					</a>
				</div>
			</div>
			<div
				class="navbar-item dropdown has-divider has-user-avatar {userOpen == true ? 'active' : ''}"
				on:mouseleave={() => {
					userOpen = !userOpen;
				}}
			>
				<!-- svelte-ignore a11y-click-events-have-key-events -->
				<!-- svelte-ignore a11y-mouse-events-have-key-events -->
				<span
					class="navbar-link"
					on:mouseover={() => {
						userOpen = !userOpen;
					}}
				>
					<div class="user-avatar">
						<img
							src="https://avatars.dicebear.com/v2/initials/john-doe.svg"
							alt="John Doe"
							class="rounded-full"
						/>
					</div>
					<div class="is-user-name"><span>John Doe</span></div>
					<span class="icon"><i class="mdi mdi-chevron-down" /></span>
				</span>
				<div class="navbar-dropdown">
					<a href="profile.html" class="navbar-item">
						<span class="icon"><i class="mdi mdi-account" /></span>
						<span>My Profile</span>
					</a>
					<a href="/" class="navbar-item">
						<span class="icon"><i class="mdi mdi-settings" /></span>
						<span>Settings</span>
					</a>
					<a href="/" class="navbar-item">
						<span class="icon"><i class="mdi mdi-email" /></span>
						<span>Messages</span>
					</a>
					<hr class="navbar-divider" />
					<a href="/" class="navbar-item">
						<span class="icon"><i class="mdi mdi-logout" /></span>
						<span>Log Out</span>
					</a>
				</div>
			</div>
			<a href="//tailwind-admin-templates" class="navbar-item has-divider desktop-icon-only">
				<span class="icon"><i class="mdi mdi-help-circle-outline" /></span>
				<span>About</span>
			</a>
			<a
				href="https://github.com/justboil/admin-one-tailwind"
				class="navbar-item has-divider desktop-icon-only"
			>
				<span class="icon"><i class="mdi mdi-github-circle" /></span>
				<span>GitHub</span>
			</a>
			<a title="Log out" href="/" class="navbar-item desktop-icon-only">
				<span class="icon"><i class="mdi mdi-logout" /></span>
				<span>Log out</span>
			</a>
		</div>
	</div>
</nav>

<script>
	import { page } from '$app/stores';
	$: active = $page.route.id;
</script>

<aside class="aside is-placed-left is-expanded">
	<div class="aside-tools">
		<div>
			Admin <b class="font-black">One</b>
		</div>
	</div>
	<div class="menu is-menu-main">
		<p class="menu-label">General</p>
		<ul class="menu-list">
			<li class={active == '/' ? 'active' : ''}>
				<a href="/">
					<span class="icon"><i class="mdi mdi-desktop-mac" /></span>
					<span class="menu-item-label">Dashboard</span>
				</a>
			</li>
		</ul>
		<p class="menu-label">Examples</p>
		<ul class="menu-list">
			<li class="--set-active-tables-html {active == '/tables' ? 'active' : ''}">
				<a href="/tables">
					<span class="icon"><i class="mdi mdi-table" /></span>
					<span class="menu-item-label">Tables</span>
				</a>
			</li>
			<li class="--set-active-forms-html {active == '/forms' ? 'active' : ''}">
				<a href="/forms">
					<span class="icon"><i class="mdi mdi-square-edit-outline" /></span>
					<span class="menu-item-label">Forms</span>
				</a>
			</li>
			<li class="--set-active-profile-html">
				<a href="/">
					<span class="icon"><i class="mdi mdi-account-circle" /></span>
					<span class="menu-item-label">Profile</span>
				</a>
			</li>
			<li>
				<a href="/">
					<span class="icon"><i class="mdi mdi-lock" /></span>
					<span class="menu-item-label">Login</span>
				</a>
			</li>
			<li>
				<!-- svelte-ignore a11y-missing-attribute -->
				<a class="dropdown">
					<span class="icon"><i class="mdi mdi-view-list" /></span>
					<span class="menu-item-label">Submenus</span>
					<span class="icon"><i class="mdi mdi-plus" /></span>
				</a>
				<ul>
					<li>
						<a href="/">
							<span>Sub-item One</span>
						</a>
					</li>
					<li>
						<a href="/">
							<span>Sub-item Two</span>
						</a>
					</li>
				</ul>
			</li>
		</ul>
		<p class="menu-label">About</p>
		<ul class="menu-list">
			<li>
				<a href="/" target="_blank" class="has-icon">
					<span class="icon"><i class="mdi mdi-credit-card-outline" /></span>
					<span class="menu-item-label">Premium Demo</span>
				</a>
			</li>
			<li>
				<a href="//tailwind-admin-templates" class="has-icon">
					<span class="icon"><i class="mdi mdi-help-circle" /></span>
					<span class="menu-item-label">About</span>
				</a>
			</li>
			<li>
				<a href="https://github.com/justboil/admin-one-tailwind" class="has-icon">
					<span class="icon"><i class="mdi mdi-github-circle" /></span>
					<span class="menu-item-label">GitHub</span>
				</a>
			</li>
		</ul>
	</div>
</aside>

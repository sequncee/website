<script>
	import { page } from '$app/stores';
	import logo from '$lib/images/svelte-logo.svg';
	import github from '$lib/images/github.svg';
</script>

<header>
	<div class="corner">
		<a href="/">
			<img src={logo} alt="SvelteKit" />
		</a>
	</div>

	<nav>
		<ul>
			<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">主页</a>
			</li>
			<li aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
				<a href="/about">关于我们</a>
			</li>
			<li aria-current={$page.url.pathname.startsWith('/services') ? 'page' : undefined}>
				<a href="/services">产品&服务</a>
			</li>
			<li aria-current={$page.url.pathname.startsWith('/contact') ? 'page' : undefined}>
				<a href="/contact">联系我们</a>
			</li>
			
			<!-- <li aria-current={$page.url.pathname.startsWith('/sverdle') ? 'page' : undefined}>
				<a href="/sverdle">Sverdle</a>
			</li> -->

		</ul>

	</nav>

	<div class="corner" id="github">
		<a href="https://github.com/legiorange">
			<img src={github} alt="GitHub" />
		</a>
	</div>

</header>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@700&display=swap');
	header {
		display: flex;
		justify-content: space-between;
		background-color: #010000;
	}

	.corner {
		width: 3em;
		height: 3em;
	}

	.corner a {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
	}

	.corner img {
		width: 2em;
		height: 2em;
		object-fit: contain;
		
	}
	#github{
		 filter: invert(99%) sepia(18%) saturate(4190%) hue-rotate(290deg) brightness(128%) contrast(94%);
	}

	/* nav {
		display: flex;
		justify-content: center;
		--background: rgba(255, 255, 255, 0.7);
	} */
	.nav {
	display: flex;
	align-items: center;
	justify-content: space-between;
	}
	ul {
  display: flex;
  list-style-type: none;
  
}
nav ul a {
  margin: 10px 30px;
  position: relative;
  color: white;
  font-family: 'Noto Sans SC',"Oswald", sans-serif;
  font-size: 20px;
  text-transform: uppercase;
  text-decoration: none;
}
nav ul a:before {
  position: absolute;
  bottom: -2px;
  content: "";
  width: 100%;
  height: 3px;
  background: var(--highlight);
  transform: translateX(-100%);
  opacity: 0;
}
nav ul a:hover:before {
  opacity: 1;
  transition: 0.5s transform ease, 0.8s opacity ease;
  transform: translateX(0);
}
nav ul .active {
  color: var(--highlight);
}
nav ul .active:hover:before {
  opacity: 0;
}


	a:hover {
		color: #d72323;
	}
</style>

<script>
	export let segment;
</script>

<style>
	nav {
		border-bottom: 1px solid rgba(255,62,0,0.1);
		font-weight: 300;
		padding: 0 1em;
	}

	ul {
		margin: 0;
		padding: 0;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}

	li {
		display: block;
		float: left;
	}

	[aria-current] {
		position: relative;
		display: inline-block;
	}

	[aria-current]::after {
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 2px;
		background-color: rgb(255,62,0);
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 1em 0.5em;
		display: block;
	}
</style>

<nav>
  <div class="mr-6 p-1 float-left">
    <a class="text-blue-800 hover:text-blue-800"
       rel=prefetch aria-current='{segment === undefined ? "page" : undefined}'
       href='.'>M</a>
  </div>

  <ul class="flex flex-row-reverse">
    <li class="mr-6 p-1 order-4">
      <a class="text-blue-500 hover:text-blue-800"
         rel=prefetch aria-current='{segment === "portfolio" ? "page" : undefined}'
         href='portfolio'>Portfolio</a>
    </li>

    <li class="mr-6 p-1 order-3">
      <a class="text-blue-500 hover:text-blue-800"
         rel=prefetch aria-current='{segment === "resume" ? "page" : undefined}'
         href='resume'>Resume</a>
    </li>

    <li class="mr-6 p-1 order-2">
      <a class="text-blue-500 hover:text-blue-800"
         rel=prefetch aria-current='{segment === "about" ? "page" : undefined}'
         href='about'>About</a>
    </li>

    <li class="mr-6 p-1 order-1">
      <a class="text-blue-500 hover:text-blue-800"
         rel=prefetch aria-current='{segment === "contact" ? "page" : undefined}'
         href='contact'>Contact</a>
    </li>

  </ul>

</nav>

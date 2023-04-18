<svelte:head>
	<title>关于我们</title>
	<meta name="description" content="About Sequnce E Team" />
</svelte:head>
<div>

	<h1>关于我们</h1>

</div>
<section class="about">
	<p>Sequnce E 是一家领先的技术公司，提供广泛的服务以帮助企业实现其目标。  我们的专家团队专注于软件开发、数据分析和人工智能。  我们致力于提供创新的解决方案，帮助我们的客户在竞争中保持领先地位。</p>
	<p>在 Sequnce E，我们与客户建立长期关系，密切合作，了解客户的需求并开发满足他们特定要求的定制解决方案。  我们的目标是通过利用最新技术和最佳实践帮助我们的客户取得成功。</p>
	<h3>我们的使命</h3>
	<p>我们的使命是使用新兴技术为您的解决方案提供动力。  我们相信技术应该成为创新和进步的驱动力，我们致力于帮助各种规模的企业利用最新的工具和技术来实现他们的目标。</p>
	
  </section>

<style>
	h1 {
  --s: 0.1em;   /* the thickness of the line */
  --c: #2c4bff; /* the color */
  
  color: #0000;
  padding-bottom: var(--s);
  background: 
    linear-gradient(90deg,var(--c) 50%,#000 0) calc(100% - var(--_p,0%))/200% 100%,
    linear-gradient(var(--c) 0 0) 0% 100%/var(--_p,0%) var(--s) no-repeat;
  -webkit-background-clip: text,padding-box;
          background-clip: text,padding-box;
  transition: 0.5s;
}
h1:hover {--_p: 100%}
div{
	margin: auto;
  margin-top: auto;
  margin-bottom: auto;
margin-bottom: 20px;
margin-top: 20px;
}

body {
  height: 100vh;
  margin: 0;
  display: grid;
  place-content: center;
}

</style>
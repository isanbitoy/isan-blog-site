<template>
	<div class="author">
		<figure>
			<g-image alt="Author image" class="author__image" 
				src="~/assets/images/author.jpg" 
				width="180" height="180" blur="5" />
		</figure>
		
		<h1 v-if="showTitle" class="author__site-title">
			{{ $static.metaData.siteName }}
		</h1>

		<!--<p class="author__intro">
			A simple, hackable & minimalistic starter for Gridsome that uses Markdown for content.
		</p>-->
		<p class="author__intro">
			my personal and minimalist blog site.
		</p>

		<!--<p class="author__links">
			<a href="https://isan-web-profile.netlify.com/" target="_blank">Profile</a>
			<a href="https://github.com/isanbitoy" target="_blank">GitHub</a>
		</p>-->
	</div>
</template>

<static-query>
query {
  metaData {
    siteName
  }
}
</static-query>

<script>
export default {
	props: ['showTitle']
};
</script>
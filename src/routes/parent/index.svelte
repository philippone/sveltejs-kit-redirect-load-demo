<script context="module">
	export const prerender = true;

	export async function load() {
		return {
			status: 302,
			redirect: './parent/child'
		};
	}
</script>

parent page
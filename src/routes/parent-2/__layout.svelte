<script context="module">
	export const prerender = true;

	export async function load({url}) {

		console.log('parent 2 __layout load');

    // load data that should be available in layout and parent page (pass to page via stuff)

	if (url.pathname.endsWith('parent-2')) {
			return {
			status: 302,
			redirect: './parent-2/child'
		};
	}

		return {
			status: 200,
      stuff: {
        loadedData: {}
      }
		};
	}
</script>


<slot/>
<script context="module">
	export const prerender = true;

	export async function load() {

		console.log('parent __layout load');

    // load data that should be available in layout and parent page (pass to page via stuff)

		return {
			status: 200,
      stuff: {
        loadedData: {}
      }
		};
	}
</script>


<slot/>
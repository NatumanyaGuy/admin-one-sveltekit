<script>
	import TitleBar from '$lib/Dashboard/TitleBar.svelte';
	import EmailInput from '$lib/Form/EmailInput.svelte';
	import Select from '$lib/Form/Select.svelte';
	import TelInput from '$lib/Form/TelInput.svelte';
	import TextInput from '$lib/Form/TextInput.svelte';
	import Textarea from '$lib/Form/Textarea.svelte';
	import Button from '$lib/UI/Button.svelte';
</script>

<TitleBar _page="Forms" />

<section class="section main-section">
	<div class="card mb-6">
		<div class="card-content">
			<form method="get">
				<TextInput />

				<EmailInput />

				<TelInput />

				<Select />

				<hr />

				<Textarea />
				<hr />

				<Button type="red">Cancel</Button>
				<Button type="green">Submit</Button>
			</form>
		</div>
	</div>
</section>

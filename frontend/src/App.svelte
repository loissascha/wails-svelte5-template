<script>
	import { QuitApp, MaximiseApp, MinimiseApp } from "../wailsjs/go/app/App";

	let title = "Wails Template";

	function QuitButton() {
		QuitApp();
	}

	function MaximiseButton() {
		MaximiseApp();
	}

	function MinimiseButton() {
		MinimiseApp();
	}
</script>

<main
	class="w-full h-full bg-latte-base dark:bg-mocha-base text-latte-text dark:text-mocha-text grid grid-rows-[auto_1fr]"
>
	<drag
		class="w-full bg-latte-surface0 dark:bg-mocha-surface0 cursor-grabbing"
		style="--wails-draggable:drag"
	>
		<div class="w-full grid grid-cols-3">
			<div></div>
			<div class="text-center py-1">{title}</div>
			<div class="text-right">
				<button
					class="font-bold px-2 py-1"
					onclick={() => {
						MinimiseButton();
					}}>_</button
				><button
					class="font-bold px-2 py-1"
					onclick={() => {
						MaximiseButton();
					}}>O</button
				><button
					class="font-bold px-2 py-1"
					onclick={() => {
						QuitButton();
					}}>X</button
				>
			</div>
		</div>
	</drag>

	<div
		class="grid grid-cols-[300px_1fr] border-l border-b border-r border-latte-surface0 dark:border-mocha-surface0 overflow-y-auto"
	>
		<nav class="bg-latte-surface1 dark:bg-mocha-surface1 p-2"></nav>

		<content class="p-2">
		</content>
	</div>
</main>

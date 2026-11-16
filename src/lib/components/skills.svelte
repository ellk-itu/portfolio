<script lang="ts">
	import ViteIcon from '#lib/assets/icons/Vite.svg?component';
	import BunIcon from '#lib/assets/icons/Bun.svg?component';
	import SvelteIcon from '#lib/assets/icons/Svelte.svg?component';
	import FireBaseIcon from '#lib/assets/icons/Firebase.svg?component';
	import TailWindIcon from '#lib/assets/icons/Tailwind.svg?component';
	import ReactIcon from '#lib/assets/icons/React.svg?component';
	import SassIcon from '#lib/assets/icons/Sass.svg?component';
	import AWSIcon from '#lib/assets/icons/Aws.svg?component';
	import NodeIcon from '#lib/assets/icons/Node.svg?component';
	import PythonIcon from '#lib/assets/icons/Python.svg?component';
	import UvIcon from '#lib/assets/icons/Uv.svg?component';
	import FastAPIIcon from '#lib/assets/icons/FastAPI.svg?component';
	import PyPiIcon from '#lib/assets/icons/PyPi.svg?component';
	import RustIcon from '#lib/assets/icons/Rust.svg?component';
	import SQLiteIcon from '#lib/assets/icons/SQLite.svg?component';
	import MongoDBIcon from '#lib/assets/icons/MongoDB.svg?component';
	import MySQLIcon from '#lib/assets/icons/MySql.svg?component';
	import CSharpIcon from '#lib/assets/icons/CSharp.svg?component';
	import CPlusPlusIcon from '#lib/assets/icons/CPlusPlus.svg?component';
	import ArduinoIcon from '#lib/assets/icons/Arduino.svg?component';
	import TauriIcon from '#lib/assets/icons/Tauri.svg?component';
	import FlutterIcon from '#lib/assets/icons/Flutter.svg?component';
</script>

<div class="min-h-screen flex flex-col justify-center skills">
	<div class="py-8">
		<h1>Using modern <br /> design stacks</h1>
		<h4>What can I say. I’m a gen z developer</h4>
	</div>

	<ul>
		<li>
			<h3>Web</h3>
			<div class="flex flex-col icons-alt flex-1 gap-1 list">
				<div>
					<ViteIcon />
					<p>Vite</p>
				</div>
				<div>
					<BunIcon />
					<p>Bun</p>
				</div>
				<div>
					<SvelteIcon />
					<p>Svelte</p>
				</div>
				<div>
					<FireBaseIcon />
					<p>Firebase</p>
				</div>
				<div>
					<TailWindIcon />
					<p>Tailwindcss</p>
				</div>
			</div>
			<div class="flex flex-col">
				<h5>Alternatively</h5>
				<div class="flex alt-icons gap-1">
					<ReactIcon />
					<SassIcon />
					<AWSIcon />
					<NodeIcon />
				</div>
			</div>
		</li>
		<li>
			<h3>Scripting</h3>
			<div class="flex flex-col icons-alt flex-1 gap-1 list">
				<div>
					<PythonIcon />
					<p>Vite</p>
				</div>
				<div>
					<UvIcon />
					<p>Bun</p>
				</div>
				<div>
					<FastAPIIcon />
					<p>Svelte</p>
				</div>
				<div>
					<FireBaseIcon />
					<p>Firebase</p>
				</div>
			</div>
			<div class="flex flex-col">
				<h5>Alternatively</h5>
				<div class="flex alt-icons gap-1">
					<PyPiIcon />
					<AWSIcon />
				</div>
			</div>
		</li>
		<li>
			<h3>Server</h3>
			<div class="flex flex-col icons-alt flex-1 gap-1 list">
				<div>
					<RustIcon />
					<p>Vite</p>
				</div>
				<div>
					<SQLiteIcon />
					<p>Bun</p>
				</div>
			</div>
			<div class="flex flex-col">
				<h5>Alternatively</h5>
				<div class="flex alt-icons gap-1">
					<MongoDBIcon />
					<MySQLIcon />
					<CSharpIcon />
				</div>
			</div>
		</li>
		<li>
			<h3>Hardware</h3>
			<div class="flex flex-col icons-alt flex-1 gap-1 list">
				<div>
					<CPlusPlusIcon />
					<p>Vite</p>
				</div>
			</div>
			<div class="flex flex-col">
				<h5>Alternatively</h5>
				<div class="flex alt-icons gap-1">
					<RustIcon />
					<ArduinoIcon />
				</div>
			</div>
		</li>
		<li>
			<h3>Phone</h3>
			<div class="flex flex-col icons-alt flex-1 gap-1 list">
				<div>
					<TauriIcon />
					<p>Vite</p>
				</div>
			</div>
			<div class="flex flex-col">
				<h5>Alternatively</h5>
				<div class="flex alt-icons gap-1">
					<FlutterIcon />
					<ReactIcon />
				</div>
			</div>
		</li>
	</ul>
</div>

<style lang="scss">
	p {
		font-family: 'BDO Grotesk', Inter, sans-serif;
	}

	.skills {
		padding: max(0px, calc(var(--font-size) * 4 - 2rem));

		& ul {
			display: flex;
			width: 100%;
			flex-wrap: wrap;

			li {
				min-width: fit-content;
				display: flex;
				flex-direction: column;
				flex-grow: 1;
				gap: 1rem;
				padding: 1rem;
				border-left: 4px solid var(--dark);
			}
		}
	}

	.alt-icons {
		justify-items: center;

		:global(*) {
			fill: var(--dark);

			& path[stroke] {
				fill: none;
				stroke: var(--dark);
			}

			& g[stroke] {
				:global(*) {
					fill: none;
				}
				fill: none;
				stroke: var(--dark);
			}
		}

		:global(*) {
			width: 32px;
			height: 32px;
		}
	}

	.list {
		> div {
			display: flex;
			gap: 1rem;
			align-items: center;

			p {
				font-family: 'BDO Grotesk', Inter, sans-serif;
			}
		}

		:global(*) {
			fill: var(--red);

			& path[stroke] {
				fill: none;
				stroke: var(--red);
			}

			& g[stroke] {
				:global(*) {
					fill: none;
				}
				fill: none;
				stroke: var(--red);
			}
		}
	}
</style>

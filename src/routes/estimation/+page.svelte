<script lang="ts">
	import * as Table from '$lib/components/ui/table';
	import { Button } from '$lib/Components/ui/button';

	// import { AspectRatio } from '$lib/components/ui/aspect-ratio';
	const arrayOfObjects = [
		{
			key1: 'Super Gear',
			key2: 'Nylon PA',
			key3: '...',
			key4: '$86.32',
			key5: '-86.32'
		},
		{
			key1: 'Super Gear',
			key2: 'Nylon PA',
			key3: '...',
			key4: '$86.32',
			key5: '-86.32'
		},
		{
			key1: 'Super Gear',
			key2: 'Nylon PA',
			key3: '...',
			key4: '$86.32',
			key5: '-86.32'
		},
		{
			key1: 'Super Gear',
			key2: 'Nylon PA',
			key3: '...',
			key4: '$86.32',
			key5: '-86.32'
		}
	];
</script>

<div class=" my-8 mx-6 sm:mx-12 flex justify-end">
	<Button href="/estimation/new">New Estimation</Button>
</div>
<div class="mx-4 my-8 overflow-hidden rounded-lg shadow-lg md:mx-12">
	<div class="flex flex-wrap">
		<div class="w-full">
			<div class="">
				<Table.Root class="">
					<Table.Header class="border-b-2  bg-gray-200 text-base font-semibold    ">
						<Table.Row>
							<Table.Head>Name</Table.Head>
							<Table.Head>AM Material</Table.Head>
							<Table.Head>Model</Table.Head>
							<Table.Head>Average Price</Table.Head>
							<Table.Head>Savings</Table.Head>
							<Table.Head></Table.Head>
						</Table.Row>
					</Table.Header>
					<Table.Body>
						{#each arrayOfObjects as a, index}
							<Table.Row class=" border-b text-base ">
								<Table.Cell>{a.key1}</Table.Cell>
								<Table.Cell>{a.key2}</Table.Cell>
								<Table.Cell class="">{a.key3}</Table.Cell>
								<Table.Cell>{a.key4}</Table.Cell>
								<Table.Cell>{a.key5}</Table.Cell>
								<Table.Cell class="text-center">
									<Button>Order</Button>
								</Table.Cell>
							</Table.Row>
						{/each}
					</Table.Body>
				</Table.Root>
			</div>
		</div>
	</div>
</div>

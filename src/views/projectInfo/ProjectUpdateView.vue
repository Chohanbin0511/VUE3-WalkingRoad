<template>
	<TheViewLayout>
		<template #mainPanel>
			<v-container>
				<h1>Update....</h1>
				<v-timeline class="mt-15">
					<v-timeline-item
						v-for="item in updateInfoList"
						:key="item"
						:dot-color="item.color"
						size="x-small"
					>
						{{ item.time }}
						<div class="font-weight-normal">
							<strong>{{ item.text }}</strong>
						</div>
					</v-timeline-item>
				</v-timeline>
			</v-container>
			<!-- 검색 창-->
		</template>
	</TheViewLayout>
</template>

<script setup>
import TheViewLayout from '@/layouts/TheViewLayout.vue';
import { ref } from 'vue';

const updateInfoList = ref([
	{
		color: 'blue',
		text: '길 상세보기 지도 표시',
		time: '2022/10/19',
	},
	{
		color: 'blue',
		text: '카카오 로그인',
		time: '2022/09/25',
	},
	{
		color: 'green',
		text: 'layout 조정',
		time: '2022/09/15',
	},
	{
		color: 'yellow',
		text: 'git Test',
		time: '2022/09/14',
	},
]);
</script>

<style lang="scss" scoped></style>

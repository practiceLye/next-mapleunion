<template>
    <v-app>
        <!-- header -->
        <v-app-bar title="다음에 키울 유니온 캐릭터는?">
            <template v-slot:prepend>
                <v-app-bar-nav-icon />
            </template>
            <template v-slot:append>
                <v-btn icon="mdi-lightbulb-on-outline"></v-btn>
            </template>
        </v-app-bar>
        <!-- body -->
        <v-main class="d-flex flex-column">
            <v-container>
                <!-- input -->
                <v-card class="w-100 px-auto" height="90px">
                    <v-card-text>
                        <v-text-field v-model="input" class="mx-auto" width="50%" label="본캐 닉네임을 입력해주세요." append-inner-icon="mdi-magnify" @click:append-inner="onClickSearch"></v-text-field>
                    </v-card-text>
                </v-card>
                <!-- result -->
                <v-card class="w-100 my-5">
                    <template v-slot:text>
                        <div class="d-flex flex-row">
                            <v-list width="20%" :items="items"></v-list>
                            <v-divider vertical></v-divider>
                            <div class="d-flex flex-column px-5 w-75">
                                <h2 class="d-flex justify-start">이 직업을 키우시는건 어떤가요?</h2>
                                <div class="d-flex justify-center w-100 pt-6">
                                    <div>
                                        <v-img
                                            width="300"
                                            height="300"
                                            aspect-ratio="16/9"
                                            cover
                                            src="https://cdn.vuetifyjs.com/images/parallax/material.jpg"
                                        ></v-img>
                                        <h2>{{ resultCharactor }}</h2>
                                        <p>공격대원 효과</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </template>
                </v-card>
            </v-container>
        </v-main>
        <!-- footer -->
        <!-- <v-footer></v-footer> -->
    </v-app>
</template>
<script setup>
import { ref } from 'vue'

const input = ref('')

const items = ref([
    {
        title: 'Item #1',
    },
    {
        title: 'Item #2',
    },
    {
        title: 'Item #3',
    },
])

const resultCharactor = ref('직업이름')

const onClickSearch = () => {
    console.log('클릭')
}
</script>
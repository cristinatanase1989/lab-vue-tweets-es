<template>
<Actions />
<Message />
<ProfileImage />
<Timestamp />
<User />

<!-- <h3>{{otraInfoQuemMeLlegaDelPadre}}</h3> -->

    <div class="tweet">
        <img src="https://i.imgur.com/9yw1Fyw.jpg" class="profile" alt="profile" />

        <div class="body">
            <div class="top">
                <span class="user">
                    {{tweetHijo[0].user}}
                    <span class="name">Ironhack</span>
                    {{tweetHijo[0].name}}
                    <span class="handle">@ironhack</span>
                    {{tweetHijo[0].handle}}
                </span>

                <span class="timestamp">Nov 30, 2020</span>

            </div>

            <p class="message">
                {{tweetHijo[0].message}}
                On December 7th, we will be hosting a #webinar that will introduce you
                to #SQL! Are you ready? 🚀
            </p>

            <div class="actions">
                <!-- Font Awesome icons -->
                <i class="far fa-comment"></i>
                <i class="fas fa-retweet"></i>
                <i class="far fa-heart"></i>
                <i class="fas fa-share"></i>
            </div>
        </div>

        <i class="fas fa-ellipsis-h"></i>
    </div>
</template>

<style scoped>
a {
    color: #42b983;
}
</style>
 <script setup>
import Actions from './Actions.vue';
import Message from './Message.vue';
import ProfileImage from './ProfileImage.vue';
import Timestamp from './Timestamp.vue';
import User from './User.vue';

import {defineProps} from 'vue';

const props = defineProps([
    'tweetHijo',
    
    // 'otraInfoQuemMeLlegaDelPadre'
]

)


</script>

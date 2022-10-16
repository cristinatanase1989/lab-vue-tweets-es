<!-- <template>
<Actions />
<Message />
<ProfileImage />
<Timestamp />
<User />

<h3>{{otraInfoQuemMeLlegaDelPadre}}</h3> 

    <div class="tweet">
        <img src="https://i.imgur.com/9yw1Fyw.jpg" class="profile" alt="profile" />
 <ProfileImage/>
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
                 Font Awesome icons 
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
    
     'otraInfoQuemMeLlegaDelPadre'
]

)


</script> -->
<template>
    <div class="tweet">
        <ProfileImage :image="props.tweet.user.image" />
        <div class="body">
            <div class="top">
                <User :name="props.tweet.user.name" :handle="props.tweet.user.handle" />
                <!-- <User :userData="{name: props.tweet.user.name, handle: props.tweet.user.handle}" /> -->
                <Timestamp :timestamp="props.tweet.timestamp" />
            </div>
            <Message :message="props.tweet.message" />
            <Action />
        </div>
        <i class="fas fa-ellipsis-h"></i>
    </div>
</template>

<script setup>
import { defineProps } from 'vue'
import ProfileImage from './ProfileImage.vue'
import User from './User.vue';
import Timestamp from './Timestamp.vue';
import Message from './Message.vue';
import Action from './Actions.vue'

const props = defineProps({
    tweet: Object
})
// No da informacion del tipo de prop que recibes
// const props = defineProps(['tweet'])
</script>
  
<style scoped>
a {
    color: #42b983;
}
</style>
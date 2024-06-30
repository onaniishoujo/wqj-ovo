<template>
<div class="mockup-phone absolute left-1/2 -translate-x-1/2 mt-10 shadow-2xl hover:shadow-sm">
    <div class="camera"></div> 
    <div class="display">
        <div class="artboard artboard-demo phone-1 bg-slate-100">
            <div class="absolute top-10 text-center font-semibold z-10 bg-slate-100">
                <span class="absolute w-10 -right-8 -top-4 z-30"><svg id="Flat" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 256 256"><path d="M74,128a10,10,0,1,1-10-10A10.01114,10.01114,0,0,1,74,128Zm118-10a10,10,0,1,0,10,10A10.01146,10.01146,0,0,0,192,118Zm-64,0a10,10,0,1,0,10,10A10.01114,10.01114,0,0,0,128,118Z"/></svg>
                </span>
                <p class="relative w-60 text-center">初2021级4班 (113)</p>
                <span class="absolute w-8 -left-8 -top-2 z-30"><svg viewBox="0 0 512 512" xmlns="http://www.w3.org/2000/svg"><title/><g data-name="1" id="_1"><path d="M353,450a15,15,0,0,1-10.61-4.39L157.5,260.71a15,15,0,0,1,0-21.21L342.39,54.6a15,15,0,1,1,21.22,21.21L189.32,250.1,363.61,424.39A15,15,0,0,1,353,450Z"/></g></svg></span>
            </div>
            <div ref="msgBody" class="w-4/5 mx-auto mt-0 overflow-auto scroll mb-16">
                <div class="chat chat-start">
                <div class="chat-image avatar">
                    <div class="w-10 rounded-full">
                    <img alt="Tailwind CSS chat bubble component" src="/src/assets/wag.jpg" />
                    </div>
                </div>
                <div class="chat-header">
                    王安国
                    <time class="text-xs opacity-50">12:45</time>
                </div>
                <div class="chat-bubble bg-white text-black">@王庆杰妈妈 王庆杰又逃课去嫖娼了! 还没给钱!</div>
                <div class="chat-footer opacity-50">
                    Delivered
                </div>
                </div>
            
                <div class="chat chat-start">
                <div class="chat-image avatar">
                    <div class="w-10 rounded-full">
                    <img alt="Tailwind CSS chat bubble component" src="/src/assets/wico.jpg" />
                    </div>
                </div>
                <div class="chat-header">
                    王庆杰妈妈
                    <time class="text-xs opacity-50">12:45</time>
                </div>
                <div class="chat-bubble bg-white text-black">不好意思, 我们家杰哥从小就爱嫖, 让您费心了🌹🌹</div>
                <div class="chat-footer opacity-50">
                    Delivered
                </div>
                </div>
                
                <div class="chat chat-end">
                <div class="chat-image avatar">
                    <div class="w-10 rounded-full">
                    <img alt="Tailwind CSS chat bubble component" src="/src/assets/avatar.jpg" />
                    </div>
                </div>
                <div class="chat-header">
                    オナニー少女w
                    <time class="text-xs opacity-50">12:46</time>
                </div>
                <div class="chat-bubble bg-green-400 text-black">@王庆杰妈妈 杰哥包夜的钱转给我谢谢</div>
                <div class="chat-footer opacity-50">
                    Seen at 12:46
                </div>
                </div>
                <div class="absolute w-full h-10 bottom-5 left-0 flex items-center z-10">
                    <button class="btn btn-circle btn-outline btn-sm mx-1 ml-3 translate-x-1 hover:bg-gray-100">
                        <svg viewBox="-6.4 -6.4 44.80 44.80" xmlns="http://www.w3.org/2000/svg" fill="#000000" transform="rotate(90)matrix(1, 0, 0, 1, 0, 0)"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <g fill="none" fill-rule="evenodd"> <path d="m0 0h32v32h-32z"></path> <path d="m16 23.3333333c.7054971 0 1.3378647.3131046 1.7657251.8079361-.5364679.4639137-1.1239266.9712419-1.7657251 1.5255163-.6383398-.5591127-1.2226122-1.0708429-1.7573994-1.5392067.4304214-.4865055 1.0579721-.7942457 1.7573994-.7942457zm0-5.6666666c2.3048894 0 4.4576506 1.2009433 5.704885 3.0752846-.4130934.3552245-.9166883.7900247-1.5310671 1.3205162-.8551473-1.4455488-2.4631903-2.3958008-4.1738179-2.3958008-1.6939811 0-3.2935514.9375716-4.153541 2.3633155-.6104727-.535199-1.1109102-.9732794-1.5210712-1.3322518 1.2518588-1.8474905 3.3914515-3.0310637 5.6746122-3.0310637zm.0064666-5.8333334c3.6910267 0 7.7501479 2.2543887 9.7175152 5.4253088-.7374102.6387525-1.2199186 1.0573621-1.5362933 1.3321302-1.5123244-2.7101472-5.0642122-4.757439-8.1812219-4.757439-3.0920156 0-6.62217548 2.0244039-8.15333066 4.7080787-.3127146-.2753249-.79333049-.6962176-1.52619224-1.3382492 1.98147431-3.140502 6.0163913-5.3698295 9.6795229-5.3698295zm.0032333-5.8333333c5.4911176 0 11.2324815 3.15266123 14.167125 7.4001118-.5539993.4804544-1.0599156.9185988-1.5234281 1.3200576-2.5144049-3.7988077-7.7353145-6.7201694-12.6436969-6.7201694-4.8664206 0-10.02085911 2.8700013-12.59269965 6.655398-.45802592-.4033711-.96136471-.8444698-1.51080184-1.3259792 2.98225947-4.22806264 8.65545979-7.3294188 14.10350149-7.3294188z" fill="#000000"></path> </g> </g></svg>
                    </button>
                    <input @focus="iptFocus" v-model="msg" ref="ipt" id="iptc" type="text" placeholder="@王庆杰妈妈" class="input border-none w-48 h-10 mx-1">
                    <button class="btn btn-circle btn-sm mx-1">
                        <img src="/src/assets/laughing.svg">
                    </button>
                    <button @click="submitText" id="submit_button" ref="submitButton" class="btn btn-circle btn-outline btn-sm mx-1 text-lg">+</button>
                </div>
        </div>
    </div>
</div>
</div>
</template>

<script setup lang="ts">
import { ref, type Ref } from 'vue'

let msg: any = ref('这里能输入并发送消息')
const msgBody: Ref<HTMLElement | undefined> = ref()
const submitButton: Ref<HTMLElement | undefined> = ref()
const ipt: Ref<HTMLElement | undefined> = ref()


function submitText(): void {
    if (msgBody.value) {
        msg.value = msg.value.replace(/</g, '')
        msg.value = msg.value.replace(/>/g, '')
        let msgTemplate: string = `<div class="chat chat-end"><div class="chat-image avatar"><div class="w-10 rounded-full"><img src="/src/assets/avatar.jpg" /></div></div><div class="chat-header">オナニー少女w<time class="text-xs opacity-50">12:46</time></div><div class="chat-bubble bg-green-400 text-black break-all">${msg.value}</div><div class="chat-footer opacity-50">Seen at 12:46</div>`
        msgBody.value.innerHTML += msgTemplate
        let s = document.getElementById('submit_button') as HTMLElement
        msg = document.getElementById('iptc') as HTMLElement
        s.onclick = submitText
        msgBody.value.scrollTop = msgBody.value.scrollHeight
    }
}

function iptFocus(): void {
    if (submitButton.value && ipt.value) {
        let v = submitButton.value

        v.innerHTML = '发送'
        v.classList.remove('text-lg')

        ipt.value.style.width = '170px'

        v.style.width = '50px'
        v.style.backgroundColor = 'rgb(74 222 128)'
        v.style.color = 'white'
        v.classList.add('rounded-md')
    }
}
</script>

<style>
.scroll {
    scrollbar-width: none;
    -ms-overflow-style: none;
}

.scroll::-webkit-scrollbar {
  display: none;
}

</style>
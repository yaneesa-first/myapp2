<template>
    <div class= "container">
        <img :src="picture" :width="size" :height="size" style="margin-top: 20px;">
        <form @submit.prevent="submitForm">
            กรอกชื่อเล่น <input type="text" ref="nicknameEl">
            <input type="submit" value="บันทึก" style="margin-top: 20px;">
        </form>
        <p>ชื่อ - นามสกุล : {{ getFullname() }}</p>
        <p>อายุ : {{ age }}</p>
        <p>ชื่อเล่น : {{ nickname }}</p>
        <button @click="toggleVisible"> {{ isVisible? "ซ่อน" : "แสดง" }}รายละเอียด</button>
        <div v-show="isVisible">
        <p>ที่อยู่ : <span v-html="address"></span></p>
        <p v-if="hobby.length ===0">ไม่มีงานอดิเรก</p>
        <div v-else>
            <p>งานอดิเรก :</p>
        <ul>
            <li v-for="items in hobby">{{ items }}</li>
        </ul>
        </div>
        <p>ข้อมูลพื้นฐาน :</p>
        <ul>
           <li>เพศ : {{ general.gender }}</li>
           <li>น้ำหนัก : {{ general.weight }}</li>
           <li>ส่วนสูง : {{ general.height }}</li>
           <li>โรคประจำตัว : {{ general.status }}</li>
        </ul>
        </div>
    </div>
</template>

<script>
export default{
    data(){
        return{
            firstname:"Yaneesa",
            lastname:"Chaisuwan",
            nickname:"",
            age: 19,
            address: "<i>Chonburi</i>",
            picture:"https://rms.tatc.ac.th/files/importpicstd/01/66309010007.jpg",
            size:150,
            hobby: ["ฟังเพลง","เล่นเกม","ดูหนัง"],
            general:{gender:"หญิง",weight:62.5,height:157,status:false},
            isVisible: false,
        };
    },
    methods: {
        getFullname(){
            return (this.firstname) + (this.lastname);
        },
        toggleVisible(){
            this.isVisible = !this.isVisible
        },
        submitForm(){
            this.nickname = this.$refs.nicknameEl.value
        }
    },
};
</script>
<style>
   body{
      background-color:rgb(222, 241, 211);
      font-size: 15px;
}
   
</style>
<template>
    <div >
        <img :src="picture" :width="size" :height="size">
        <p>ชื่อ : {{ firstname }}</p>
        <p>นามสกุล : {{ lastname }}</p>
        <p>ชื่อเล่น : {{ nickname }}</p>
        <p>อายุ : {{ age }}</p>
        <p>ที่อยู่ : <span v-html="address"></span></p>
        <p v-if="hobby.length ===0">ไม่มีงานอดิเรก</p>
        <div v-else>
            <p>งานอดิเรก :</p>
        <ul>
            <li v-for="item in hobby">{{ item }}</li>
        </ul>
        </div>
        <p>ข้อมูลพื้นฐาน :</p>
        <ul>
            <li v-for="(value,key) in general" :key="key">{{ key }} : {{ value }}</li>
        </ul>
        <button @click="showData">คลิกเพื่อดูข้อมูล</button>
    </div>
</template>

<script>
export default{
    data(){
        return{
            firstname:"Yaneesa",
            lastname:"Chaisuwan",
            age: 19,
            address: "<i>Chonburi</i>",
            picture:"https://rms.tatc.ac.th/files/importpicstd/01/66309010007.jpg",
            size:150,
            hobby: [],
            general:{gender:"หญิง",weight:62.5,height:157,status:false},
            nickname : ''
        }
    },
    methods: {
        getFullname(){
            return `$(this.firstname) $(this.lastname)` 
        },
        showData(){
            alert(this.firstname)
        },
        increment(value){
            this.age += value
        },
        decrement(value){
            this.age -= value
        },
        setNickName(event){
            this.nickname=event.target.value
        },
        submitForm(){
            alert('บันทึกข้อมูลเรียบร้อย')
        }
    }
}
</script>
<style>
   body{
      background-color:rgb(222, 241, 211);
      font-size: 15px;
}
   
</style>
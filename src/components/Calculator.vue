<template>
    <div id="calc">
        <section>
            <label for="price">총 금액: </label>
            <input type="number" id="price" v-model="totalPrice">
        </section>

        <section>
            <label for="people">인원 수: </label>
            <input type="number" id="people" v-model="totalPeople">
        </section>

        <button @click="clickBtn">더치페이 하기</button>
        <button @click="plus">0.1 더하기</button>
    </div>
</template>

<script>
export default {
    data() {
        return{
            totalPrice: '',
            totalPeople: '',
            count: 0.1,
        }
    },
    // updated() {
    //     console.log(this.totalPrice);
    //     console.log(this.totalPeople);
    // },
    methods: {
        clickBtn() {
            this.$emit('showResult',this.totalPrice,this.totalPeople);
        },
        plus() {
            this.count += 0.1;
            console.log(this.count.toFixed(1));
        }
    }
}
</script>

<style scoped>
    #calc {
        width: 60vw;
        margin: 0 auto;
        text-align: center;
    }

    section{
        margin-top: 60px;
    }

    label {
        font-size: 32px;
    }

    input {
        font-family: 'LAB디지털';
        font-size: 32px;
        outline: none;
        appearance: none;
        border: none;
        border-radius: 50px;
        background: #a69fdb;
        box-shadow: -20px 20px 60px #8d87ba,
            20px -20px 60px #bfb7fc;
    text-shadow: -1px -1px 0px #666;
        width: 200px;
        height: 50px;
        padding: 0 30px;
        box-sizing: border-box;
        color: #fff;
    }
    button{
        font-family: 'LAB디지털';
        font-size: 24px;
        cursor: pointer;
        color: #fff;
        appearance: none;
        outline: none;
        border: none;
        width: 200px;
        height: 60px;
        margin: 60px 0;
        border-radius: 50px;
        background: #a69fdb;
        box-shadow:  -20px 20px 60px #8d87ba,
             20px -20px 60px #bfb7fc;
                 text-shadow: -1px -1px 0px #666;
    }
    button:active {
        border-radius: 50px;
        background: #a69fdb;
        box-shadow: inset 20px 20px 60px #8d87ba,
            inset -20px -20px 60px #bfb7fc;
    }
</style>
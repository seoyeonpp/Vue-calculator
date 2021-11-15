<template>
    <div id="calc">
        <section>
            <label for="price">총 금액: </label>
            <input type="number" id="price">
        </section>

        <section>
            <label for="people">인원 수: </label>
            <input type="number" id="people">
        </section>

        <button>더치페이 하기</button>
    </div>
</template>

<script>
export default {

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
    }
    button:active {
        border-radius: 50px;
        background: #a69fdb;
        box-shadow: inset 20px 20px 60px #8d87ba,
            inset -20px -20px 60px #bfb7fc;
    }
</style>
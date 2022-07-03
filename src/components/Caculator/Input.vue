<template>
    <div class="input">
        <div class="label">
            {{ label }}
        </div>
        <div class="input-text">
            <div class="inner-input">
                <input type="text" placeholder="" />
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        label: String,
    }
}
</script>

<style lang="scss" scoped>
.label {
    font-weight: 400;
    font-size: 24px;
    color: #FFFFFF;
    padding-bottom: 7px;
}
.input-text {
    border: 4px solid #000000;
    width: 100%;
    .inner-input {
        background: #FBF9F6;
        margin: 4px;
            padding: 24px 0;
    }
}
</style>
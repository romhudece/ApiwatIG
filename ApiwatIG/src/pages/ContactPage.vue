<template>
    <div id="contact-page">
        <h1>ติดต่อเรา</h1>
        <a :href="backLink">
            <button>
                ย้อนกลับ
            </button>
        </a>
    </div>
</template>

<script>
export default {
    name: 'ContactPage',
    data: function (){
        return {
            backLink: '/'
        }
    }
}
</script>

<style>

</style>
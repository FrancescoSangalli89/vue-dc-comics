<template>
    <div class="footer-links">
        <h4>{{title}}</h4>
        <ul>
            <li v-for="(url, index) in urls" :key="index">
                <a :href="url.url">{{url.text}}</a>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "FooterMenu",
    props: {
        title: String,
        urls: Array
    }
}
</script>

<style scoped lang="scss">
    .footer-links {
        margin: 0 1rem;
        h4 {
            color: #fff;
            margin-bottom: 1rem;
        }
        ul {
            list-style: none;
            li {
                margin-bottom: 0.5rem;

                a {
                text-decoration: none;
                color: gray;
                
                }
            }
            
        }
    }
    
</style>
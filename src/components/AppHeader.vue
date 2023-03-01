<script>

export default {
    data() {
        return {
            arrayListItemHeader: [
                'Characters', 
                'Comics', 
                'Movies', 
                'Tv', 
                'Games', 
                'Collectibles', 
                'Videos', 
                'Fans', 
                'News'
            ],
            currentIndex: 0
        }
    }
}

</script>

<template>

    <header>
        <div class="container">
            <div class="row">
                <img class="col" src="/public/img/dc-logo.png" alt="">
                <ul class="col">
                    <li class="a-header"
                    v-for=" listItem in arrayListItemHeader"
                    >
                        {{ listItem }}
                    </li>
                </ul>
            </div>
        </div>
    </header>

</template>

<style lang="scss" scoped>

$blue: #338af9;

.row {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 20px 0;
    width: 100%;

    img {
        width: 80px;
    }
    
    .col{
        display: flex;
        gap: 30px;
        text-transform: uppercase;

        li{
            // padding-bottom: 50px;
            &:hover {
                color: $blue;
                // border-bottom: 5px solid $blue;
            }
        }
    }
}

</style>
<template>
    <div class = "vote-list-container">

        <div class="title">
            Vote
        </div>

        <div class="vote-list">
            <div class = "inside-vote-list">

                <div id="vote-list-nav-bar" class="vote-list-nav-bar">
                    <span class="active" :class="{Active : conditionActive}" @click="voteListaActiveActive">Active</span>
                    <span class="closed" :class="{Closed : !conditionActive}" @click="voteListClosedActive">Closed</span>
                </div>

                <div class="vote-list-content">
                    <div class="tab-active" v-if="conditionActive">
                        <img src="../assets/voinuoc.png">

                        <div class="anounce">
                            <span>No proposal up for vote. Please check other voting instead.</span>
                        </div>
                    </div>

                    <div class="tab-closed" v-else>
                        <a href="#">
                            <div class="vote-for">
                                <div class="vote-for-top">
                                    <span class = "vote-for-your">Vote for Your Favorite Pool</span>
                                    <span class = "ends-at">Ends at: Oct 18 2020 17:00:00</span>
                                </div>

                                <div class="vote-for-bot">
                                    <span class="closed">Closed</span>
                                    <div class="author-total">
                                        <span>Author: </span>
                                        <span class="text333">SUN Team</span>
                                        <span>Total pool supply: </span>
                                        <span class="text333">1,200SUN</span>
                                    </div>                               
                                </div>
                            </div>
                        </a>
                    </div>
                </div>
            </div>
        </div>

    </div>
</template>

<script>
export default {
    el :'#vote-list-nav-bar',
    data() {
        return {
            conditionActive : true
        }
    },
    methods: {
        voteListaActiveActive(){
            this.conditionActive = true;
        },
        voteListClosedActive(){
            this.conditionActive = false;
        }
    },
}
</script>

<style scoped>
    .vote-list-container{
        width: 60%;
        margin: 10px auto 0 auto;
    }

    .title{
        font-size: 1vw;
        color: #fff;
    }

    .vote-list{
        background: rgb(251, 251, 251);
        box-shadow: 0 20px 40px 0 hsla(0,0%,58%,.06);
        border-radius: 10px;
        min-height: 585px;
        padding: 20px;
        margin-top: 20px;
    }

    .inside-vote-list{
        box-sizing: border-box;
        margin: 0;
        padding: 0;
        color: rgba(0,0,0,.65);
        font-size: 14px;
        line-height: 1.5715;
    }


    .vote-list-nav-bar {
        position: relative;
        padding: 15px;
        border-bottom: 1px solid rgb(212, 212, 212) ;
    }

    .vote-list-nav-bar span{
        position: absolute;
        z-index: 1;
        padding-bottom: 7px;
        margin-right : 30px;
    }

    .vote-list-nav-bar .active{
        top: 0;
        left: 0;
    }

    .vote-list-nav-bar .closed{
        top: 0;
        left: 90px;
    }

    .vote-list-content .tab-active{
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 150px 0;
    }

    .active.Active, .closed.Closed{
        color: rgb(96, 93, 255);
        border-bottom: 3px solid rgb(96, 93, 255);
    }

    .tab-closed {
        margin: 40px 15px;
    }

    .tab-closed .vote-for{
        padding: 20px;
        background-color: #fff;
        border-radius: 10px;
    }

    .vote-for-top {
        display: flex;
        justify-content: space-between;
    }
    
    .vote-for-top .vote-for-your {
        font-family: PingFangSC-Medium;
        font-size: 1vw;
        color: #333;
    }

    .vote-for-top .ends-at{
        font-family: PingFangSC-Regular;
        font-size: .6vw;
        color: #999;
        line-height: 17px;
    }

    .vote-for-bot{
        margin-top: 20px;
        display: flex;
        justify-content: space-between;
    }

    .vote-for-bot .closed{
        background: hsla(0,0%,60%,.2);
        color: #999;
        padding: 5px 15px;
        border-radius: 10px;
    }

    .vote-for-bot .author-total{
        font-family: PingFangSC-Regular;
        font-size: .6vw;
        color: #999;
        line-height: 17px;
    }

    .text333 {
        color: #333;
    }
</style>
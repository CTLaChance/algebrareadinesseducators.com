<script>
    import ReturnArrow from './ReturnArrow.svelte';
</script>

<style lang="scss">
    #about {
        display: flex;
        justify-content: left;
        align-items: center;
        height: fit-content;

        animation: component-load 1s .25s cubic-bezier(.61,.02,.24,.98) both;

        #about-content {
            width: 70%;
            margin: auto auto auto 0;

            display: flex;

            #about-left {
                width: 50%;
                display: flex;
                justify-content: space-around;
                align-items: center;

                #left-portrait, #right-portrait{
                    width: 45%;

                    img {
                        width: 100%;
                    }
                }
            }

            #about-right {
                width: 50%;
                border-left: 1px solid #bbbbbb;
                padding-left: 15px;

                h1 {
                    margin-top: 0;
                }
    
                h3 {
                    font-weight: 400;
                }
            }

            @media screen and (orientation: portrait) {
                margin: auto;
                flex-direction: column;

                #about-left {
                    width: 100%;
                    margin-top: 16px;
                }

                #about-right {
                    width: 100%;
                    padding: 0;
                    border: none;
                    
                    h1 {
                        text-align: center;
                        margin: 16px 0px;
                    }

                    h3 {
                        margin: 16px 0px;
                    }
                }
            }
        }
    }
</style>

<div id="about">
    <ReturnArrow />
    <div id="about-content">
        <div id="about-left">
            <div id="left-portrait"><img src="./kathy.jpg" alt="Katherine LaChance Portrait"></div>
            <div id="right-portrait"><img src="./rhonda.jpg" alt="Rhonda Brady Portrait"></div>
        </div>
        <div id="about-right">
            <h1>ABOUT US</h1>
            <h3>After spending several years searching for a resource that spirals necessary skills for success in math, we decided to write our own. Our students’ scores on the state mandated test improved dramatically after the implementation of our builders. Enjoy the same success by implementing builders as your daily homework assignments.<br><br>Our books are designed to recycle skills necessary for algebra readiness. When used effectively, students practice skills until they become automatic, allowing for deeper understanding of future mathematical concepts.</h3>
        </div>
    </div>
</div>
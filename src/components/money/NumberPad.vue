<template>
    <div class="number-pad">
        <div class="output">100</div>
        <div class="buttons">
            <div class="button">
                <button>1</button>
            </div>
            <div class="button">
                <button>2</button>
            </div>
            <div class="button">
                <button>3</button>
            </div>
            <div class="button">
                <button>Del</button>
            </div>
            <div class="button">
                <button>4</button>
            </div>
            <div class="button">
                <button>5</button>
            </div>
            <div class="button">
                <button>6</button>
            </div>
            <div class="button">
                <button>AC</button>
            </div>
            <div class="button">
                <button>6</button>
            </div>
            <div class="button">
                <button>7</button>
            </div>
            <div class="button">
                <button>8</button>
            </div>
            <div class="button ok">
                <button>OK</button>
            </div>
            <div class="button zero">
                <button>0</button>
            </div>
            <div class="button">
                <button>.</button>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
    export default {
        name: 'NumberPad'
    };
</script>

<style lang="less" scoped>
    @import "~@/assets/styles/global.less";

    .number-pad {
        margin-bottom: 8px;

        .output {
            font-size: 36px;
            font-family: Consolas, monospace;
            padding: 9px 16px;
            text-align: right;
        }

        .buttons:extend(.clearFix) {
            .button {
                @btn-height: 64px;
                float: left;
                width: 25%;
                height: @btn-height + 8px;
                display: flex;
                justify-content: center;
                padding: 4px;
                align-items: center;

                &.ok {
                    height: (@btn-height + 8px)*2;
                    float: right;

                    > button {
                        height: 95%;
                    }
                }

                &.zero {
                    width: 25%*2;

                    > button {
                        width: 90%;
                    }
                }

                > button {
                    width: @btn-height;
                    height: @btn-height;
                    border: none;
                    font-size: 24px;
                    font-family: Helvetica;
                    font-weight: normal;
                    border-radius: @btn-height / 2;
                    color: #999;
                    background: linear-gradient(135deg, rgb(236, 236, 236, 0.5) 0%, rgba(250, 250, 250, 1) 100%);
                    box-shadow: -4px -4px 10px -8px rgba(255, 255, 255, 1), 4px 4px 10px -8px rgba(0, 0, 0, .3);
                }

                > button:active {
                    box-shadow: -4px -4px 10px -8px rgba(255, 255, 255, 1) inset, 4px 4px 10px -8px rgba(0, 0, 0, .3) inset;
                }
            }
        }
    }
</style>
<template>
    <div class="yuansu">
        <h1>元素周期表</h1>
        <h2>现代的化学元素周期律（Periodic table）是19世纪俄国人门捷列夫发现的。他将当时已知的63种元素以表的形式排列，把有相似化学性质的元素放在同一直行，这就是元素周期表的雏形。这个表经过多年修订后才成为当代的周期表。在周期表中，元素是以元素的原子序数排列，最小的排行最先。表中一横行称为一个周期，一列称为一个族。</h2>
        <div class="beizhu">
            <div v-for="(item, index) in bzarr" :key="index" :style="{background: item.background}" class="bzitem">
                {{item.name}}
            </div>
        </div>
        <div class="yuansubox">
            <div class="ysitem">
                <div class="item" style="border:none !important;background:none !important;color:#000 !important;">周期</div>
                <div v-for="(item, index) in crr" :key="index" class="item" style="border:none !important;background:none !important;color:#000 !important;">
                    {{item}}
                </div>
            </div>
            <div v-for="(item, index) in arr" :key="index" class="ysitem">
                <div v-for="(obj, num) in item" :key="num" class="item" :style="num == 0 ? 'border:none !important;background:none !important;color:#000 !important;' : {background: obj.background}" >
                    <p class="itemtop"><span class="elrd">{{obj.id}}</span><span class="elff">{{obj.symbol}}</span></p>
                    <p class="itembottom">{{obj.name}}</p>
                </div>
            </div>
        </div>
        <div class="yuansubottom">
            <div v-for="(item, index) in brr" :key="index" class="ysbottom">
                <div v-for="(obj, num) in item" :key="num" class="item" :style="{background: obj.background}">
                    <p class="itemtop"><span class="elrd">{{obj.id}}</span><span class="elff">{{obj.symbol}}</span></p>
                    <p class="itembottom">{{obj.name}}</p>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'Yuansu',
    data () {
        return {
            arr: [
                [
                    {
                        'name': 'IA'
                    },
                    {
                        'id': 1, // 原子序数
                        'name': '氢', // 元素名称
                        'symbol': 'H', // 元素符号
                        'background': '#00F700', // 背景色
                    },
                    {
                        'id': 3, // 原子序数
                        'name': '锂', // 元素名称
                        'symbol': 'Li', // 元素符号
                        'background': '#FFAA00', // 背景色
                    },
                    {
                        'id': 11, // 原子序数
                        'name': '钠', // 元素名称
                        'symbol': 'Na', // 元素符号
                        'background': '#FFAA00', // 背景色
                    },
                    {
                        'id': 19, // 原子序数
                        'name': '钾', // 元素名称
                        'symbol': 'K', // 元素符号
                        'background': '#FFAA00', // 背景色
                    },
                    {
                        'id': 37, // 原子序数
                        'name': '铷', // 元素名称
                        'symbol': 'Rb', // 元素符号
                        'background': '#FFAA00', // 背景色
                    },
                    {
                        'id': 55, // 原子序数
                        'name': '铯', // 元素名称
                        'symbol': 'Cs', // 元素符号
                        'background': '#FFAA00', // 背景色
                    },
                    {
                        'id': 87, // 原子序数
                        'name': '钫', // 元素名称
                        'symbol': 'Fr', // 元素符号
                        'background': '#FFAA00', // 背景色
                    }
                ],
                [
                    {
                        'name': 'IIA'
                    },
                    {
                        'id': 4, // 原子序数
                        'name': '铍', // 元素名称
                        'symbol': 'Be', // 元素符号
                        'background': '#F7F700', // 背景色
                    },
                    {
                        'id': 12, // 原子序数
                        'name': '镁', // 元素名称
                        'symbol': 'Mg', // 元素符号
                        'background': '#F7F700', // 背景色
                    },
                    {
                        'id': 20, // 原子序数
                        'name': '钙', // 元素名称
                        'symbol': 'Ga', // 元素符号
                        'background': '#F7F700', // 背景色
                    },
                    {
                        'id': 38, // 原子序数
                        'name': '锶', // 元素名称
                        'symbol': 'Sr', // 元素符号
                        'background': '#F7F700', // 背景色
                    },
                    {
                        'id': 56, // 原子序数
                        'name': '钡', // 元素名称
                        'symbol': 'Ba', // 元素符号
                        'background': '#F7F700', // 背景色
                    },
                    {
                        'id': 88, // 原子序数
                        'name': '镭', // 元素名称
                        'symbol': 'Ra', // 元素符号
                        'background': '#F7F700', // 背景色
                    },
                ],
                [
                    {
                        'name': 'IIIB'
                    },
                    {
                        'id': 21, // 原子序数
                        'name': '钪', // 元素名称
                        'symbol': 'Sc', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 39, // 原子序数
                        'name': '钇', // 元素名称
                        'symbol': 'Y', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 51, // 原子序数
                        'name': '镧系', // 元素名称
                        'symbol': '-71', // 元素符号
                        'background': '#FFAA88', // 背景色
                    },
                    {
                        'id': 89, // 原子序数
                        'name': '锕系', // 元素名称
                        'symbol': '-103', // 元素符号
                        'background': '#DDAACC', // 背景色
                    },
                ],
                [
                    {
                        'name': 'IVB'
                    },
                    {
                        'id': 22, // 原子序数
                        'name': '钛', // 元素名称
                        'symbol': 'Ti', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 40, // 原子序数
                        'name': '锆', // 元素名称
                        'symbol': 'Zr', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 72, // 原子序数
                        'name': '铪', // 元素名称
                        'symbol': 'Hf', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 104, // 原子序数
                        'name': '鑪', // 元素名称
                        'symbol': 'Rf', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                ],
                [
                    {
                        'name': 'VB'
                    },
                    {
                        'id': 23, // 原子序数
                        'name': '钒', // 元素名称
                        'symbol': 'V', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 41, // 原子序数
                        'name': '铌', // 元素名称
                        'symbol': 'Nb', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 73, // 原子序数
                        'name': '钽', // 元素名称
                        'symbol': 'Ta', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 105, // 原子序数
                        'name': '𨧀', // 元素名称
                        'symbol': 'Db', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                ],
                [
                    {
                        'name': 'VIB'
                    },
                    {
                        'id': 24, // 原子序数
                        'name': '铬', // 元素名称
                        'symbol': 'Cr', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 42, // 原子序数
                        'name': '钼', // 元素名称
                        'symbol': 'Mo', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 74, // 原子序数
                        'name': '钨', // 元素名称
                        'symbol': 'W', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 106, // 原子序数
                        'name': '𨭎', // 元素名称
                        'symbol': 'Sg', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                ],
                [
                    {
                        'name': 'VIIB'
                    },
                    {
                        'id': 25, // 原子序数
                        'name': '锰', // 元素名称
                        'symbol': 'Mn', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 43, // 原子序数
                        'name': '锝', // 元素名称
                        'symbol': 'Tc', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 75, // 原子序数
                        'name': '铼', // 元素名称
                        'symbol': 'Re', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 107, // 原子序数
                        'name': '𨨏', // 元素名称
                        'symbol': 'Bh', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                ],
                [
                    {
                        'name': 'VIII'
                    },
                    {
                        'id': 26, // 原子序数
                        'name': '铁', // 元素名称
                        'symbol': 'Fe', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 44, // 原子序数
                        'name': '钌', // 元素名称
                        'symbol': 'Ru', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 76, // 原子序数
                        'name': '锇', // 元素名称
                        'symbol': 'Os', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 108, // 原子序数
                        'name': '𨭆', // 元素名称
                        'symbol': 'Hs', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                ],
                [
                    {
                        'name': 'VIII'
                    },
                    {
                        'id': 27, // 原子序数
                        'name': '钴', // 元素名称
                        'symbol': 'Co', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 45, // 原子序数
                        'name': '铑', // 元素名称
                        'symbol': 'Rh', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 77, // 原子序数
                        'name': '铱', // 元素名称
                        'symbol': 'Ir', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 109, // 原子序数
                        'name': '䥑', // 元素名称
                        'symbol': 'Mt', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                ],
                [
                    {
                        'name': 'VIII'
                    },
                    {
                        'id': 28, // 原子序数
                        'name': '镍', // 元素名称
                        'symbol': 'Ni', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 46, // 原子序数
                        'name': '钯', // 元素名称
                        'symbol': 'Pd', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 78, // 原子序数
                        'name': '铂', // 元素名称
                        'symbol': 'Pt', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 110, // 原子序数
                        'name': '鐽', // 元素名称
                        'symbol': 'Ds', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                ],
                [
                    {
                        'name': 'IB'
                    },
                    {
                        'id': 29, // 原子序数
                        'name': '铜', // 元素名称
                        'symbol': 'Cu', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 47, // 原子序数
                        'name': '银', // 元素名称
                        'symbol': 'Ag', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 79, // 原子序数
                        'name': '金', // 元素名称
                        'symbol': 'Au', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 111, // 原子序数
                        'name': '錀', // 元素名称
                        'symbol': 'Rg', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                ],
                [
                    {
                        'name': 'IIB'
                    },
                    {
                        'id': 30, // 原子序数
                        'name': '锌', // 元素名称
                        'symbol': 'Zn', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 48, // 原子序数
                        'name': '镉', // 元素名称
                        'symbol': 'Cd', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 80, // 原子序数
                        'name': '汞', // 元素名称
                        'symbol': 'Hg', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 112, // 原子序数
                        'name': 'Uub', // 元素名称
                        'symbol': 'Cn', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                ],
                [
                    {
                        'name': 'IIIA'
                    },
                    {
                        'id': 5, // 原子序数
                        'name': '硼', // 元素名称
                        'symbol': 'B', // 元素符号
                        'background': 'rgb(204, 204, 153)', // 背景色
                    },
                    {
                        'id': 13, // 原子序数
                        'name': '铝', // 元素名称
                        'symbol': 'Al', // 元素符号
                        'background': '#00CCCC', // 背景色
                    },
                    {
                        'id': 31, // 原子序数
                        'name': '镓', // 元素名称
                        'symbol': 'Ga', // 元素符号
                        'background': '#00CCCC', // 背景色
                    },
                    {
                        'id': 49, // 原子序数
                        'name': '铟', // 元素名称
                        'symbol': 'In', // 元素符号
                        'background': '#00CCCC', // 背景色
                    },
                    {
                        'id': 81, // 原子序数
                        'name': '铊', // 元素名称
                        'symbol': 'Tl', // 元素符号
                        'background': '#00CCCC', // 背景色
                    },
                    {
                        'id': 113, // 原子序数
                        'name': 'Uut', // 元素名称
                        'symbol': '', // 元素符号
                        'background': '#00CCCC', // 背景色
                    },
                ],
                [
                    {
                        'name': 'IVA'
                    },
                    {
                        'id': 6, // 原子序数
                        'name': '碳', // 元素名称
                        'symbol': 'C', // 元素符号
                        'background': '#00F700', // 背景色
                    },
                    {
                        'id': 14, // 原子序数
                        'name': '硅', // 元素名称
                        'symbol': 'Si', // 元素符号
                        'background': 'rgb(204, 204, 153)', // 背景色
                    },
                    {
                        'id': 32, // 原子序数
                        'name': '锗', // 元素名称
                        'symbol': 'Ge', // 元素符号
                        'background': 'rgb(204, 204, 153)', // 背景色
                    },
                    {
                        'id': 50, // 原子序数
                        'name': '锡', // 元素名称
                        'symbol': 'Sn', // 元素符号
                        'background': '#00CCCC', // 背景色
                    },
                    {
                        'id': 82, // 原子序数
                        'name': '铅', // 元素名称
                        'symbol': 'Pb', // 元素符号
                        'background': '#00CCCC', // 背景色
                    },
                    {
                        'id': 114, // 原子序数
                        'name': 'Uuq', // 元素名称
                        'symbol': '', // 元素符号
                        'background': '#00CCCC', // 背景色
                    },
                ],
                [
                    {
                        'name': 'VA'
                    },
                    {
                        'id': 7, // 原子序数
                        'name': '氮', // 元素名称
                        'symbol': 'N', // 元素符号
                        'background': '#00F700', // 背景色
                    },
                    {
                        'id': 15, // 原子序数
                        'name': '磷', // 元素名称
                        'symbol': 'P', // 元素符号
                        'background': '#00F700', // 背景色
                    },
                    {
                        'id': 33, // 原子序数
                        'name': '砷', // 元素名称
                        'symbol': 'As', // 元素符号
                        'background': 'rgb(204, 204, 153)', // 背景色
                    },
                    {
                        'id': 51, // 原子序数
                        'name': '锑', // 元素名称
                        'symbol': 'Sb', // 元素符号
                        'background': 'rgb(204, 204, 153)', // 背景色
                    },
                    {
                        'id': 83, // 原子序数
                        'name': '铋', // 元素名称
                        'symbol': 'Bi', // 元素符号
                        'background': '#00CCCC', // 背景色
                    },
                    {
                        'id': 115, // 原子序数
                        'name': 'Uup', // 元素名称
                        'symbol': '', // 元素符号
                        'background': '#00CCCC', // 背景色
                    },
                ],
                [
                    {
                        'name': 'VIA'
                    },
                    {
                        'id': 8, // 原子序数
                        'name': '氧', // 元素名称
                        'symbol': 'O', // 元素符号
                        'background': '#00F700', // 背景色
                    },
                    {
                        'id': 16, // 原子序数
                        'name': '硫', // 元素名称
                        'symbol': 'S', // 元素符号
                        'background': '#00F700', // 背景色
                    },
                    {
                        'id': 34, // 原子序数
                        'name': '硒', // 元素名称
                        'symbol': 'Se', // 元素符号
                        'background': '#00F700', // 背景色
                    },
                    {
                        'id': 52, // 原子序数
                        'name': '碲', // 元素名称
                        'symbol': 'Te', // 元素符号
                        'background': 'rgb(204, 204, 153)', // 背景色
                    },
                    {
                        'id': 84, // 原子序数
                        'name': '钋', // 元素名称
                        'symbol': 'Po', // 元素符号
                        'background': 'rgb(204, 204, 153)', // 背景色
                    },
                    {
                        'id': 116, // 原子序数
                        'name': 'Uuh', // 元素名称
                        'symbol': '', // 元素符号
                        'background': '#00CCCC', // 背景色
                    },
                ],
                [
                    {
                        'name': 'VIIA'
                    },
                    {
                        'id': 9, // 原子序数
                        'name': '氟', // 元素名称
                        'symbol': 'F', // 元素符号
                        'background': 'rgb(240, 230, 140)', // 背景色
                    },
                    {
                        'id': 17, // 原子序数
                        'name': '氯', // 元素名称
                        'symbol': 'Cl', // 元素符号
                        'background': 'rgb(240, 230, 140)', // 背景色
                    },
                    {
                        'id': 35, // 原子序数
                        'name': '溴', // 元素名称
                        'symbol': 'Br', // 元素符号
                        'background': 'rgb(240, 230, 140)', // 背景色
                    },
                    {
                        'id': 53, // 原子序数
                        'name': '碘', // 元素名称
                        'symbol': 'I', // 元素符号
                        'background': 'rgb(240, 230, 140)', // 背景色
                    },
                    {
                        'id': 85, // 原子序数
                        'name': '砹', // 元素名称
                        'symbol': 'At', // 元素符号
                        'background': 'rgb(240, 230, 140)', // 背景色
                    },
                    {
                        'id': 117, // 原子序数
                        'name': 'Uus', // 元素名称
                        'symbol': '', // 元素符号
                        'background': '#fff', // 背景色
                    },
                ],
                [
                    {
                        'name': '0'
                    },
                    {
                        'id': 2, // 原子序数
                        'name': '氦', // 元素名称
                        'symbol': 'He', // 元素符号
                        'background': 'rgb(240, 248, 255)', // 背景色
                    },
                    {
                        'id': 10, // 原子序数
                        'name': '氖', // 元素名称
                        'symbol': 'Ne', // 元素符号
                        'background': 'rgb(240, 248, 255)', // 背景色
                    },
                    {
                        'id': 18, // 原子序数
                        'name': '氩', // 元素名称
                        'symbol': 'Ar', // 元素符号
                        'background': 'rgb(240, 248, 255)', // 背景色
                    },
                    {
                        'id': 36, // 原子序数
                        'name': '氪', // 元素名称
                        'symbol': 'Kr', // 元素符号
                        'background': 'rgb(240, 248, 255)', // 背景色
                    },
                    {
                        'id': 54, // 原子序数
                        'name': '氙', // 元素名称
                        'symbol': 'Xe', // 元素符号
                        'background': 'rgb(240, 248, 255)', // 背景色
                    },
                    {
                        'id': 86, // 原子序数
                        'name': '氡', // 元素名称
                        'symbol': 'Rn', // 元素符号
                        'background': 'rgb(240, 248, 255)', // 背景色
                    },
                    {
                        'id': 118, // 原子序数
                        'name': 'Uuo', // 元素名称
                        'symbol': '', // 元素符号
                        'background': '#fff', // 背景色
                    },
                ]
            ],
            brr: [
                [
                    {
                        'name': '镧系', // 元素名称
                        'background': '#FFAA88', // 背景色
                    },
                    {
                        'id': 57, // 原子序数
                        'name': '镧', // 元素名称
                        'symbol': 'La', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 58, // 原子序数
                        'name': '铈', // 元素名称
                        'symbol': 'Ce', // 元素符号
                        'background': '#FFAA88', // 背景色
                    },
                    {
                        'id': 59, // 原子序数
                        'name': '镨', // 元素名称
                        'symbol': 'Pr', // 元素符号
                        'background': '#FFAA88', // 背景色
                    },
                    {
                        'id': 60, // 原子序数
                        'name': '钕', // 元素名称
                        'symbol': 'Nd', // 元素符号
                        'background': '#FFAA88', // 背景色
                    },
                    {
                        'id': 61, // 原子序数
                        'name': '钷', // 元素名称
                        'symbol': 'Pm', // 元素符号
                        'background': '#FFAA88', // 背景色
                    },
                    {
                        'id': 62, // 原子序数
                        'name': '钐', // 元素名称
                        'symbol': 'Sm', // 元素符号
                        'background': '#FFAA88', // 背景色
                    },
                    {
                        'id': 63, // 原子序数
                        'name': '铕', // 元素名称
                        'symbol': 'Eu', // 元素符号
                        'background': '#FFAA88', // 背景色
                    },
                    {
                        'id': 64, // 原子序数
                        'name': '钆', // 元素名称
                        'symbol': 'Gd', // 元素符号
                        'background': '#FFAA88', // 背景色
                    },
                    {
                        'id': 65, // 原子序数
                        'name': '铽', // 元素名称
                        'symbol': 'Tb', // 元素符号
                        'background': '#FFAA88', // 背景色
                    },
                    {
                        'id': 66, // 原子序数
                        'name': '镝', // 元素名称
                        'symbol': 'Dy', // 元素符号
                        'background': '#FFAA88', // 背景色
                    },
                    {
                        'id': 67, // 原子序数
                        'name': '钬', // 元素名称
                        'symbol': 'Ho', // 元素符号
                        'background': '#FFAA88', // 背景色
                    },
                    {
                        'id': 68, // 原子序数
                        'name': '铒', // 元素名称
                        'symbol': 'Er', // 元素符号
                        'background': '#FFAA88', // 背景色
                    },
                    {
                        'id': 69, // 原子序数
                        'name': '铥', // 元素名称
                        'symbol': 'Tm', // 元素符号
                        'background': '#FFAA88', // 背景色
                    },
                    {
                        'id': 70, // 原子序数
                        'name': '镱', // 元素名称
                        'symbol': 'Yb', // 元素符号
                        'background': '#FFAA88', // 背景色
                    },
                    {
                        'id': 71, // 原子序数
                        'name': '镥', // 元素名称
                        'symbol': 'Lu', // 元素符号
                        'background': '#FFAA88', // 背景色
                    },
                ],
                [
                    {
                        'name': '锕系', // 元素名称
                        'background': '#DDAACC', // 背景色
                    },
                    {
                        'id': 89, // 原子序数
                        'name': '锕', // 元素名称
                        'symbol': 'Ac', // 元素符号
                        'background': '#FF7799', // 背景色
                    },
                    {
                        'id': 90, // 原子序数
                        'name': '钍', // 元素名称
                        'symbol': 'Th', // 元素符号
                        'background': '#DDAACC', // 背景色
                    },
                    {
                        'id': 91, // 原子序数
                        'name': '镤', // 元素名称
                        'symbol': 'Pa', // 元素符号
                        'background': '#DDAACC', // 背景色
                    },
                    {
                        'id': 92, // 原子序数
                        'name': '铀', // 元素名称
                        'symbol': 'U', // 元素符号
                        'background': '#DDAACC', // 背景色
                    },
                    {
                        'id': 93, // 原子序数
                        'name': '镎', // 元素名称
                        'symbol': 'Np', // 元素符号
                        'background': '#DDAACC', // 背景色
                    },
                    {
                        'id': 94, // 原子序数
                        'name': '钚', // 元素名称
                        'symbol': 'Pu', // 元素符号
                        'background': '#DDAACC', // 背景色
                    },
                    {
                        'id': 95, // 原子序数
                        'name': '镅', // 元素名称
                        'symbol': 'Am', // 元素符号
                        'background': '#DDAACC', // 背景色
                    },
                    {
                        'id': 96, // 原子序数
                        'name': '锔', // 元素名称
                        'symbol': 'Cm', // 元素符号
                        'background': '#DDAACC', // 背景色
                    },
                    {
                        'id': 97, // 原子序数
                        'name': '锫', // 元素名称
                        'symbol': 'Bk', // 元素符号
                        'background': '#DDAACC', // 背景色
                    },
                    {
                        'id': 98, // 原子序数
                        'name': '锎', // 元素名称
                        'symbol': 'Cf', // 元素符号
                        'background': '#DDAACC', // 背景色
                    },
                    {
                        'id': 99, // 原子序数
                        'name': '锿', // 元素名称
                        'symbol': 'Es', // 元素符号
                        'background': '#DDAACC', // 背景色
                    },
                    {
                        'id': 100, // 原子序数
                        'name': '镄', // 元素名称
                        'symbol': 'Fm', // 元素符号
                        'background': '#DDAACC', // 背景色
                    },
                    {
                        'id': 101, // 原子序数
                        'name': '钔', // 元素名称
                        'symbol': 'Md', // 元素符号
                        'background': '#DDAACC', // 背景色
                    },
                    {
                        'id': 102, // 原子序数
                        'name': '锘', // 元素名称
                        'symbol': 'No', // 元素符号
                        'background': '#DDAACC', // 背景色
                    },
                    {
                        'id': 103, // 原子序数
                        'name': '铹', // 元素名称
                        'symbol': 'Lr', // 元素符号
                        'background': '#DDAACC', // 背景色
                    },
                ]
            ],
            crr: [1,2,3,4,5,6,7], // 周期
            bzarr: [
                {
                    id: 1,
                    name: '碱金属',
                    background: "#FFAA00"
                },
                {
                    id: 2,
                    name: '碱土金属',
                    background: '#F7F700'
                },
                {
                    id: 3,
                    name: '镧系元素',
                    background: '#FFAA88'
                },
                {
                    id: 4,
                    name: '锕系元素',
                    background: '#DDAACC'
                },
                {
                    id: 5,
                    name: '过渡金属',
                    background: '#FF7799'
                },
                {
                    id: 6,
                    name: '主族金属',
                    background: '#00CCCC'
                },
                {
                    id: 7,
                    name: '类金属',
                    background: 'rgb(204, 204, 153)'
                },
                {
                    id: 8,
                    name: '非金属',
                    background: '#00F700'
                },
                {
                    id: 9,
                    name: '卤素',
                    background: 'rgb(240, 230, 140)'
                },
                {
                    id: 10,
                    name: '惰性气体',
                    background: 'rgb(240, 248, 255)'
                },
                {
                    id: 11,
                    name: '未发现',
                    background: '#fff'
                },
            ], // 备注
        }
    }
}
</script>
<style scoped>
.yuansu{
    width: 874px;
    margin: 0 auto;
}
h1{
    font-size: 20px;
}
h2{
    font-size: 16px;
    text-align: left;
    text-indent: 32px;
    margin: 0 20px;
    line-height: 24px;
}
.yuansubox{
    height: 368px;
    display: flex;
    align-items: flex-end;
    justify-content: center;
}
.ysitem{
        width: 46px;
    }
.yuansubottom{
    margin-top: 20px;
}
.ysbottom{
    display: flex;
    justify-content: center;
    width: 736px;
    margin: 0 auto;
}
.item{
    width: 46px;
    height: 46px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    font-size: 12px;
    color: Black;
    text-decoration: none;
    border: 1px solid Silver;
    cursor: pointer;
    background: #FFAA00;
    
}
.itemtop{
    margin: 0 15%;
    width: 70%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    text-align: center;
    
}
.elrd{
    color: #990000;
}
.elff{
    color: #0000CC;
}
.itembottom{
    margin: 0;
    text-align: center;
}
.item:hover{
    text-decoration: none;
    color: red;
    border: 1px solid #A54108;
    background: #FFFFE7 !important;
    animation: elementhover 1s forwards;
}
.beizhu{
    display: flex;
    justify-content: center;
}
.bzitem{
    padding: 2px 12px;
    font-size: 14px;
}
@keyframes elementhover {
    0% {
        transform: rotate(0deg) scale(1);
    }
    50% {
        transform: rotate(180deg) scale(4);
    }
    100% {
        transform: rotate(360deg) scale(2);
    }
}
</style>

<template>
    <div>
        <canvas id="myChart"></canvas>
    </div>
</template>

<script setup>
import Chart from 'chart.js/auto';

const labels=[
    'january',
    'february',
    'march',
    'april',
    'may',
    'june',
];




const data= {
    labels : labels,
    datasets: [{
        label: 'Pengunjung',
        backgroundColor: 'rgb(222,39,225 )',
        backgroundColor: [
        'rgb(222 ,39, 225)',
        'rgb(144, 142, 248)',
        'rgb(254, 245, 42)',
        'rgb(13, 255, 66)',
        'rgb(12, 121, 183)',
        'rgb(232, 9, 9)',
        ],
        borderColor: 'rgb(144, 142, 248)',
        data: [8, 10, 15, 20, 15, 10, 45],
    }]
};

const config = {
    type: 'bar',
    data: data,
    options: {}
};

onMounted(()=>{
    const myChart = new Chart(
    document.getElementById('myChart'),
    config
);
})
</script>
<script>
let top1 = someStore()
let top2 = someStore()
let topLevelGet = $top1
topLevelGet = $top2

function test(top1) {
    let passedGet = $top1
}

function test2($top1) {
    let paramShadowed = $top1
}

function test3() {
    let $top2 = "hi"
    let letshadowed = $top2
}

const test4 = ({a,  b: { $top1: $top2 }}) => $top2 && $top1

</script>


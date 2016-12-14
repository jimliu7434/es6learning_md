# 陣列

## array.from
* 將類似陣列的資料群轉為陣列
* 只要有 length 屬性均可轉換

## 擴展符號 ...
* 將陣列所有內容取出為 arg1, arg2, arg3 ..... 型態
* 可替代 apply 方法
* 可直接合併陣列 (取代 concat )

        // ES5
        [1, 2].concat(more)
        // ES6
        [1, 2, ...more]
        
* 亦可將類似陣列的資料群轉為陣列「內容」 (再用[]包起即為新陣列)

        // NodeList 對象
        [...document.querySelectorAll('div')];

## include()
        [1, 2, 3].includes(2);     // true
        [1, 2, 3].includes(4);     // false
        [1, 2, NaN].includes(NaN); // true

## of()
        Array.of(3, 11, 8) // [3,11,8]
        Array.of(3) // [3]
        Array.of(3).length // 1

## find() & findIndex()
        [1, 4, -5, 10].find(function(value, index, arr){
                return value < 0;
        });
        // equals to
        [1, 4, -5, 10].find((n) => n < 0)  // -5 
        
        //findIndex
        [1, 4, -5, 10].findIndex((n) => n < 0)  // 2
        [1, 4, -5, 10].findIndex((n) => n < -5)  // -1


## entries(), keys(), values() 
        for (let index of ['a', 'b'].keys()) {
                console.log(index);
        }
        // 0
        // 1

        for (let elem of ['a', 'b'].values()) {
                console.log(elem);
        }
        // 'a'
        // 'b'

        for (let [index, elem] of ['a', 'b'].entries()) {
                console.log(index, elem);
        }
        // 0 "a"
        // 1 "b"


## 空位
* array 中元素「無值」時的狀態(非 undefined )
* 因各環境處理空位原則不同，儘量勿產生空位狀況
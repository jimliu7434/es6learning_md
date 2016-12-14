# 變數

## 宣告詞綴
* var
* function
* let
* const
* import
* class

## var 
* 頂層宣告(全域)

## let 
* 區塊宣告


## const
* 需直接賦值
* 賦值為 Object 時，僅鎖定 Object 位址，Property 可被修改
* 需鎖定 Object Property 請使用 Object.freeze(obj)


## ES5 global 對象不一問題
* Browser : **window**
* Node.js : **global**
* WebWorker : **self頂層**  


## 解構賦值
        // for example
        let a = 1,
            b = 2,
            c = 3;  
        // equals to
        let [a, b, c] = [1, 2, 3];
        // if 
        let [a, b, c] = [1, 2];  // c = undefined

## 預設值
        [x, y = 'b'] = ['a'];  // x = 'a', y = 'b'
        [x, y = 'b'] = ['a', undefined]; // x='a', y='b'
        let {length : len} = 'hello';  // len = 5
        


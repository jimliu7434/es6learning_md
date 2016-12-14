# 函數

## 預設值
* 用法
        
        function log(x, y = 'World') { }
* 應用方式

        function throwIfMissing() {
            throw new Error('Missing parameter');
        }

        function foo(mustBeProvided = throwIfMissing()) {
            return mustBeProvided;
        }

        foo();  // Error: Missing parameter
* 使用 預設值 時，無法在 function 內 **'use strict'**，但可以全域使用 **'use strict'**

## rest parameters
* 將任意數量參數組合成 array 型態
* 可取代 ES5 的 arguments 寫法
* rest parameters 必須是函數的最後一個參數

        // arguments 寫法
        function sortNumbers() {
            return Array.prototype.slice.call(arguments).sort();
        }
        // rest parameter
        function sortNumbers ( ...numbers ) {
            numbers.sort();
        } 

## arrow function
* between ES5
         
        var f = function() { return 5; };
        // equals to
        var f = () => 5;

* return a **Value**

        var f = (num1, num2) => num1 + num2;

* return a **function**

        var f = (num1, num2) => { return num1 + num2; }

* return a **object** -> add "( )" to keep difference between returning function

        var f = (id, name) => ({ id: id, name: name });  

* **this** object 指向定義 arrow function 時的 object，而非實際叫用時的 object
* 不可當 constructor ， 不可以 new 
* 無 arguments, super
* 不可使用 yield 
        


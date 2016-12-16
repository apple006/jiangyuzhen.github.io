### 递归
---
tab    function fn(){
tab      const args = Array.from(arguments)
tab      console.log(args)
tab      const last = args[args.length - 1]
tab      if(typeof last !== 'function'){
tab       return fn.bind(null, args.join(','))
tab      } else { 
tab       last.call(console, args[0])
tab      }
tab    }

### 递归
***
`function fn(){
  const args = Array.from(arguments)
  console.log(args)
  const last = args[args.length - 1]
  if(typeof last !== 'function'){
   return fn.bind(null, args.join(','))
  } else { 
   last.call(console, args[0])
  }
}` 

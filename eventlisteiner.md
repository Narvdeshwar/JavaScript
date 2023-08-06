# EventTarget  
The EventTarget interface is implemented by objects that can receive events and may have listeners for them. 
# There are 3 EventTarget 
1. addEventListener()
2. removeEventListener() - works only when 1.same target 2. same type 3.same function
# Phases of event
1. capturing phase
2. at target phase
3. bubbling phase
# preventDefault()
It prevent the default action of any event.
``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EventTarget</title>
</head>
<body>
    <a href="https://www.facebook.com">facebook</a>
    <a href="https://www.facebook.com">facebook</a>
    <a href="https://www.facebook.com">facebook</a>
    <script>
        const a=document.querySelectorAll('a');
        const link=a[2];
        link.addEventListener('click',(e)=>{
            e.preventDefault();
            console.log('3rd link will not work');
        })

    </script>
</body>
</html>
```
``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EventTarget</title>
</head>
<body>
    <script>
        let myDiv=document.createElement('div')
        const myFunc=(e)=>{
            console.log(e.target.textContent);
        }
        myDiv.addEventListener('click',myFunc)
        for(let i=1;i<=50;i++){
            let para=document.createElement('p')
            para.textContent='this is para'+i
            myDiv.appendChild(para)
        }
        document.body.append(myDiv)
    </script>
</body>
</html>
```

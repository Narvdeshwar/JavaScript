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
# adding event listner programatically
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
# targetting particular html element eg for span element
``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EventTarget</title>
</head>
<body>
    <div id="wrapper">
        <p>hello <span>xyxspan</span></p>
        <p>hello1 <span>yvkdj</span></p>
        <p>hello2 <span>kdsuhfid</span></p>
    </div>
    <script>
        document.querySelector('#wrapper').addEventListener('click',(e)=>{
            if(e.target.nodeName==='SPAN'){
                console.log(e.target.textContent);
            }
        })
    </script>
</body>
</html>
```
## performance on adding html element in document it increase time by repaint and reflow to prevent this we use fragment.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <script>
        // let t1=performance.now();
        // for(let i=0;i<1000;i++){
        //     let para=document.createElement('p');
        //     para.textContent='add text'+ i;
        //     document.body.appendChild(para)
        // }
        // let t2=performance.now()
        // console.log(t2-t1);

        // let t3=performance.now();
        // let myDiv=document.createElement('div');
        // for(let i=0;i<1000;i++){
        //     let para=document.createElement('p');
        //     para.textContent='add text'+ i;
        //     myDiv.appendChild(para)
        // }
        // document.body.appendChild(myDiv);
        // let t4=performance.now();
        // console.log(t4-t3);

        let t5=performance.now()
        let fragment=document.createDocumentFragment();
        for(let i=0;i<1000;i++){
            let para=document.createElement('p');
            para.textContent='add text'+ i;
            fragment.appendChild(para)
        }
        document.body.appendChild(fragment);
        let t6=performance.now()
        console.log(t6-t5);

    </script>
</body>
</html>
```

# 

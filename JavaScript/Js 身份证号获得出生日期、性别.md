```
//----------------------------------------------------------
//  功能：根据身份证号获得出生日期
//  参数：身份证号 psidno
//  返回值：出生日期
//----------------------------------------------------------
 function GetBirthday(psidno){
    var birthdayno,birthdaytemp
    if(psidno.length==18){
        birthdayno=psidno.substring(6,14)
    }else if(psidno.length==15){
        birthdaytemp=psidno.substring(6,12)
        birthdayno="19"+birthdaytemp
    }else{
        alert("错误的身份证号码，请核对！")
        return false
    }
    var birthday=birthdayno.substring(0,4)+"-"+birthdayno.substring(4,6)+"-"+birthdayno.substring(6,8)
    return birthday    
}
```
```
//----------------------------------------------------------
//  功能：根据身份证号获得性别
//  参数：身份证号 psidno
//  返回值：性别
//----------------------------------------------------------
function Getsex(psidno){
    var sexno,sex
    if(psidno.length==18){
        sexno=psidno.substring(16,17)
    }else if(psidno.length==15){
        sexno=psidno.substring(14,15)
    }else{
        alert("错误的身份证号码，请核对！")
        return false
    }
    var tempid=sexno%2;
    if(tempid==0){
        sex='F'
    }else{
        sex='M'
    }
    return sex
}
```

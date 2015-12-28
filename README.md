# somecode
record
//window.onload
function addLoadEvent(Func) {
    var oldLoad = window.onload;
    if (typeof window.onload != "function") {
        window.onload = Func;
    } else {
        window.onload = function () {
            oldLoad();
            Func();
        }
    }
    
    //insertafter
    function  insertAfter(a,b){
        var parent = b.parentNode;
        if(parent.lastChild == b){
            parent.appendChild(a)
        }else{
            parent.insertBefore(a,b.nextSibling)
        }
    }

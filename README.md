const SingleDay = 'yioytt.herokuapp.com'
const DoubleDay = 'yioytt.herokuapp.com'
addEventListener(
"fetch",event => {
let nd = new Date();
if (nd.getDate()%2) {
host = SingleDay
} else {
host = DoubleDay
} 
let url=new URL(event.request.url);
url.hostname=host;
let request=new Request(url,event.request);
event. respondWith(
fetch(request)
)
}
)



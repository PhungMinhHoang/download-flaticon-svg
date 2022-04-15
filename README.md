### Lưu ý
* Bạn cần đăng nhập vào flaticon trước rồi mới sử dụng nút này.
* Bạn chỉ có thể tải SVG khi bạn đang xem chi tiết một icon. Không thể tải ở trang listing.

### Thêm đoạn code sau vào url của Bookmark
```
javascript:(function()%7Bvar%20url%20%3D%20window.location.href.split(%22%3F%22)%5B0%5D%3Bvar%20filename%20%3D%20url.split(%22%2F%22)%5Burl.split(%22%2F%22).length%20-%201%5D%3Bvar%20id%20%3D%20filename.split(%22_%22)%5B1%5D%3Bif%20(!id)%20%7Balert(%22You%20can%20only%20download%20svg%20icon%20while%20viewing%20an%20icon.%22)%3Breturn%3B%7Dvar%20onlyName%20%3D%20filename.split(%22_%22)%5B0%5D%3Bfunction%20downloadURI(uri%2C%20name)%20%7Bvar%20link%20%3D%20document.createElement(%22a%22)%3Blink.setAttribute(%22download%22%2C%20name)%3Blink.href%20%3D%20uri%3Bdocument.body.appendChild(link)%3Blink.click()%3Blink.remove()%3B%7Dvar%20loggedin%20%3D%20document.getElementById(%22gr_connected%22)%3Bif%20(!loggedin)%20%7Balert(%22Please%20login%20before%20clicking%20on%20me.%22)%3Breturn%3B%7Dfetch(%22https%3A%2F%2Fwww.flaticon.com%2Feditor%2Ficon%2Fsvg%2F%22%20%2B%20id%20%2B%20%22%3Ftype%3Dstandard%22).then(function%20(response)%20%7Breturn%20response.json()%3B%7D).then((data)%20%3D%3E%20%7BdownloadURI(data.url%2C%20onlyName%20%2B%20%22.svg%22)%3B%7D).catch((error)%20%3D%3E%20%7Balert(%22Something%20went%20wrong%20%3E.%3C%22)%3B%7D)%7D)()
```

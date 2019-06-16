# Sample Express DevOps App

Practive DevOps using IBM Cloud continous delivery service.

Create your own custom DevOps toolchain to go from your source code to a running application in a minutes.

**Steps**

1. Fork/Clone the github repo by using the following command: `git clone https://github.com/samerfouad/sample-express-app.git`

1. `git clone YOUR_REPO_URL`

```javascript
var express = require('express');
var bodyParser = require('body-parser');
var port = process.env.PORT || 3000;
var app = express();
app.use(bodyParser.text());
function convertToCaps(str) {
    return str.toUpperCase();
}
app.get('/', function(req,res) {
    res.end('Hello Cloud Native Developers');
});
app.post('/api/capitalise', function(req, res) {
    res.send(convertToCaps(req.body));
})
if (require.main === module) {
    app.listen(port, function() {
        console.log('Server listening on port: ' + port);
    });
}
```

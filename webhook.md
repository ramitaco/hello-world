 app.get('/webhook', function (req, res) {
    if (req.query['hub.verify_token'] === 'all_you_need_is_love') {
      res.send(req.query['hub.challenge']);
    } else {
      res.send('Error, wrong validation token');    
    }
  });

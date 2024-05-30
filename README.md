### This is an HTML5 Sample App that triggers using two Rules. 

### Responsive Content with sample Rules created in inReality Platform 

* We have two sample Rules that is created
* Rule 1 - When a person is detected it will show the image "Come Closer"    --- druleid
* Rule 2 - When a person is engaged or in the emnagement zone it will show the image "Running shoes advertisement"    --- cruleid


#### How to run the HTML5 Demo ####
## Unzip the file and deploy it to any HTTP server. 
### If you do not have any HTTP server availavle you can do it using Python script below. Navigate to the unzipped folder and run the following commands
```sh
$ cd 'absolute path of directory'
$ python3 -m http.server 8000 # to start a local http server at port 8000
$ Open http://localhost:8000/index.html in a browser
```

#### How to change the Message Broker (MQ) IP address and other details

* MQ channel and authentication to subscribe to Rules Engine events 
* Update the below properties at line number 138 onwards

```
    var url = new URL(location.href);
    let mqHost = 'localhost';
    const topic = 'rvh';
    const username = 'rvh_readonly';
    const password = 'P2UK8P';
    const channel = 'event.outputs'
```

#### How to run it #####

* Create 2 rules - One for detection and one for closer.


#### Running the HTML5 Demo and passing the variables through the URL. 

`http://localhost:8000/index.html?druleid=<Rule id of Rule 1>&cruleid=<Rule id of Rule 2>&mqhost=<IP address of Message Broker>`

Example: `http://localhost:8000/index.html?druleid=abcdefghijklm098765&cruleid=xyzmnolk7654987&mqhost=192.168.0.19`


    
24.10.16  21.46
tags: [[web]] [[backend]] [[mongodb]] [[error]]

# unable to start mongodb

`sudo systemctl start mongod`  
`sudo systemctl status mongod  `
- shows 
- Active: failed (Result: exit-code) since Wed 2024-10-16 21:23:11 EAT; 3s ago

## tried
- look for a process using port :27017 and kill the process, but there were no process running on that port
- suggested by Gemini.

## what worked
- first i looked at the log files
	- `sudo cat /var/log/mongodb/mongod.log` 
- there was an error
`"msg":"Failed to unlink socket file","attr":{"path":"/tmp/m ongodb-27017.sock","error":"Operation not permitted"}}`

- pasted it into the browser and found similar question
- https://www.mongodb.com/community/forums/t/failed-to-unlink-socket-file-operation-not-permitted/208542/4

- `sudo rm -f /tmp/mongodb-27017.sock  `
- `sudo systemctl start mongod`  
- `sudo systemctl status mongod → Running`
- pasted the above command and it worked


# Reference


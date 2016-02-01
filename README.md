# todos 0.2.0
This is **"TODOS"** meteor demo application modified to work with Oracle database. It demonstrates the features of [metstrike:meteor-oracle](https://atmospherejs.com/metstrike/meteor-oracle) package, like elastic data model, oplog tailing, and reactivity.

## Installation
**Step 1:** Install or get access to any **Oracle Database**

**Step 2:** Install **Oracle Instant Client**

**Step 3:** Create a meteor account in your oracle database.
See [metstrike:meteor-oracle](https://atmospherejs.com/metstrike/meteor-oracle) for details.

**Step 4:** Check out and run TODOS
```bash
$ cd <PATH-TO-YOUR-WORKSPACE>
$ git clone https://github.com/metstrike/todos-oracle.git
$ cd todos-oracle
$ export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:<PATH-TO-YOUR-ORACLE-INSTANT-CLIENT>/instantclient_11_2/
$ meteor
```

## Connecting to different Oracle database/account
Modify the connection options in **lib/collections.js**
```js
if(Meteor.isServer) {
  Oracle.setDefaultOracleOptions(
    {connection: {
    	user: "scott", 
    	password: "tiger", 
    	connectString: "host:1521/sid"
    	}
    });
}
```


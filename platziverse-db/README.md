# Lab IoT


## Usage

const setupDatabase = require('db')

setupDatabase(config).then(db=> {
    const { Agent, Metric } = db
}).catch(err => console.error(err))
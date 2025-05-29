• Created a database named “todo”
use todo

• Inserted one record to a table named tasks_table
Table contains task_name, time(start,end), status of the task

db.todolist.find()
{
  _id: ObjectId('6836e14e0015f6fa849a8e0b'),
  Task: 'Wake up and wash the car',
  status: 'InComplete'
}
{
  _id: ObjectId('6836e14e0015f6fa849a8e0c'),
  Task: 'Take preworkout and Go to GYM ',
  status: 'InComplete'
}
{
  _id: ObjectId('6836e14e0015f6fa849a8e0d'),
  Task: 'Take Shower',
  status: 'InComplete'
}
db.todolist.insertMany([
  {"Task":"Eating BreakFast",
"status":"InComplete"
},
  {"Task":"Drinking Water",
"status":"InComplete"
},
  {"Task":"Driving The Car",
"Status":"InComplete"
},
  {"Task":"Going to Office",
"status":"InComplete"
},
  {"Task":"Eating Lunch",
"status":"InComplete"
},
  {"Task":"Completing Work",
"status":"InComplete"
},
  {"Task":"Sleep",
"status"""InComplete
}
])
db.todolist.updateMany(
{"status":"InComplete"},
{$set:{"status":true}}
)
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 9,
  modifiedCount: 9,
  upsertedCount: 0
}
db.todolist.find()
{
  _id: ObjectId('6836e14e0015f6fa849a8e0b'),
  Task: 'Wake up and wash the car',
  status: true
}
{
  _id: ObjectId('6836e14e0015f6fa849a8e0c'),
  Task: 'Take preworkout and Go to GYM ',
  status: true
}
{
  _id: ObjectId('6836e14e0015f6fa849a8e0d'),
  Task: 'Take Shower',
  status: true
}
{
  _id: ObjectId('6836e749d68e73f50adc76f7'),
  Task: 'Eating BreakFast',
  status: true
}

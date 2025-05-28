<pre># mongo_ass

use to-do-list
switched to db to-do-list
db["sudheshna"].find()
{}


db.sudheshna.insertOne({title:"buy groceries",completed:"false",dueDate:"2025-06-01"})
{
  acknowledged: true,
  insertedId: ObjectId('6836e1f73b607dc4240f3f41')
}

db.sudheshna.insertOne({title:"study for exam",completed:"true",dueDate:"2025-19-01"})
{
  acknowledged: true,
  insertedId: ObjectId('6836e2333b607dc4240f3f42')
}

db.sudheshna.insertOne({title:"wash clothes",completed:"false",dueDate:"2025-28-05"})
{
  acknowledged: true,
  insertedId: ObjectId('6836e3303b607dc4240f3f43')
}


db.sudheshna.insertOne({title:"cook food",completed:"true","dueDate":"2025-28-05"})
{
  acknowledged: true,
  insertedId: ObjectId('6836e3553b607dc4240f3f44')
}


db.sudheshna.insertMany([{title:"exercise",completed:"true",dueDate:"2025-26-05"},{title:"organize desk",completed:"true","dueDate":"2025-27-05"}])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('6836e4f73b607dc4240f3f45'),
    '1': ObjectId('6836e4f73b607dc4240f3f46')
  }
}


db.sudheshna.insertMany([{title:"call mom",completed:"false",dueDate:"2025-28-04"},{title:"read novel",completed:"false","dueDate":"2025-22-05"}])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('6836e55d3b607dc4240f3f47'),
    '1': ObjectId('6836e55d3b607dc4240f3f48')
  }
}


db.sudheshna.insertMany([{title:"pay electricity bill",completed:"true",dueDate:"2025-01-05"},{title:"reply to mail",completed:"true","dueDate":"2025-12-05"}])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('6836e5a73b607dc4240f3f49'),
    '1': ObjectId('6836e5a73b607dc4240f3f4a')
  }
}


db.sudheshna.find()
{
  _id: ObjectId('6836e1f73b607dc4240f3f41'),
  title: 'buy groceries',
  completed: 'false',
  dueDate: '2025-06-01'
}


{
  _id: ObjectId('6836e2333b607dc4240f3f42'),
  title: 'study for exam',
  completed: 'true',
  dueDate: '2025-19-01'
}


{
  _id: ObjectId('6836e3303b607dc4240f3f43'),
  title: 'wash clothes',
  completed: 'false',
  dueDate: '2025-28-05'
}


{
  _id: ObjectId('6836e3553b607dc4240f3f44'),
  title: 'cook food',
  completed: 'true',
  dueDate: '2025-28-05'
}


{
  _id: ObjectId('6836e4f73b607dc4240f3f45'),
  title: 'exercise',
  completed: 'true',
  dueDate: '2025-26-05'
}


{
  _id: ObjectId('6836e4f73b607dc4240f3f46'),
  title: 'organize desk',
  completed: 'true',
  dueDate: '2025-27-05'
}


{
  _id: ObjectId('6836e55d3b607dc4240f3f47'),
  title: 'call mom',
  completed: 'false',
  dueDate: '2025-28-04'
}

{
  _id: ObjectId('6836e55d3b607dc4240f3f48'),
  title: 'read novel',
  completed: 'false',
  dueDate: '2025-22-05'
}


{
  _id: ObjectId('6836e5a73b607dc4240f3f49'),
  title: 'pay electricity bill',
  completed: 'true',
  dueDate: '2025-01-05'
}


{
  _id: ObjectId('6836e5a73b607dc4240f3f4a'),
  title: 'reply to mail',
  completed: 'true',
  dueDate: '2025-12-05'
}
db.sudheshna.find({completed:false})
db.sudheshna.find({completed:"false"})
{
  _id: ObjectId('6836e1f73b607dc4240f3f41'),
  title: 'buy groceries',
  completed: 'false',
  dueDate: '2025-06-01'
}
{
  _id: ObjectId('6836e3303b607dc4240f3f43'),
  title: 'wash clothes',
  completed: 'false',
  dueDate: '2025-28-05'
}
{
  _id: ObjectId('6836e55d3b607dc4240f3f47'),
  title: 'call mom',
  completed: 'false',
  dueDate: '2025-28-04'
}
{
  _id: ObjectId('6836e55d3b607dc4240f3f48'),
  title: 'read novel',
  completed: 'false',
  dueDate: '2025-22-05'
}
db.sudheshna.find({completed:"true"})
{
  _id: ObjectId('6836e2333b607dc4240f3f42'),
  title: 'study for exam',
  completed: 'true',
  dueDate: '2025-19-01'
}
{
  _id: ObjectId('6836e3553b607dc4240f3f44'),
  title: 'cook food',
  completed: 'true',
  dueDate: '2025-28-05'
}
{
  _id: ObjectId('6836e4f73b607dc4240f3f45'),
  title: 'exercise',
  completed: 'true',
  dueDate: '2025-26-05'
}
{
  _id: ObjectId('6836e4f73b607dc4240f3f46'),
  title: 'organize desk',
  completed: 'true',
  dueDate: '2025-27-05'
}
{
  _id: ObjectId('6836e5a73b607dc4240f3f49'),
  title: 'pay electricity bill',
  completed: 'true',
  dueDate: '2025-01-05'
}
{
  _id: ObjectId('6836e5a73b607dc4240f3f4a'),
  title: 'reply to mail',
  completed: 'true',
  dueDate: '2025-12-05'
}
db.sudheshna.find({duedate:"2025-01-05"})
db.sudheshna.find({dueDate:"2025-01-05"})
{
  _id: ObjectId('6836e5a73b607dc4240f3f49'),
  title: 'pay electricity bill',
  completed: 'true',
  dueDate: '2025-01-05'
}
db.sudheshna.updateMany({completed:"true"},{$set:{completed:"false"}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 6,
  modifiedCount: 6,
  upsertedCount: 0
}
db.sudheshna.insertOne({title:"pack your bags",completed:"true","dueDate":"2025-28-05"})
{
  acknowledged: true,
  insertedId: ObjectId('6836e91e3b607dc4240f3f4b')
}
db.sudheshna.updateMany({completed:"false"},{$set:{completed:"true"}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 10,
  modifiedCount: 10,
  upsertedCount: 0
}
db.sudheshna.updateMany({completed:"true"},{$set:{completed:"false"}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 11,
  modifiedCount: 11,
  upsertedCount: 0
}
db.sudheshna.updateMany({},[{$set:{dueDate:
"$Time CreatedAt"}}])
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 11,
  modifiedCount: 11,
  upsertedCount: 0
}
db.sudheshna.updateMany({},[{$set:{dueDate:
"Time CreatedAt"}}])
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 11,
  modifiedCount: 11,
  upsertedCount: 0
}
db.sudheshna.updateMany({},[{$set:{TimecreatedAt:"2025-02-04"}}])
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 11,
  modifiedCount: 11,
  upsertedCount: 0
}
db.sudheshna.updateMany({},{$set:{TimecreatedAt:new Date()}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 11,
  modifiedCount: 11,
  upsertedCount: 0
}
db.sudheshna.deleteMany({$expr:{$eq:["$dueDate","$Time CreatedAt"]}})
{
  acknowledged: true,
  deletedCount: 0
}
db.sudheshna.updateMany({},{$unset:{dueDate:""}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 11,
  modifiedCount: 11,
  upsertedCount: 0
}
db.sudheshna.updateMany({},{$set:{TimeupdatedAt:new Date()}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 11,
  modifiedCount: 11,
  upsertedCount: 0
}
db.sudheshna.updateMany({_id:{$in:[ObjectId("6836e1f73b607dc4240f3f41"),
ObjectId("6836e2333b607dc4240f3f42"),
ObjectId("6836e3303b607dc4240f3f43"),
ObjectId("6836e3553b607dc4240f3f44"),
ObjectId("6836e55d3b607dc4240f3f47")]}},
{$set:{completed:"true", 
TimeupdatedAt:new Date()}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 5,
  modifiedCount: 5,
  upsertedCount: 0
}
db.sudheshna.updateMany( { title: { $in: ["study for exam", "exercise"] } },
  { $set: { priority: "High" } }
)
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 2,
  modifiedCount: 2,
  upsertedCount: 0
}
db.sudheshna.updateMany(
  { title: "wash clothes" },
  { $set: { priority: "Low" } }
)
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
db.sudheshna.updateMany(
  { priority: { $exists: false } },
  { $set: { priority: "Medium" } }
)
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 8,
  modifiedCount: 8,
  upsertedCount: 0
}
db.sudheshna.updateOne(
  { _id: ObjectId("6836e1f73b607dc4240f3f41") },
  {
    $set: {
      completed: "false",
      TimeupdatedAt: new Date()
    }
  }
)
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
db.sudheshna.updateOne(
  { title: "buy groceries" },
  {
    $set: {
      completed: "false",
      TimeupdatedAt: new Date()
    }
  }
)
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
db.sudheshna.countDocuments()
11
db.sudheshna.deleteOne({ title: "read novel"})
{
  acknowledged: true,
  deletedCount: 1
}
db.sudheshna.countDocuments()
10
db.sudheshna.find().sort({ TimecreatedAt: 1 })
{
  _id: ObjectId('6836e1f73b607dc4240f3f41'),
  title: 'buy groceries',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T14:38:24.751Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e2333b607dc4240f3f42'),
  title: 'study for exam',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'High'
}
{
  _id: ObjectId('6836e3303b607dc4240f3f43'),
  title: 'wash clothes',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'Low'
}
{
  _id: ObjectId('6836e3553b607dc4240f3f44'),
  title: 'cook food',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e4f73b607dc4240f3f45'),
  title: 'exercise',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'High'
}
{
  _id: ObjectId('6836e4f73b607dc4240f3f46'),
  title: 'organize desk',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e55d3b607dc4240f3f47'),
  title: 'call mom',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e5a73b607dc4240f3f49'),
  title: 'pay electricity bill',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e5a73b607dc4240f3f4a'),
  title: 'reply to mail',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e91e3b607dc4240f3f4b'),
  title: 'pack your bags',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium'
}
db.sudheshna.find().sort({ TimeupdatedAt: -1 })
{
  _id: ObjectId('6836e1f73b607dc4240f3f41'),
  title: 'buy groceries',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T14:38:24.751Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e2333b607dc4240f3f42'),
  title: 'study for exam',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'High'
}
{
  _id: ObjectId('6836e3303b607dc4240f3f43'),
  title: 'wash clothes',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'Low'
}
{
  _id: ObjectId('6836e3553b607dc4240f3f44'),
  title: 'cook food',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e55d3b607dc4240f3f47'),
  title: 'call mom',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e4f73b607dc4240f3f45'),
  title: 'exercise',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'High'
}
{
  _id: ObjectId('6836e4f73b607dc4240f3f46'),
  title: 'organize desk',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e5a73b607dc4240f3f49'),
  title: 'pay electricity bill',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e5a73b607dc4240f3f4a'),
  title: 'reply to mail',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e91e3b607dc4240f3f4b'),
  title: 'pack your bags',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium'
}
db.sudheshna.find().sort({ priority: 1 })
{
  _id: ObjectId('6836e2333b607dc4240f3f42'),
  title: 'study for exam',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'High'
}
{
  _id: ObjectId('6836e4f73b607dc4240f3f45'),
  title: 'exercise',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'High'
}
{
  _id: ObjectId('6836e3303b607dc4240f3f43'),
  title: 'wash clothes',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'Low'
}
{
  _id: ObjectId('6836e1f73b607dc4240f3f41'),
  title: 'buy groceries',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T14:38:24.751Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e3553b607dc4240f3f44'),
  title: 'cook food',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e4f73b607dc4240f3f46'),
  title: 'organize desk',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e55d3b607dc4240f3f47'),
  title: 'call mom',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e5a73b607dc4240f3f49'),
  title: 'pay electricity bill',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e5a73b607dc4240f3f4a'),
  title: 'reply to mail',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e91e3b607dc4240f3f4b'),
  title: 'pack your bags',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium'
}
db.sudheshna.find().sort({ completed: 1 })
{
  _id: ObjectId('6836e1f73b607dc4240f3f41'),
  title: 'buy groceries',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T14:38:24.751Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e4f73b607dc4240f3f45'),
  title: 'exercise',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'High'
}
{
  _id: ObjectId('6836e4f73b607dc4240f3f46'),
  title: 'organize desk',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e5a73b607dc4240f3f49'),
  title: 'pay electricity bill',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e5a73b607dc4240f3f4a'),
  title: 'reply to mail',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e91e3b607dc4240f3f4b'),
  title: 'pack your bags',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e2333b607dc4240f3f42'),
  title: 'study for exam',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'High'
}
{
  _id: ObjectId('6836e3303b607dc4240f3f43'),
  title: 'wash clothes',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'Low'
}
{
  _id: ObjectId('6836e3553b607dc4240f3f44'),
  title: 'cook food',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'Medium'
}
{
  _id: ObjectId('6836e55d3b607dc4240f3f47'),
  title: 'call mom',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'Medium'
}
db.sudheshna.updateMany(
  {},
  { $set: { DueDate: new Date() } }
)
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 10,
  modifiedCount: 10,
  upsertedCount: 0
}
db.sudheshna.find({
  DueDate: {
    $gte: new Date("2025-05-28T00:00:00.000Z"),
    $lte: new Date("2025-05-28T23:59:59.999Z")
  }
})
{
  _id: ObjectId('6836e1f73b607dc4240f3f41'),
  title: 'buy groceries',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T14:38:24.751Z,
  priority: 'Medium',
  DueDate: 2025-05-28T14:51:04.341Z
}
{
  _id: ObjectId('6836e2333b607dc4240f3f42'),
  title: 'study for exam',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'High',
  DueDate: 2025-05-28T14:51:04.341Z
}
{
  _id: ObjectId('6836e3303b607dc4240f3f43'),
  title: 'wash clothes',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'Low',
  DueDate: 2025-05-28T14:51:04.341Z
}
{
  _id: ObjectId('6836e3553b607dc4240f3f44'),
  title: 'cook food',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'Medium',
  DueDate: 2025-05-28T14:51:04.341Z
}
{
  _id: ObjectId('6836e4f73b607dc4240f3f45'),
  title: 'exercise',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'High',
  DueDate: 2025-05-28T14:51:04.341Z
}
{
  _id: ObjectId('6836e4f73b607dc4240f3f46'),
  title: 'organize desk',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium',
  DueDate: 2025-05-28T14:51:04.341Z
}
{
  _id: ObjectId('6836e55d3b607dc4240f3f47'),
  title: 'call mom',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'Medium',
  DueDate: 2025-05-28T14:51:04.341Z
}
{
  _id: ObjectId('6836e5a73b607dc4240f3f49'),
  title: 'pay electricity bill',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium',
  DueDate: 2025-05-28T14:51:04.341Z
}
{
  _id: ObjectId('6836e5a73b607dc4240f3f4a'),
  title: 'reply to mail',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium',
  DueDate: 2025-05-28T14:51:04.341Z
}
{
  _id: ObjectId('6836e91e3b607dc4240f3f4b'),
  title: 'pack your bags',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium',
  DueDate: 2025-05-28T14:51:04.341Z
}
db.sudheshna.find({
  DueDate: { $lt: new Date() }
})
{
  _id: ObjectId('6836e1f73b607dc4240f3f41'),
  title: 'buy groceries',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T14:38:24.751Z,
  priority: 'Medium',
  DueDate: 2025-05-28T14:51:04.341Z
}
{
  _id: ObjectId('6836e2333b607dc4240f3f42'),
  title: 'study for exam',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'High',
  DueDate: 2025-05-28T14:51:04.341Z
}
{
  _id: ObjectId('6836e3303b607dc4240f3f43'),
  title: 'wash clothes',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'Low',
  DueDate: 2025-05-28T14:51:04.341Z
}
{
  _id: ObjectId('6836e3553b607dc4240f3f44'),
  title: 'cook food',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'Medium',
  DueDate: 2025-05-28T14:51:04.341Z
}
{
  _id: ObjectId('6836e4f73b607dc4240f3f45'),
  title: 'exercise',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'High',
  DueDate: 2025-05-28T14:51:04.341Z
}
{
  _id: ObjectId('6836e4f73b607dc4240f3f46'),
  title: 'organize desk',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium',
  DueDate: 2025-05-28T14:51:04.341Z
}
{
  _id: ObjectId('6836e55d3b607dc4240f3f47'),
  title: 'call mom',
  completed: 'true',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:32:37.325Z,
  priority: 'Medium',
  DueDate: 2025-05-28T14:51:04.341Z
}
{
  _id: ObjectId('6836e5a73b607dc4240f3f49'),
  title: 'pay electricity bill',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium',
  DueDate: 2025-05-28T14:51:04.341Z
}
{
  _id: ObjectId('6836e5a73b607dc4240f3f4a'),
  title: 'reply to mail',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium',
  DueDate: 2025-05-28T14:51:04.341Z
}
{
  _id: ObjectId('6836e91e3b607dc4240f3f4b'),
  title: 'pack your bags',
  completed: 'false',
  TimecreatedAt: 2025-05-28T11:11:31.122Z,
  TimeupdatedAt: 2025-05-28T11:21:48.680Z,
  priority: 'Medium',
  DueDate: 2025-05-28T14:51:04.341Z
}
db.sudheshna.insertOne({
  _id: ObjectId("6836ea9b3b607dc4240f3f4c"),
  title: "finish project report",
  completed: "true",
  TimecreatedAt: new Date("2025-05-28T14:20:00.000Z"),
  TimeupdatedAt: new Date("2025-05-28T14:30:00.000Z"),
  priority: "High",
  DueDate: new Date("2025-05-28T16:00:00.000Z")
})

{
  acknowledged: true,
  insertedId: ObjectId('6836ea9b3b607dc4240f3f4c')
}
db.sudheshna.find({
  TimecreatedAt: {
    $gte: new Date(Date.now() - 20 * 60 * 1000)
  }
})
 db.sudheshna.insertOne({
  _id: ObjectId("6836ea9b3b607dc4240f3f4c"),
  title: "finish project report",
  completed: "true",
  TimecreatedAt: new Date("2025-05-28T14:20:00.000Z"),
  TimeupdatedAt: new Date("2025-05-28T14:30:00.000Z"),
  priority: "High",
  DueDate: new Date("2025-05-28T16:00:00.000Z")
})
</pre>

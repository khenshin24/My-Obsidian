
@blp.response(200,UserLoginLogsSchema(many=True))
		In the context of the `UserLoginLogsSchema`, `many=True` indicates that the response will contain multiple instances of `UserLoginLogsSchema`. This is typically used when the response is expected to be a list or collection of objects rather than a single object.


Nested = login_log.py files

class UserWithLogsSchema(Schema): id = fields.UUID() username = fields.Str() logs = fields.Nested(LogSchema, many=True) what is the meaning of Nested

ChatGPT

In the context of marshmallow, a Python library for object serialization, `Nested` is a field type used to represent nested (or embedded) objects within another object.

In the schema you provided, `Nested` is used to indicate that the `logs` field contains a nested structure of objects defined by the `LogSchema`. By specifying `many=True`, it indicates that `logs` can contain multiple instances of the nested `LogSchema`.

For example, if you have a `UserWithLogs` object, it may have multiple logs associated with it. Each log would be represented as an instance of the `LogSchema`, and they would be nested within the `logs` field of the `UserWithLogs` object.


[How to Create Joins in SQLAlchemy (youtube.com)](https://www.youtube.com/watch?v=FDrB5X3zSHc)
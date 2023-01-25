# Dart Records and Patterns

A project to play around with Records and Patterns.

The bellow code can be seen inside ./bin folder. 
```dart
Future<(Exception?, String?)> dummyResponse() async {
  if(DateTime.now().millisecondsSinceEpoch %2 == 0) {
    /// error
    return (Exception('Some dummy exception'), null);
  }

  /// success
  return (null, 'Some dummy data', );
}

void main(List<String> arguments) async {
  final (data, error) = await dummyResponse();

  if(error!=null) {
    ///handle error...
    print(error);
    return;
  }
  ///handle success...
  print(data);
}
```

# Swipe Actions New

# swipe_actions_new

A widget which can be used to call functions when the wrapped child is dragged or flinged. Only intended to work with horizontal swipes.
Original Library: [Swipe Actions](https://pub.dev/packages/swipe_actions)

## Getting Started

Import the package

```dart
import 'package:swipe_actions_new/swipe_actions.dart';
```

And use Swipe class, for example:
```dart
Swipe(
    child: ListTile(
      title: Text("Some Child"),
    ),
    menuItems: <SwipeAction>[
      SwipeAction(
        icon: Icons.add,
        onSelect: () {
          setState(() {
            _counts[i]++;
          });
        },
        highlighColor: Colors.green,
      ),
      SwipeAction(
        icon: Icons.remove,
        onSelect: () {
          setState(() {
            _counts[i]--;
          });
        },
        highlighColor: Colors.red,
      ),
      SwipeAction(
        icon: Icons.open_in_new,
        onSelect: () {
          Navigator.push(
            context,
            MaterialPageRoute(
                builder: (context) => Scaffold(
                      appBar: AppBar(
                        title: Text("Counter $i"),
                      ),
                      body: Center(
                          child: Text(
                        _counts[i].toString(),
                        style: TextStyle(fontSize: 100),
                      )),
                    )),
          );
        },
        highlighColor: Colors.yellow,
      )
    ],
)
```

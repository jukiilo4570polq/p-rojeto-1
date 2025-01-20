# p-rojeto-1
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: Text("Layout Responsivo")),
        body: LayoutBuilder(
          builder: (context, constraints) {
            if (constraints.maxWidth < 600) {
              return Column(
                children: [
                  Text("Tela Pequena", style: TextStyle(fontSize: 24)),
                ],
              );
            } else {
              return Row(
                children: [
                  Text("Tela Grande", style: TextStyle(fontSize: 24)),
                ],
              );
            }
          },
        ),
      ),
    );
  }
}

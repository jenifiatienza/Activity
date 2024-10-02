import 'package:flutter/material.dart';

void main () => runApp (const AnimatedAlignmentExampleApp());

class AnimatedAlignmentExampleApp extends StatelessWidget {
  const AnimatedAlignmentExampleApp ({super.key});

  static const Duration duration = Duration(seconds: 1);
  static const Curve curve = Curves.fastOutSlowIn;


  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: Text('Animated Align Sample')),
        body: const AnimatedAlignmentExample(
          duration:duration,
          curve:curve,
        ),
      )
    );
  }
}

class AnimatedAlignmentExample extends StatefulWidget{
  const AnimatedAlignmentExample({
    required this.duration,
    required this.curve,
    super.key,
});
  final Duration duration;
  final Curve curve;

  @override
  State<AnimatedAlignmentExample> createState() => _AnimatedAlignmentExampleState();
  }
  class _AnimatedAlignmentExampleState extends State<AnimatedAlignmentExample>{
    bool selected = false;

  @override
  Widget build(BuildContext context) {
    return GestureDetector(
      onTap: () {
        setState(() {
                  selected = !selected; 
                });
      },
      child: Center(
        child: Container(
              width: 250.0,
        height: 250.0,
        color: Colors.red,
        child: AnimatedAlign(
          alignment: selected ? Alignment.topRight: Alignment.bottomLeft,
           duration: widget.duration,
           curve: widget.curve,
           child: const FlutterLogo( size: 50.0)
           ),

        )
    
        ),
      );
  }

}

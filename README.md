# Flutter-App-
main.dart
import 'package:flutter/material.dart';
import 'package:http/http.dart' as http;
void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: SearchPage(),
    );
  }
}

class SearchPage extends StatefulWidget {
  const SearchPage({Key? key}) : super(key: key);
  @override
  State<SearchPage> createState() => _SearchPageState();
}



class _HomepageState extends State<Homepage>{

}

class _SearchPageState extends State<SearchPage> {
  void updateList(String value) {
    final uri = Uri.parse(
        'https://raw.githubusercontent.com/https://drive.google.com/file/d/1ibmr3WD7Jw6oLL6O_W390WojCLfCHw-k/view?usp=sharing');
    final response = await http.get(uri);
  }


  class _HomepageState extends State<Homepage>{
    int _value=1;



  class _AvailabilityState extends State<Availability>{
    int _value = 2;
  }

}
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Color(0xFF1f1545),
      appBar: AppBar(
        backgroundColor: Color(0xFF1f1545),
        elevation: 0.0,
      ),
      body: Padding(
        padding: EdgeInsets.all(16),
        child: Column(
          mainAxisAlignment: MainAxisAlignment.start,
          crossAxisAlignment: CrossAxisAlignment.start,
          children: [
            Text(
              "Search",
              style: TextStyle(
                  color: Colors.white,
                  fontSize: 22.0,
                  fontWeight: FontWeight.bold),
            ),
            SizedBox(
              height: 20.0,
            ),
            TextField(
              style: TextStyle(color: Colors.white),
              decoration: InputDecoration(
                filled: true,
                fillColor: Color(0xff302360),
                border: OutlineInputBorder(
                  borderRadius: BorderRadius.circular(8.0),
                  borderSide: BorderSide.none,
                ),
                hintText: "eg: Name",
                prefixIcon: Icon(Icons.search),
                prefixIconColor: Colors.pink.shade100,
              ),
            ),
            SizedBox(
              height: 20.0,
            ),
            Expanded(
              children:[
                Row(children: [
                  Radio(
                    value: 1,
                    groupValue: _value,
                    onChanged: (value){
                      setState(() {
                        _value = value ;
                      });
                    },
                  ),
                  SizedBox(width: 10.0,),
                  Text("Male"),
                ],),
                Row(children: [
                  Radio(
                    value: 2,
                    groupValue: _value,
                    onChanged: (value){
                      setState(() {
                        _value = value;
                      });
                    },
                  ),
                  SizedBox(width: 10.0,),
                  Text("Female"),
                ],),
                Row(children: [
                  Radio(
                    value: 3,
                    groupValue: _value,
                    onChanged: (value){
                      setState(() {
                        _value = value;
                      });
                    },
                  ),
                  SizedBox(width: 10.0,),
                  Text("Others"),
                ],),
              ]
              )
            )




    Widget build(BuildContext, context){
      children:[
        "Availabity",
        style:TextStyle(
          color: Colors.white,
          fontSize: 22.0;
          fontWeight:FontWeight.bold),

        ),
           Expanded(
              children:[
                Row(children: [
                  Radio(
                    value: 2,
                    groupValue: _value,
                    onChanged: (value){
                      setState(() {
                        _value = value ;
                      });
                    },
                  ),
                  SizedBox(width: 10.0,),
                  Text("Yes"),
                ],),
                Row(children: [
                  Radio(
                    value: 2,
                    groupValue: _value,
                    onChanged: (value){
                      setState(() {
                        _value = value;
                      });
                    },
                  ),
                  SizedBox(width: 10.0,),
                  Text("No"),
                ],),
                ],),
      
      ]
      

    @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Color(0xFF1f1545),
      appBar: AppBar(
        backgroundColor: Color(0xFF1f1545),
        elevation: 0.0,
      ),
      body: Padding(
        padding: EdgeInsets.all(16),
        child: Column(
          mainAxisAlignment: MainAxisAlignment.start,
          crossAxisAlignment: CrossAxisAlignment.start,
          children: [
            Text(
              "Create Team",
              style: TextStyle(
                  color: Colors.white,
                  fontSize: 22.0,
                  fontWeight: FontWeight.bold),
            ),
      
    })
          ],
        ),
      ),
   )
   }
   ))))))) );
  }
}





widget_test.dart

import 'package:flutter/material.dart';

class Widget extends StatefulWidget {
  const Widget({Key? key}) : super(key: key);

  @override
  State<Widget> createState() => WidgetState();
}

class WidgetState extends State<Widget> {
  String dropdownValue = 'One';

  @override
  Center build(BuildContext context) {
    return Center(
      child: DropdownButton<String>(
        value: dropdownValue,
        icon: const Icon(Icons.menu),
        style: const TextStyle(color: Colors.white),
        underline: Container(
          height: 2,
          color: const Color.fromARGB(255, 99, 77, 77),
        ),
        onChanged: (String? newValue) {
          setState(() {
            dropdownValue = newValue!;
          });
        },
        items: const [
          DropdownMenuItem<String>(
            value: "One",
            child: Text('Marketing'),
          ),
          DropdownMenuItem<String>(
            value: "Two",
            child: Text('Finance'),
          ),
          DropdownMenuItem<String>(
            value: "Three",
            child: Text('Sales'),
          ),
          DropdownMenuItem<String>(
            value: "Four",
            child: Text('IT'),
          ),
          DropdownMenuItem<String>(
            value: "Five",
            child: Text('UI designing'),
          ),
          DropdownMenuItem<String>(
            value: "Six",
            child: Text('Business Development'),
          ),
        ],
      ),
    );
  }
}










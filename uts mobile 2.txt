import 'package:flutter/material.dart';

void main () {
	runApp(MaterialApp (
	debugShow-CheckedModeBanner:false,
	title : 'Routing Navigation',
	initialRoute : '/',
	routes: {
		'/'  : (context) => HalamanPertama (),
		HalamanKedua.routeName : (context) => HalamanKedua (), 
		HalamanKetiga.routeName : (context) => HalamanKetiga(),
		HalamanKeempat.routname : (context) => HalamanKeempat(),
    }'
  ));
 }



class HalamanPertama extends StatelessWidget {
 @override
 Widget build(BuildContext context) {
 return Scaffold(
	appBar: AppBar(
	title : Text ('Halaman Pertama'},
	),
	body: Center(
		child: ListView(
			children: <Widget>[
				RaisedButton(
				child: Text('Pindah Halaman Kedua'),
				onPressed: () (
				  Navigator.pusNamed(context, HalamanKedua.routeName);
				},
	 			),
				RaisedButton(
				  child: Text('Pindah Halaman Ketiga'),
				  onPressed: () {
					Navigator.pushReplacementNamed(context, HalamanKetiga.routeName);
				},
	 			),
				RaisedButton(
				  child: Text('Pindah Halaman Keempat'),
				  onPressed: () {
					Navigator.pushReplacementNamed(context, HalamanKeempat.routeName);
	      	  },
	        ),
	      },
	    ),
	  ],	
	),
      ),	
    );
  }
}

class HalamanKedua extends StatelessWidget {
 static const String routeName = "/halamanKedua";
 @override
 Widget build(BuildContext context) {
	return Scaffold(
		appBar: AppBar
			title: Text("Halaman Kedua"),
		),
		body: Center(
			child: RaisedButton(
				child: Text('Kembali'),
				onPressed: () {
				Navigator.pop(context);
       },
      ),
     ),
    );
   }
  }

class HalamanKetiga extends StatelessWidget {
 static const String routName = "\halamanKetiga";
 @override
 Widget build(BuildContext ) {
	return scaffold(
		appBar: AppBar(
			title: Text("Halaman Ketiga"),
		),
		body: Center(
			child: Text('Halaman Ketiga'),
   ),
  );
 }
}

class HalamanKeempat extends StatelessWidget {
 static const String routName = "\halamanKeempat";
 @override
 Widget build(BuildContext ) {
	return scaffold(
		appBar: AppBar(
			title: Text("Halaman Keempat"),
		),
		body: Center(
			child: Text('Halaman Keempat'),
   ),
  );
 }
}

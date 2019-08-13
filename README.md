# rewards-using-spring

##Technologies used for this project:  Spring Boot, H2, Maven

Please follow the below steps 
1)	Do maven clean install 
2)	Start the application
3)	Type below url in browser, this will calculate the reward points  and create dataset information in H2 DB
http://localhost:8080/createDataSet
Sample data:
 Rewards r1 = new Rewards();
		r1.setCustomerName("cust1");
		r1.setPurchaseAmount(120);
		r1.setCreatedDate(sdf.parse("10/06/2019"));
		
		Rewards r2 = new Rewards();
		r2.setCustomerName("cust1");
		r2.setPurchaseAmount(80);
		r2.setCreatedDate(sdf.parse("12/07/2019"));
		
		Rewards r3 = new Rewards();
		r3.setCustomerName("cust1");
		r3.setPurchaseAmount(120);
		r3.setCreatedDate(sdf.parse("10/08/2019"));
		
		Rewards r4 = new Rewards();
		r4.setCustomerName("cust1");
		r4.setPurchaseAmount(90);
		r4.setCreatedDate(sdf.parse("11/08/2019"));
		
		// 2nd Customer
		Rewards c1 = new Rewards();
		c1.setCustomerName("cust2");
		c1.setPurchaseAmount(120);
		c1.setCreatedDate(sdf.parse("13/07/2019"));
		
		Rewards c2 = new Rewards();
		c2.setCustomerName("cust2");
		c2.setPurchaseAmount(110);
		c2.setCreatedDate(sdf.parse("12/08/2019"));

4)	Type below url to get the customer total earning points and monthly wise total earning points
http://localhost:8080/getCustomerRewardPoints?customerName=cust1

Sample Output:
{"totalPoints":250,"rewards":[{"month":6,"monthPoints":90},{"month":7,"monthPoints":30},{"month":8,"monthPoints":130}]}


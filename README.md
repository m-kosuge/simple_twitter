# simple_twitter
簡易Twitter(Java)

CREATE TABLE users ( 
	id 				    INTEGER 			AUTO_INCREMENT 	    			PRIMARY KEY,
	account 		  VARCHAR(20) 	UNIQUE 			    NOT NULL,
	name 			    VARCHAR(20) 						      NOT NULL,
	email 			  VARCHAR(50) 	UNIQUE 			    NOT NULL,
	password 		  VARCHAR(255) 					        NOT NULL,
	description 	TEXT 							            NOT NULL,
	created_date 	TIMESTAMP 						        NOT NULL 	DEFAULT CURRENT_TIMESTAMP,
	updated_date 	TIMESTAMP 						        NOT NULL 	DEFAULT CURRENT_TIMESTAMP
);

CREATE TABLE messages ( 
	id 			    	INTEGER 			AUTO_INCREMENT 				    PRIMARY KEY,
	user_id 	  	INTEGER 						          NOT NULL,
	text 			    TEXT 							            NOT NULL,
	created_date 	TIMESTAMP 						        NOT NULL 	DEFAULT CURRENT_TIMESTAMP,
	updated_date 	TIMESTAMP 						        NOT NULL 	DEFAULT CURRENT_TIMESTAMP
);

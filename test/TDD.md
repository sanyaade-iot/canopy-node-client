3rd Party REST api in Node

-main interactions between your client
and the API
	-store/fetch
	-api Keys
	-Time-varient data
-goals
	-fast
	-granular
	- -as representative as possible- -

-mocks/stubs

-Store & Fetch
	-Store (POST) ->
	                |	                
	-Fetch (GET)  <-

-Mocha
	describe a test suite:

(	i.e. describe('Youtube', function(){
			this.timeout(10000);
			before(function(){
					nockturnal.before()
				});
		});
		it('Require key', function(done){
			var youTube = new YouTube();
			youTube.search(config.query, 1, function(response){
				response.should.have.paroperty('error', {...})
				...
			done();
				})
		after(function(done){
				...		
		});		
			});

	-Nock - simulates HTTP requests?

		-Nockturnal
		 - easy recording
		 - Inhibits external HTTP requests
		 - Hides "plain text secrets"
		 - *works with time-varying data

mocha stores the req/res in 'fixtures/blah.json'  and uses "scope" :
				"method" : 
				"path":

nockturnal give you place holders that encode your private keys (plain text secret) and hides it from version control

mcok.config.conf.js
module.exports= {
	key:'MOCK_KEY',
	id:'MOCK_ID',
	query: 'nodejs song'
}




-------------------------


gcloud-promise

-connects to google cloud services and make an oauth call

-needs GClOUD_KEYFILE = cred.json mocha
 
 -gcloud-datastore

 -gcloud-storage

 -Lars wrote a blog post


 -bluebird promises
 -change your current http request set up
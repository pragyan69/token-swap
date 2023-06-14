1. first we will create the function to sign in to metamask for the sign in button



// creating the connect function

async function connect (){
    if( typeof window.ethereum != undefined){
        // now put the if part under try and catch

        try{
            console.log("connecting");
            await ethereum.request({method: 'eth_request_Accounts'})

        }
        catch(e){
          console.log(e);
        }

    }
    else{
      document.getElementById("login_button").innerHTML = "Please install metamask"
    }
}
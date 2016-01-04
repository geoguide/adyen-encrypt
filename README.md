# adyen-encrypt

> An adyen encrypt library, written in ES2015 for React

    npm i -S adyen-encrypt

###### Constructor

`key` The public key string you can find in the Adyen customer area

`opts` An object containing optionals as described below

    import AdyenEncrypt from 'adyen-encrypt'
    
    const instance = AdyenEncrypt(key, {
      enableValidations: true,
      numberIgnoreNonNumeric: true,
      cvcIgnoreBins: '101,404'
    })
    
###### encrypt

`data` The object to encrypt

Returns the encrypted string

    instance.encrypt({
      number: '5555 4444 3333 1111',
      cvc: '737',
      expiryMonth: '06',
      expiryYear: '2016',
      holderName: 'Balthazar Gronon'
    })

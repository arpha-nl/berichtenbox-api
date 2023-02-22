# Berichtenbox API

With the Berichtenbox API organisations are able to send Berichtenbox messages to the central Berichtenbox system of the Dutch Government in the most secure and easy way possible. The Berichtenbox API is provided by the Arpha B.V. API Platform.

## OpenAPI specification

In this Git repository you will find the OpenAPI specification, you can also have a look at [berichtenbox.readme.io](https://berichtenbox.readme.io/) to discover and test the API.

## Request access

To be able to test the API yourself, you will have to [request access](https://www.berichtenbox.dev/testen/). Testing the API is free of costs.

## Example message

```
{
 "BerichtLeverancierID" : "00000003564624920000", // OIN (from the formal sender of this letter, for example municipality)
 "Berichten" : [
   {
     "BerichtID" : "7E9126B2-C661-4C0F-9E05-7B038906CCCF", // UUID-format
     "BerichtType" : "APIDEMO",  // max 8 chars
     "PublicatieDatum" : "2022-06-11T09:30:47Z", // optional, YYYY-MM-DDTHH:MM:SSZ
     "Onderwerp" : "Subject of the message", // max 50 chars
     "Berichttekst" : "Hi,\r\n\r\nThis is a message, sent with the Berichtenbox API.\r\n\r\nRegards,\r\nBBAPI\r\nhttps://www.berichtenbox.dev", // max 4000 chars
     "Referentie" : "BB API Demo", // optional, max 25 chars
     "GebruikerID" : "000000012", // valid BSN
     "Bijlagen" : [  // optional, max. 2 PDF attachments per message
       {
         "Inhoud" : "ZGl0aXNlZW5QREZiZXN0YW5k", //base64 encoded PDF, total file size of binary PDFs 500kB
         "Omschrijving" : "Filename", // description or filename of PDF, max 128 chars
         "Volgorde" : "1" // optional when sending 2 PDF's
       }
     ]
   }
 ]
}
```

## Need help?

Please contact us if you need any help with the API.
More information on [berichtenbox.dev](https://www.berichtenbox.dev/)

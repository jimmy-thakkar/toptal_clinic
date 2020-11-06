# toptal_clinic
GoogleCalenderoAuth.vfp is a visualforce page which is used to Connect to Google account and get an access code for Google Integration

GoogleCalenderApi.apxc is an apex class used as a controller in GoogleCalenderoAuth visualforce to callout the Google integration services

AppointmentTrigger.apxt is a trigger on Appointment__c object which will call the handler AppointmentTriggerHandler.apxc

AppointmentTriggerHandler.apxc is again an apex class used to book an event in Physician's google calender as well as sending an email to the Patient.

NOTE: 
- For managing the Access token for Google integration I have created a custom setting (GoogleCalenderInfo__c) to store Access Token
- I have created few labels
  - organizerEmail in which the organizer email (google email account to connect between SF and Google) has been mentioned.
  - clientSecret in which the client Secret key shared by google while configuring the calender api
  - consumerKey in which the consumer key shared by google while configuring the calender api

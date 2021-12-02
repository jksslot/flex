# flex
function doGet() {
  return HtmlService.createTemplateFromFile('index')
  .evaluate()
  .addMetaTag('viewport', 'width=device-width, initial-scale=1')
  .setXFrameOptionsMode(HtmlService.XFrameOptionsMode.ALLOWALL) 
}

function record(data){
  var jks = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet()
  jks.appendRow([new Date(),data.name1,data.name2,"'"+data.name3,data.name4,data.name5])
}

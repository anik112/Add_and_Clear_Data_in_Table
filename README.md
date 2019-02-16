# Add_and_Clear_Data_in_Table
Clear and add data in jTable


*First you make list object and get data from database.

// Make Same *java.util.List* object and put data in list using *get_all_company_information()* mathod.
// Here *CompanyInformation* is class. i make Company information List where i put lot of company_information
   object.
        
        List<CompanyInformation> informatiopnList= new CompanyInformation().get_all_company_information();
        
// Make *javax.swing.table.DefaultTableModel* object and get table model from my table.
        
        DefaultTableModel model= (DefaultTableModel) jTblShowCompanyInfo.getModel();
      
// Set table row=0.
      
        model.setRowCount(0);

// Make *Object* class array where i put my single data from list.

        Object[] row=new Object[2];
        
// Loop for set data in table
        
        for(int i=0; i<informatiopnList.size(); i++){
            row[0]=informatiopnList.get(i).getCompanyName(); // set row[0]=company name
            row[1]=informatiopnList.get(i).getAddress(); // set roe[1]=company address
            
            model.addRow(row); // add row in table
        }
        
        
    
// get cruent date from windows
    
    private final Calendar calendar = Calendar.getInstance(); // get clender format
    private final java.sql.Date processDate = new java.sql.Date(calendar.getTime().getTime()); // get cruent date

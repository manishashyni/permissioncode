# permissioncode

package p1;
import java.io.File;
import java.io.IOException;

public class FolderCreation {

	public static void main(String args[]) throws IOException {
        boolean success = false;
       // boolean s;
    
      Runtime.getRuntime().exec("net use p: \\\\ad.infosys.com\\storage\\gec\\TRAINEE\\HANDSON\\Sandeep_forToolTesting\\");
     // File f = new File("\\\\ad.infosys.com\\storage\\gec\\TRAINEE\\HANDSON\\Sandeep_forToolTesting\\xy4");
      File f = new File("p:\\xy"); 
      {
  if (f.exists()) {
      System.out.println("File already exists");

  } else {
      System.out.println("No such file exists, creating now");
     
			success = f.mkdir();
			System.out.println(success);
			
	//	Runtime.getRuntime().exec("icalcls  \\\\ad.infosys.com\\storage\\gec\\TRAINEE\\HANDSON\\Sandeep_forToolTesting\\xy4/deny Everyone:R");
		Runtime.getRuntime().exec("icalcls p:\\xy /deny Everyone:R");
		
		}
      if (success) {
          System.out.printf("Successfully created new file: %s%n", f);
      } else {
          System.out.printf("Failed to create new file: %s%n", f);
      }
  }
        }
	

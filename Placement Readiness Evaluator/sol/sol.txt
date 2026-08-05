
public class Main {

    public static void main(String[] args) {
        String name = "Ananaya";
        double academicPercentage = 72.5;
        int attendancePercentage = 75;
        int activeBacklogs = 0;
        boolean projectCompleted = true;
        int communicationScore = 68;
        int aptitudeScore = 64;
        boolean academicStatus = academicPercentage >= 60;
        boolean attendanceStatus = attendancePercentage >= 75;
        boolean backlogStatus = activeBacklogs == 0;
        boolean projectStatus = projectCompleted == true;
        boolean communicationStatus = communicationScore >= 60;
        boolean aptitudeStatus = aptitudeScore >= 60;
        String res1 = (academicStatus == true) ? "Eligible" : "Not Eligible";
        String res2 = (attendanceStatus == true) ? "Eligible" : "Not Eligible";
        String res3 = (backlogStatus == true) ? "Eligible" : "Not Eligible";
        String res4 = (projectStatus == true) ? "Completed" : "Not Completed";
        String res5 = (communicationStatus == true) ? "Eligible" : "Not Eligible";
        String res6 = (aptitudeStatus == true) ? "Eligible" : "Not Eligible";
        System.out.println("Student Name: " + name);
        System.out.println("Academic Status: " + res1);
        System.out.println("Attendance Status:  " + res2);
        System.out.println("Backlog Status: " + res3);
        System.out.println("Project Status: " + res4);
        System.out.println("Communication Status: " + res5);
        System.out.println("Aptitude Status: " + res6);

        if (academicStatus && attendanceStatus && backlogStatus && projectStatus && communicationStatus && aptitudeStatus) {
            System.out.println("Final Result: PLACEMENT READY");
            System.out.println("Message: All placement requirements are satisfied.");
        } else {

            System.out.println("Final Result: NOT PLACEMENT READY");
            System.out.println("Areas to Improve");
            while (!academicStatus && attendanceStatus && backlogStatus && projectStatus && communicationStatus && aptitudeStatus) {
                System.out.println("Academic");
            }
            if (!attendanceStatus) {
                System.out.println("Attendance");
            }
            if (!backlogStatus) {
                System.out.println("Backlog");
            }
            if (!projectStatus) {
                System.out.println("Project");
            }
            if (!communicationStatus) {
                System.out.println("Communication");
            }
            if (!aptitudeStatus) {
                System.out.println("Aptitude");
            }
        }
    }
}

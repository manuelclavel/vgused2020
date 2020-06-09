## BookingDemo

    
    import java.time.LocalTime;
    
    public class BookingDemo {
    	
	public static void main(String[] args) {
		
		LocalTime endTime = LocalTime.of(10,00);
		
		BadmintonCourt badminton = new BadmintonCourt();
		badminton.setEndTime(endTime);
		ZumbaClass zumba = new ZumbaClass();
		zumba.setEndTime(endTime);
		
		Booking[] bookings = {badminton,zumba};
	
	    }
	}
	
## Booking

    import java.time.LocalTime;
    
    public abstract class  Booking {
	private LocalTime startTime;
	private LocalTime endTime;
	
	public LocalTime getStartTime() {
		return startTime;
	}
	public void setStartTime(LocalTime startTime) {
		this.startTime = startTime;
	}
	public LocalTime getEndTime() {
		return endTime;
	}
	public void setEndTime(LocalTime endTime) {
		this.endTime = endTime;
	}
	
    }
	
## BadmintonCourt

    
    public class BadmintonCourt extends Booking {
	
	public void extendBooking(int minutes) {
		System.out.println("Booking has been extended for " + Integer.toString(minutes));
	}

    }
	
## ZumbaClass
    
    import java.time.LocalTime;

    public class ZumbaClass extends Booking {
	
	public void extendBooking(LocalTime time) {
		System.out.println("Booking has been extended until " + time.toString());
	}

    }



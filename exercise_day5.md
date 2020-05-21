## Base code

## Class: Booking
>package abstractfactory;
>
>public abstract class Booking {
>	//protected int price;
>
>}

## Class: ZumbaClass
>package abstractfactory;
>
>public abstract class ZumbaClass extends Booking {
>	
>}


## Class: BookingAbstractFactory
>package abstractfactory;
>
>public abstract class BookingAbstractFactory {
>	 private static final BD001Factory bd001 = new BD001Factory();
>	 // private static final BD002Factory bd002 = new BD002Factory();
> 
>	 static BookingAbstractFactory getFactory(SportCenter sportcenter) {
>        BookingAbstractFactory factory = null;
>        switch (sportcenter) {
>            case BD001:
>                factory = bd001;
>                break;
>           // case BD002:
>           //     factory = bd002;
>           //     break;
>        }
>        return factory;
>    }
>
>    public abstract ZumbaClass createZumbaClass();
>
>    // public abstract BadmintonCourt createBadmintonCourt();
>}

## Class: BD001Factory
>package abstractfactory;
>
>public class BD001Factory extends BookingAbstractFactory {
>
>	@Override
>	public ZumbaClass createZumbaClass() {
>		ZumbaClass zumbaclass = new BD001ZumbaClass();		
>		return zumbaclass;
>	}
>
>	//@Override
>	//public BadmintonCourt createBadmintonCourt() {
>	//	BadmintonCourt badmintoncourt = new BD001BadmintonCourt();
>	//	
>	//	return badmintoncourt;
>	//}
>}

## Class: BD001ZumbaClass
>package abstractfactory;
>
>public class BD001ZumbaClass extends ZumbaClass {
>	
>	public BD001ZumbaClass() {
>		//this.price = 100;
>	}
>
>}


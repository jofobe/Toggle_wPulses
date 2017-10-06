# Toggle_wPulses
Basic toggle functionality, but with added pusles

<CODE_START>
************

DIGITAL_INPUT tog;

DIGITAL_OUTPUT on_fb, off_fb, on_os, off_os;

INTEGER i;

Function FunTog()
{
	switch (i)
	{
		case (0):
		{
			on_fb = 1;
			off_fb = 0;
			pulse (100, on_os);
			i = 1;
		}
		
		case (1):
		{
			on_fb = 0;
			off_fb = 1;
			pulse (100, off_os);
			i = 0;
		}
	}	
}


PUSH tog
{
	FunTog();
}
 
 
function main()
{
	i=1;
	FunTog();
}

<CODE_END>
************

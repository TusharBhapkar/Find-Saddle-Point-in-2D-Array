# Find-Saddle-Point-in-2D-Array
Saddle point is point which is lowest in its raw and highest in its own column
int a[][]= {{1,2,3},
					{4,5,6},
					{7,8,9}};
		
		for (int i = 0; i < a.length; i++) {
			for (int j = 0; j < a.length; j++) {
				
				
				
				int element=a[i][j];
				boolean forRaws=true;
				for (int k = 0; k < a[i].length; k++)
				{
					if (element>a[i][k])
					{
						forRaws=false;
					}
				}
				
				boolean forColumns=true;
				for (int l = 0; l < a.length; l++) 
				{
					if (element<a[l][j])
					{
						forColumns=false;
					}
				}
				if (forColumns==true &&forRaws==true)
				{
					System.out.println("saddle point is:: "+a[i][j]);
				}
			}
		}

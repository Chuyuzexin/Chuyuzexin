<html>
<script>
N=0;
function move(n,source,destination,temp)
{
	if(n==1)
	{
		N++;
		document.writeln("move"+"from"+source+"to"+destination+"<br>");
		console.log("move"+"from"+source+"to"+destination);
	}
	else
	{
	move(n-1,source,temp,destination);
	move(1,source,destination,temp);
	move(n-1,temp,destination,source);
	}
}

move(7,1,2,3);//move 7 disks from 1 to 3 using 2 as temp storage
document.writeln("times of moving="+N);

</script>
</html>

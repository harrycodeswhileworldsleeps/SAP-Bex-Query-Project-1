# SAP-Bex-Query-Project-1

Business explorer query designer project. 

The data used here is from the sandbox system which has all the dummy data , hence , no real data is present in the infocube.
After logging in to the system , we can find the query designer.

![image](https://user-images.githubusercontent.com/94862735/204220976-f92bd53c-34ff-4d25-be3f-d9a39d63ffdb.png)

Here we have selected the info-provider , which is a datastore object with a datasource 0FI_GL_4 (standard datasource for general ledger) which can be chacked in the source system SAP
ECC with T code RSA6.

Scenario -> The client needs a report of material credit amount per vendor in a specific country within USA , MXC and others, we will be using a 
characteristic value variable with processing of manual entry default is USA.

First we are going to pick this local currency characteristic and put it in the filter block.
Right click and restrict it with a variable which has our options .

![image](https://user-images.githubusercontent.com/94862735/204222807-e8ff113d-e7b5-41fc-8833-8ba8a513d1cd.png)

Now let's move to the rows/columns space and start designing our query.
We will put the characteristics in row and key figures in column.

![image](https://user-images.githubusercontent.com/94862735/204223333-599ac916-8939-471e-8a72-17cea07c9bc9.png)

As we want the result to be at the vendor level , let's put the result in material/plant view.
Let's save and run the query.

![image](https://user-images.githubusercontent.com/94862735/204224053-f28deace-d9c3-4120-899e-a273c69ff10a.png)

![image](https://user-images.githubusercontent.com/94862735/204224215-9d382e77-97e3-43a9-8139-9ce2be39fb0d.png)

So here we can see the material for a particular vendor in USA which has multiple items , their credit amount is mentioned 
and the total can be seen at last. Comparision of materials can be seen in the graph.

Moreover , now we are going to have a selection made for the key figure for particular year 2016.

![image](https://user-images.githubusercontent.com/94862735/204483517-e0f399e9-878d-443d-92be-3632d25f8325.png)

Now let's create a formula field too that would contain the difference between credit amount all and credit amount 2016.

![image](https://user-images.githubusercontent.com/94862735/204484054-8ddba94f-6757-4ac3-a2ee-c211eb9374c1.png)

Both the selection and formula have keyfigure credit amount reference

Let's fire up the report on web now.

![image](https://user-images.githubusercontent.com/94862735/204485430-2092ca28-067f-4b1b-88cc-5c7b308802e5.png)

It works !.



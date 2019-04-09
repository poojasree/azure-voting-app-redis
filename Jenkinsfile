pipeline{
 agent any
 stages{
 stage('Deploy Application to AKS') 
	           {
	             agent any    
	             steps
	                  {
	                     withCredentials([azureServicePrincipal('AzureServicePriciple')]) {
                            
				            //sh 'az login --service-principal -u $AZURE_CLIENT_ID -p $AZURE_CLIENT_SECRET -t $AZURE_TENANT_ID'
	                         //sh 'az aks get-credentials --resource-group RG_MSDP1 --name MSDPaks1'
	                         sh 'az aks get-credentials --resource-group AKS --name AKS'
				            sh 'kubectl apply -f azure-vote-all-in-one-redis.yaml'
				            sh 'kubectl get svc'

	                         
	                     } 
	                         
	                         
	                        
	                  }             
	            }
	}}

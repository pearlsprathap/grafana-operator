This operator helps to create grafana with customized port number.

In any kubernetes cluster execute the below scripts,

Create a Custom Resource Definition (CRD)
	kubectl apply -f crd_grafana.yaml

Create an Operator handler or controller to manage the created CRD object
	operator_handler.py

Create a service account and role binding

	kubectl apply -f service_account.yaml
	kubectl apply -f service_account_binding.yaml

Create deployment for operator in the cluster

	kubectl apply -f grafana_operator.yaml


Create service

	kubectl apply -f grafana.yaml

Test the grafana from the port number specified in grafana.yaml from the public IP address.
# kubebot-slack




Setup

To run Kubebot on Slack, first you need to create a new bot user integration on Slack and get the token (See Slack bot users for more details).

Then you need to know the channel ids where you want to run the Kubebot. You can get them on https://slack.com/api/channels.list?token={REPLACE WITH YOUR TOKEN}

How to run it

Create a Secret

First, create a Kubernetes Secret to hold your sensitive information.

kubectl create secret generic kubebot --from-literal=token=<your_token_here> --from-literal=channel=<your_channel_id_here>

Create a kubebot Deployment

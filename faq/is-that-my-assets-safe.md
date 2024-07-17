# Is that my assets safe?

In general, both exchange and lending are build on multi-sig, so the security of multi-sig is the most important thing of service on bitcoin.

So, we need to answer two key question:

* May that platform be evil as part of the multi-sig?
  * The platform is doing a positive-sum game business which create value instead of stealing money from customers
  * The platform should be a company or doxed team which make sure that they will be punished if they do evil thing
  * The reputation history of the team better be good enough
* How the platform manage the platform part of multi-sig?
  * using MPC service to manage the keys
  * using [AWS AEE](https://aws.amazon.com/ec2/nitro/nitro-enclaves/) to manage the keys

How bitty make sure the multi-sig keys are safe:

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

&#x20;

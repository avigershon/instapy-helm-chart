kubectl -n default exec kafka-client-7c8c9bc967-cldq4 -- /usr/bin/kafka-topics --zookeeper kafka-zookeeper:2181 --list

kubectl -n default exec kafka-client-7c8c9bc967-cldq4 -- /usr/bin/kafka-topics --zookeeper kafka-zookeeper:2181 --topic test1 --create --partitions 1 --replication-factor 1

export 
kubectl -n default exec -ti kafka-client-7c8c9bc967-cldq4 -- /usr/bin/kafka-console-consumer --bootstrap-server kafka:9093 --topic test1 --consumer.config /etc/kafka/client-ssl.properties --from-beginning

kubectl -n default exec -ti kafka-client-7c8c9bc967-cldq4 -- /usr/bin/kafka-console-consumer --bootstrap-server a1bc910bab69211e88ff70abbd052e30-1949958049.us-east-1.elb.amazonaws.com:31090,a1bc5e551b69211e88ff70abbd052e30-884149231.us-east-1.elb.amazonaws.com:31091,a1bc1eeb9b69211e88ff70abbd052e30-1190865103.us-east-1.elb.amazonaws.com:31092 --topic test1 --consumer.config /etc/kafka/client-ssl.properties --from-beginning





kubectl -n default exec -ti kafka-client-7c8c9bc967-cldq4 -- /usr/bin/kafka-console-consumer --bootstrap-server a1bc910bab69211e88ff70abbd052e30-1044118569.us-east-1.elb.amazonaws.com:31090,a1bc5e551b69211e88ff70abbd052e30-2098514911.us-east-1.elb.amazonaws.com:31091,a1bc1eeb9b69211e88ff70abbd052e30-239504269.us-east-1.elb.amazonaws.com:31092 --topic test1 --consumer.config /etc/kafka/client-ssl.properties --from-beginning



kubectl -n default exec -ti kafka-client-7c8c9bc967-cldq4  -- /usr/bin/kafka-console-producer --broker-list a1bc910bab69211e88ff70abbd052e30-1044118569.us-east-1.elb.amazonaws.com:31090,a1bc5e551b69211e88ff70abbd052e30-2098514911.us-east-1.elb.amazonaws.com:31091,a1bc1eeb9b69211e88ff70abbd052e30-239504269.us-east-1.elb.amazonaws.com:31092 --topic test1 --producer.config /etc/kafka/client-ssl.properties

kubectl -n default exec -ti kafka-client-7c8c9bc967-cldq4 -- /usr/bin/kafka-console-consumer --bootstrap-server a1bc910bab69211e88ff70abbd052e30-1949958049.us-east-1.elb.amazonaws.com:31090,a1bc5e551b69211e88ff70abbd052e30-884149231.us-east-1.elb.amazonaws.com:31091,a1bc1eeb9b69211e88ff70abbd052e30-1190865103.us-east-1.elb.amazonaws.com:31092 --topic test1 --consumer.config /etc/kafka/client-ssl.properties --from-beginning


kubectl -n default exec -ti kafka-client-7c8c9bc967-cldq4 -- bash -c telnet a1bc910bab69211e88ff70abbd052e30-1949958049.us-east-1.elb.amazonaws.com 31090

telnet a1bc910bab69211e88ff70abbd052e30-1949958049.us-east-1.elb.amazonaws.com 31090

telnet a1bc910bab69211e88ff70abbd052e30-1044118569.us-east-1.elb.amazonaws.com 30505
a1bc910bab69211e88ff70abbd052e30-1044118569.us-east-1.elb.amazonaws.com:31090,a1bc5e551b69211e88ff70abbd052e30-2098514911.us-east-1.elb.amazonaws.com:31091,a1bc1eeb9b69211e88ff70abbd052e30-239504269.us-east-1.elb.amazonaws.com:31092

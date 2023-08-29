1. metrics 설치
2. docker run --name elasticsearch --network elk_network -p 127.0.0.1:9200:9200 -p 127.0.0.1:9300:9300 -e "discovery.type=single-node" docker.elastic.co/elasticsearch/elasticsearch:7.15.2
3. docker run -d --name kibana --network elk_network -p 5601:5601 -e "ELASTICSERCH_URL=http://elasticsearch:9200" docker.elastic.co/kibana/kibana:7.15.2
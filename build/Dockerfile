FROM redhat/ubi8:8.7 AS builder
RUN yum update -y && yum install -y jq && chmod +x /usr/bin/jq

FROM harness/delegate:22.12.77617 AS dep
COPY --from=builder /usr/bin/jq /usr/local/bin
RUN chmod +x /usr/local/bin/jq

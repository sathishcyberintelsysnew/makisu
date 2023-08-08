FROM alpine

CMD echo "This is not the correct one, with target"; exit 1;

FROM alpine:3.18.3 as second

CMD echo "This is the correct one, with target"; exit 0;

FROM alpine:3.18.3 as third

CMD echo "This is not the correct one, with target"; exit 1;

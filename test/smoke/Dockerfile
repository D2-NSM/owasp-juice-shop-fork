FROM alpine

RUN apk add curl

COPY smoke-test.sh smoke-test.sh

# Install shadow package which includes useradd
RUN apk --no-cache add shadow
# Create a non-root user
RUN useradd -m d2user
USER d2user

CMD ["sh", "smoke-test.sh", "http://app:3000"]
FROM benjose22/selenium_pytest_remote:v1.1
LABEL maintainer="Ben Jose" 
LABEL email="benjose22@gmail.com"
WORKDIR /entrypoint
COPY ./entrypoint.sh /entrypoint
RUN chmod +x /entrypoint/entrypoint.sh

ARG T_THREAD_COUNT=5
ENV THREAD_COUNT=$T_THREAD_COUNT
ARG T_ENABLE_PYTEST_CACHE=False
ENV ENABLE_PYTEST_CACHE=$T_ENABLE_PYTEST_CACHE
ARG T_ENABLE_ALLURE_REPORT=True
ENV ENABLE_ALLURE_REPORT=$T_ENABLE_ALLURE_REPORT
ARG T_ENABLE_MULTITHEAD=True
ENV ENABLE_MULTITHEAD=$T_ENABLE_MULTITHEAD

WORKDIR /src
ENTRYPOINT ["/entrypoint/entrypoint.sh"]
CMD ["--help"]
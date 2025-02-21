FROM public.ecr.aws/lambda/python:3.11

COPY requirements.txt ${LAMBDA_TASK_ROOT}


RUN pip install -r requirements.txt

COPY lambda_function.py ${LAMBDA_TASK_ROOT}
COPY db_manager.py ${LAMBDA_TASK_ROOT}
COPY deficiency_report.py ${LAMBDA_TASK_ROOT}
COPY s3_manager.py ${LAMBDA_TASK_ROOT}
COPY config.py ${LAMBDA_TASK_ROOT}


CMD [ "lambda_function.lambda_handler" ]

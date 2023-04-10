# AwsServerlessDemo

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 15.1.5.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
# serverless-demo

1. Crear una cuenta gratis por 1 año en https://aws.amazon.com/es/

2. Una vez creada la cuenta Generar token en la sección de [Security Credentials](https://us-east-1.console.aws.amazon.com/iamv2/home?region=us-east-1#/security_credentials) Access Key. Guárdalas para un paso mas adelante.

3. Bajar el código del repo.

4. Correr un npm i.

5. Setear el API key para que serverless pueda subir tu codigo: serverless config credentials --provider aws --key <##Llave generada en paso 2> --secret <## Secret generado en paso 2> -o

6. Correr un ng build.

7. Ir al serverless.yml y modificar el path de los archivos generados en el dist, si fuera necesario y guardar los cambios.

8. Correr el comando serverless deploy

9. Una vez publicada la infraestructura necesaria en AWS, correr el comando: serverless syncToS3

10. Para obtener el URl donde se esta hosteando tu Angular app, correr el comando: sls domainInfo

11. Navegar a tu URL para ver tu app corriendo en aws.

12. Si quieres reflejar cambios en tu código, haz los cambios, salvalos, corre el paso 6, luego el paso 9 y por ultimo el comando: serverless invalidateCloudFrontCache para actualizar el cache de aws y navega de nuevo a tu app.

13. Si quieres remover tu app de AWS, dirigete al [S3 bucket](https://s3.console.aws.amazon.com/s3/home?region=us-east-1) que creaste y vacíalo, luego puedes correr el comando: serverless remove.

# pmcalculator 
A simple process manager calculator that helps determine the correct values for child processes in PHP-FPM.

# Usage :v:

To find the correct process manager values, you can use the following command:
```bash
ps -eo size,pid,user,command --sort -size | awk '{ hr=$1/1024 ; printf("%13.2f Mb ",hr) } { for ( x=4 ; x<=NF ; x++ ) { printf("%s ",$x) } print "" }' | grep php-fpm
```

# License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

Demo: [https://www.damianoperri.it/public/phpCalculator/](https://www.damianoperri.it/public/phpCalculator/)

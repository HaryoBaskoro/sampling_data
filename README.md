# sampling_data
Tugas Sampling Data Git

## Code untuk mengambil data dari repository github
curl -L -O https://github.com/labusiam/dataset/raw/main/weather_data.xlsx

## Code untuk convert data excel based on sheet (weather_2014 & weather_2015)
in2csv weather_data.xlsx --sheet "weather_2014" > weather_2014.csv
In2csv weather_data.xlsx --sheet "weather_2015" > weather_2015.csv

## menggabungkan 2 file csv dan rename menjadi weather
csvstack weather_2014.csv weather_2015.csv > weather.csv
## menghapus file weather_data
rm weather_data.xlsx

## menampilkan view dari sample_weather dimana data diambil berdasarkan sampling 0.3
cat weather.csv | sample -r 0.3 > sample_weather.csv

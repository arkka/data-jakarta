# DATA JAKARTA

Jakarta curated and short-list datasets.

1. [General](#general)
    - [Administrative Area (2014)](#administrative-area-2014)
2. [Population / Demographics](#population---demographics)
    - [General Population (2014)](#general-Population-2014)
    - [Population Age Group (2013)](#population-age-group-2013)
    - [Population Density (2013)](#population-density-2013)
    - [Population Household (2013)](#population-household-2013)
    - [Population Jobs (2013)](#population-jobs-2013)
    - [Population Education (2013)](#population-education-2013)
    - [Income per Capita (2013)](#income-per-capita-2013)
3. [Building / Infrastructure](#building---infrastructure)
    - [Building Permit (2012)](#building-permit-1998-2012)

4. [Jakgo API](#jakgo-api)

## General
### Administrative Area (2014)
###### Datasets: [administrative-area.csv](./datasets/DATA-DKI-MENURUT-NOMOR-KODE-WILAYAH-TAHUN-2014.csv)
###### Source: [data.jakarta.go.id](http://data.jakarta.go.id/dataset/datadkimenurutnomorkodewilayah/resource/79acba1a-0f0f-4323-a6b4-f0fae0967ab7)
###### Fields:
| Fields | Column Name |
|--------| ----------- |
| year | `tahun` |
| province id | `nomor_provinsi` |
| province name | `nama_provinsi` |
| regency id | `nomor_kabupaten` |
| regency name | `nama_kabupaten` |
| district id | `nomor_kecamatan` |
| district name | `nama_kecamatan` |
| village id | `nomor_kelurahan` |
| village name | `nama_kelurahan` |

###### Administrative Level Structure

```
Provinsi (Province): DKI Jakarta
|-- Kabupaten (Regency): Jakarta Pusat
|   +-- Kecamatan (District): Setiabudi
|   |   +--- Kelurahan (Village): Guntur
```

## Population / Demographics
### General Population (2014)
###### Datasets: [DATA-DKI-MENURUT-PENDUDUK-TAHUN-2014.csv](./datasets/DATA-DKI-MENURUT-PENDUDUK-TAHUN-2014.csv)
###### Source: [data.jakarta.go.id](http://data.jakarta.go.id/dataset/datadkimenurutpenduduk)
###### Fields:
| Fields | Column Name | Unit |
|--------| ----------- | -----|
| year | `tahun` | |
| province name | `nama_provinsi` | |
| regency name | `nama_kabupaten` | |
| district id | `nama_kecamatan` | |
| village name | `name_kelurahan` | |
| Male - Indonesian | `laki-laki_wni` | |
| Female - Indonesian | `perempuan_wni` | |
| Male - Foreign | `laki-laki_wna` | |
| Female - Foreign | `perempuan_wna` | |


### Population Age Group (2013)
###### Datasets: [Penduduk-Menurut-Kelompok-Umur-dan-Jenis-Kelamin-Di-DKI-Jakarta-Tahun-2013.csv](/.datasets/Penduduk-Menurut-Kelompok-Umur-dan-Jenis-Kelamin-Di-DKI-Jakarta-Tahun-2013.csv)
###### Source: [data.jakarta.go.id](http://data.jakarta.go.id/dataset/pendudukmenurukelompokumurdanjeniskelamindkijakarta)
###### Fields:
| Fields | Column Name | Unit |
|--------| ----------- | -----|
| year | `tahun` | |
| age group | `kelompok_usia` | |
| total male | `jumlah_laki_laki` | |
| total female | `jumlah_perempuan` | |

### Population Density (2013)
###### Datasets: [dkikepadatankelurahan2013.csv](/.datasets/dkikepadatankelurahan2013.csv)
###### Source: [data.jakarta.go.id](http://data.jakarta.go.id/dataset/kepadatandluaswilayahperkelurahandkijakarta)
###### Fields:
| Fields | Column Name | Unit |
|--------| ----------- | -----|
| year | `tahun` | |
| regency name | `NAMA KABUPATEN` | |
| district name | `NAMA KECAMATAN` | |
| village name | `NAMA KELURAHAN` | |
| Area | `LUAS WILAYAH` | Km<sup>2</sup> |
| Area Density | `KEPADATAN` | population/Km<sup>2</sup> |

### Population Household (2013)
##### Datasets: [Jumlah-Kecamatan-Kelurahan-Rukun-Warga-Rukun-Tetangga-dan-Kepala-Keluarga-Menurut-Kabupaten-Atau-Kot.csv](./datasets/Jumlah-Kecamatan-Kelurahan-Rukun-Warga-Rukun-Tetangga-dan-Kepala-Keluarga-Menurut-Kabupaten-Atau-Kot.csv)
##### Source: [data.jakarta.go.id](http://data.jakarta.go.id/dataset/jumlahkecamatankelurahanrtrwdankkdkijakarta)
##### Fields:
| Fields | Column Name | Unit |
|--------| ----------- | -----|
| year | `tahun` | |
| regency name | `nama_kabkota` | |
| district name | `nama_kecamatan` | |
| number of village | `jumlah_kelurahan` | |
| number of community | `jumlah_rw` | |
| number of neighbourhood | `jumlah_rt` | |
| number of household | `jumlah_kk` | |

###### Administrative Level Structure (Detail to KK/Household)

```
Provinsi (Province): DKI Jakarta
|-- Kabupaten (Regency): Jakarta Pusat
|   +-- Kecamatan (District): Setiabudi
|   |   +--- Kelurahan (Village): Guntur
|   |   |    +-- Rukun Warga (Community): 05
|   |   |    |   +-- Rukun Tetangga (Neighbourhood): 003
|   |   |    |   |   +-- Kepala Keluarga (Household)

```


### Population Jobs (2013)
##### Datasets: [Penduduk-Yang-Bekerja-Lapangan-Pekerjaan-2013.csv](./datasets/Penduduk-Yang-Bekerja-Lapangan-Pekerjaan-2013.csv)
##### Source: [data.jakarta.go.id](http://data.jakarta.go.id/dataset/pendudukyangbekerjamenurutlapanganpekerjaanutamadkijakarta)
##### Fields:
| Fields | Column Name | Unit |
|--------| ----------- | -----|
| year | `tahun` | |
| type of industry | `lapangan_pekerjaan` | |
| male | `jumlah_lelaki` | |
| female | `jumlah_perempuan` | |

##### Industry list:
| Type of industry | Description |
|--------| ----------- |
| `Pertanian` | Agriculture |
| `Pertambangan Penggalian` | Mining and Quarrying |
| `Industri Pengolahan` | Processing Industry |
| `Listrik Gas Air Bersih` | Electricity Gas Water |
| `Konstruksi` | Construction |
| `Perdagangan Hotel dan Restoran` | Trade Hotel and Restaurant |
| `Transportasi Pergudangan dan Komunikasi` | Transportation Pergudangandan Communications |
| `Keuangan Perbankan & Jasa Perusahaan` | Banking & Financial Services Company |
| `Jasa-jasa` | Services |

### Population Education (2013)
##### Datasets: [Persentase-Penduduk-Yang-Berumur-10-Tahun-Ke-Atas-Menurut-Pendidikan-Tertinggi-Yang-Ditamatkan-Tahun.csv](./datasets/Persentase-Penduduk-Yang-Berumur-10-Tahun-Ke-Atas-Menurut-Pendidikan-Tertinggi-Yang-Ditamatkan-Tahun.csv)
##### Source: [data.jakarta.go.id](http://data.jakarta.go.id/dataset/persentasependidikanpendudukdkijakarta)
##### Fields:
| Fields | Column Name | Unit |
|--------| ----------- | -----|
| year | `tahun` | |
| education level | `jenis_pendidikan` | |
| percentage | `persentase` | |




### Income per Capita (2013)
##### Datasets: [processed-pendapatan-perkapita-jakarta-nasional-2006-2012.csv](./datasets/processed-pendapatan-perkapita-jakarta-nasional-2006-2012.csv)
##### Source: [data.jakarta.go.id](processed-pendapatan-perkapita-jakarta-nasional-2006-2012)
##### Fields:
| Fields | Column Name | Unit |
|--------| ----------- | -----|
| year | `tahun` | |
| income per capita (Jakarta) | `perkapita_jakarta` | Million Indonesia Rupiah (IDR) |
| income per capita (National) | `perkapita_nasional` | Million Indonesia Rupiah (IDR) |

> As reference, currency at 12 April 2016 EUR 1 = IDR 15028

## Building / Infrastructure

### Building Permit (1998-2012)
##### Datasets: [jumlahimbbangunandanluasbangunan19982012.csv](./datasets/jumlahimbbangunandanluasbangunan19982012.csv)
##### Source: [data.jakarta.go.id](http://data.jakarta.go.id/dataset/jumlahimbbangunandanluasbangunandkijakarta)
##### Fields:
| Fields | Column Name | Unit |
|--------| ----------- | -----|
| year | `tahun` | |
| number of permit | `imb` | |
| number of building | `bangunan` | |
| building area | `luas_bangunan` | |


## Jakgo API

Jakarta City Government has developed Jakgo API (Beta) to provide direct public access to their data with JSON and GeoJSON format.
See [Jakgo API Documentation](http://smartcity.jakarta.go.id/api/).

> API TOKEN: q06qb1eTOimT7sc9nMQfkzCKBYEzePXwYbWpEaEk

### Available Endpoints
- [Kota - City/Regency](http://smartcity.jakarta.go.id/api/#kota-get)
  - Example: [http://api-jakgo.fzlrhmn.com//api/v1/kota/3174?api_token=q06qb1eTOimT7sc9nMQfkzCKBYEzePXwYbWpEaEk&format=geojson](http://api-jakgo.fzlrhmn.com//api/v1/kota/3174?api_token=q06qb1eTOimT7sc9nMQfkzCKBYEzePXwYbWpEaEk&format=geojson)
- [Kecamatan - District](http://smartcity.jakarta.go.id/api/#kecamatan-get)
  - Example: [http://api-jakgo.fzlrhmn.com//api/v1/kecamatan/3175060?api_token=q06qb1eTOimT7sc9nMQfkzCKBYEzePXwYbWpEaEk&format=geojson](http://api-jakgo.fzlrhmn.com//api/v1/kecamatan/3175060?api_token=q06qb1eTOimT7sc9nMQfkzCKBYEzePXwYbWpEaEk&format=geojson)
- [Kelurahan - Village](http://smartcity.jakarta.go.id/api/#kelurahan-get)
  - Example: [http://api-jakgo.fzlrhmn.com//api/v1/kelurahan/3174020007?api_token=q06qb1eTOimT7sc9nMQfkzCKBYEzePXwYbWpEaEk&format=geojson](http://api-jakgo.fzlrhmn.com//api/v1/kelurahan/3174020007?api_token=q06qb1eTOimT7sc9nMQfkzCKBYEzePXwYbWpEaEk&format=geojson)
- [Rukun Warga - Community](http://smartcity.jakarta.go.id/api/#kelurahan-get)
  - Example: [http://api-jakgo.fzlrhmn.com//api/v1/rw/3174070005001000?api_token=q06qb1eTOimT7sc9nMQfkzCKBYEzePXwYbWpEaEk&format=geojson](http://api-jakgo.fzlrhmn.com//api/v1/rw/3174070005001000?api_token=q06qb1eTOimT7sc9nMQfkzCKBYEzePXwYbWpEaEk&format=geojson)
- [Pembuangan Sampah - Garbage Depot](http://smartcity.jakarta.go.id/api/#tempat-pembuangan-sampah-sementara-get)
- [Rumah Sakit Umum - General Hospital](http://smartcity.jakarta.go.id/api/#rumah-sakit-umum-get)
- [Rumah Sakit Khusus - Specialty Hospital](http://smartcity.jakarta.go.id/api/#rumah-sakit-khusus-get)
- [Puskesmas - Clinic](http://smartcity.jakarta.go.id/api/#puskesmas-get)
- [CCTV](http://smartcity.jakarta.go.id/api/#cctv-balitower-get)

### Parameters
Some reference for the API Endpoint parameters:

| Parameter | Description | Example |
|-----------| ----------- | --------|
| `kode_kota` | Regency/City Code | |
| `kode_kecamatan` | District Code | |
| `kode_kelurahan` | Village Code | |
| `kode_rw` | Community | |

### Response

Some example from Rukun Warga(RW) - Community Endpoint with parameter `3174070005001000`:
```
{
	type: "FeatureCollection",
	features: [{
		type: "Feature",
		properties: {
			kode_kota: 3174,
			nama_kota: "JAKARTA BARAT",
			kode_kecamatan: 3174070,
			nama_kecamatan: "CENGKARENG",
			kode_kelurahan: 3174070005,
			nama_kelurahan: "CENGKARENG TIMUR",
			kode_rw: 3174070005001000,
			nama_rw: "RW 01"
		},
		geometry: {
			type: "Polygon",
			coordinates: [
				[
					[
						106.73348514844, -6.1519110001687
					],
					[
						106.73344414835, -6.1521709995681
					],
					[
						106.73358714865, -6.1523289996598
					],
					[
						106.73357114881, -6.1524699998668
					],
					[
						106.73364214848, -6.1526170003505
					],
					[
						106.73407714876, -6.1527359995429
					],
					[
						106.73426114825, -6.1527860000501
					],
					[
						106.73422814853, -6.1530780000259
					],
					[
						106.73402815509, -6.1550089020611
					],
					[
						106.73401900002, -6.1550089999763
					],
					[
						106.73377450002, -6.1550584999763
					],
					[
						106.73352000002, -6.1551099999763
					],
					[
						106.73302100002, -6.1552239999764
					],
					[
						106.73247400002, -6.1552719999763
					],
					[
						106.73171200002, -6.1553299999763
					],
					[
						106.7314083307, -6.1553523858553
					],
					[
						106.73140000002, -6.1553529999764
					],
					[
						106.73091100002, -6.1551809999764
					],
					[
						106.72998171342, -6.1548659370337
					],
					[
						106.73015038945, -6.1539005172712
					],
					[
						106.7302533888, -6.1532645176195
					],
					[
						106.72990038961, -6.1531775172048
					],
					[
						106.72982000461, -6.1527168349902
					],
					[
						106.7300843891, -6.1527295172296
					],
					[
						106.73045896573, -6.1528376229341
					],
					[
						106.73056838894, -6.1523625173924
					],
					[
						106.73066462809, -6.151956633568
					],
					[
						106.73119114877, -6.1519959995919
					],
					[
						106.73146638898, -6.1520225412835
					],
					[
						106.73147114819, -6.151387000286
					],
					[
						106.73146138965, -6.1511875171664
					],
					[
						106.73146139415, -6.1509944848838
					],
					[
						106.73192205837, -6.1509820256761
					],
					[
						106.73192614849, -6.1509819995958
					],
					[
						106.73212114849, -6.1509990003797
					],
					[
						106.73251114849, -6.1510520001259
					],
					[
						106.73312814816, -6.1512029998947
					],
					[
						106.73334614832, -6.1512549995948
					],
					[
						106.73354314841, -6.1514460003089
					],
					[
						106.73353814818, -6.1516040004005
					],
					[
						106.73348514844, -6.1519110001687
					]
				]
			]
		}
	}]
}
```






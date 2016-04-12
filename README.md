# DATA JAKARTA

Jakarta curated datasets (with minor data cleaning).

1. [General](#general)
    - [Administrative Area (2014)](#administrative-area-2014)
2. [Population / Demographics](#population---demographics)
    - [General Population (2014)](#general-Population-(2014))
    - [Population Age Group (2013)](#population-age-group-(2013))
    - [Population Density (2013)](#population-density-(2013))
    - [Population Household (2013)](#population-household-(2013))
    - [Population Jobs (2013)](#population-jobs-(2013))
    - [Population Education (2013)](#population-education-(2013))
    - [Income per Capita (2013)](#income-per-capita-(2013))
3. [Infrastructure](#infrastructure)


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

## Infrastructure
### xxxxx (xxx)
##### Datasets: [xxx.csv](./datasets/xxxx.csv)
##### Source: [data.jakarta.go.id](xxxx)
##### Fields:
| Fields | Column Name | Unit |
|--------| ----------- | -----|
| year | `tahun` | |
| type of industry | `lapangan_pekerjaan` | |
| male | `jumlah_lelaki` | |
| female | `jumlah_perempuan` | |

###### Administrative Level Structure







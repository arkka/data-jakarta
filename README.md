# DATA JAKARTA

Jakarta curated datasets (with minor data cleaning).

1. [General](#general)
    - [Administrative Area (2014)](#Administrative-Area-(2014))
2. [Population / Demographics](#Population-/-Demographics)
    - [Population Density (2013)](#Population-Density-(2013))
3. [Infrastructures](#Infrastrctures)


## General
### Administrative Area (2014)
###### Datasets: [administrative-area.csv](/.datasets/DATA-DKI-MENURUT-NOMOR-KODE-WILAYAH-TAHUN-2014.csv)
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
|   |   +--- Keluarahan (Keluarahan): Guntur
```

## Population / Demographics
### General Population (2014)
###### Datasets: [DATA-DKI-MENURUT-PENDUDUK-TAHUN-2014.csv](/.datasets/DATA-DKI-MENURUT-PENDUDUK-TAHUN-2014.csv)
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










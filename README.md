# DATA JAKARTA

Jakarta curated datasets (with small data cleaning).

1. [General](#general)
    - [Administrative Area (2014)](#Administrative Area (2014))
2. [Population / Demographics](#Population-/-Demographics)
    - [Population Density (2013)](#Population Density (2013))
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
### Population Density (2013)
###### Datasets: [dkikepadatankelurahan2013.csv](/.datasets/dkikepadatankelurahan2013.csv)
###### Source: [data.jakarta.go.id](http://data.jakarta.go.id/dataset/kepadatandluaswilayahperkelurahandkijakarta)
###### Fields:
| Fields | Column Name | Unit |
|--------| ----------- | -----|
| year | `tahun` | |
| province name | `NAMA  PROVINSI` | |
| regency name | `NAMA KABUPATEN` | |
| district id | `NAMA KECAMATAN` | |
| Area | `LUAS WILAYAH` | Km<sup>2</sup>
| Area Density | `KEPADATAN` | population/Km<sup>2</sup>


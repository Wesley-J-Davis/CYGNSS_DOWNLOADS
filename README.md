This repository contains config files and run script to control the download of CYGNYSS soil moisture data while logging the process and sending alerts for failures.

Core file works as so:
#Download CYGNSS L3 soil-moisture granules with podaac-data-downloader.
#
# Usage:
#  download_cygnss_l3.sh --dest DIR --year YYYY [options]
#
# Required:
#  -d, --dest DIR           Local product root (for example, /data/CYGNSS_L3)
#  -y, --year YYYY          Year to download
#
# Options:
#  -m, --month MM            Limit to one month (default: all 12 months)
#  -c, --collection NAME     PO.DAAC collection short name (default: CYGNSS_L3_SOIL_MOISTURE_V3.2)
#  -e, --extensions REGEX    Filename regex to download (default: 36km.a32.d33.nc;
#                             the collection also serves a 9km grid, use ".nc" for both)
#  -n, --limit N              Max granules per month (useful for testing)
#      --dry-run             Search and list granules without downloading
#  -h, --help                Show this help
#
# Files land in DEST/Y<yyyy>/M<mm>

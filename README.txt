# Copyright (c) 2024  Cenk Sasmaztin <cenk@oxoonetworks.com>
# All rights reserved.
#
# Redistribution and use in source and binary forms, with or without
# modification, are permitted provided that the following conditions
# are met:
# 1. Redistributions of source code must retain the above copyright
#    notice, this list of conditions and the following disclaimer.
# 2. Redistributions in binary form must reproduce the above copyright
#    notice, this list of conditions and the following disclaimer in the
#    documentation and/or other materials provided with the distribution.
#
# THIS SOFTWARE IS PROVIDED BY THE AUTHOR AND CONTRIBUTORS ``AS IS'' AND
# ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
# IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
# ARE DISCLAIMED.  IN NO EVENT SHALL THE AUTHOR OR CONTRIBUTORS BE LIABLE
# FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
# DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS
# OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION)
# HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
# LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY
# OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF
# SUCH DAMAGE.


#Copyright (c) [2024] [Oxoo Networks LLC.]
# PURPOSE of this SCRIPT

# This code connects to a network device and retrieves the current working configuration.
#Then detects the changes made, creates a report with the change lines,
#and also backs up the new version of the configuration.
#



NTP Delay and Offset Test (ntp_test.py)
=======================================

ENGLISH
-------

A simple Python script to measure NTP (Network Time Protocol) round-trip delay and local clock offset using a remote NTP server.

FEATURES
- Connects to a remote NTP server (default: pool.ntp.org)
- Calculates:
  - Round-trip delay (ms)
  - Clock offset between system and NTP time (ms)
- Prints results to the terminal
- Shows warning if offset exceeds normal thresholds

REQUIREMENTS
- Python 3
- ntplib module

Install with:
pip install ntplib

Run the script:
python3 ntp_test.py

Sample Output:
[ NTP Test Started ]
Target NTP Server: pool.ntp.org
Local Time      : Mon Jun 23 02:46:01 2025
NTP Time        : Mon Jun 23 02:46:01 2025
Round Trip Delay: 26.695 ms
Clock Offset    : 13.531 ms

NOTES:
- Offset values over 100 ms may indicate synchronization issues.
- The script does not adjust your system clock.

TÜRKÇE
------

Basit bir Python betiği ile uzak bir NTP sunucusuna bağlanarak NTP (Ağ Zaman Protokolü) gecikmesi ve sistem saat sapması ölçümü yapılır.

ÖZELLİKLER
- Varsayılan olarak pool.ntp.org sunucusuna bağlanır
- Aşağıdaki değerleri hesaplar:
  - Gidiş-dönüş gecikmesi (ms)
  - Sistem saati ile NTP saati arasındaki fark (ms)
- Sonuçları terminalde gösterir
- Saat sapması eşikleri aşıldığında uyarı verir

GEREKSİNİMLER
- Python 3
- ntplib modülü

Kurulum:
pip install ntplib

Çalıştırmak için:
python3 ntp_test.py

Örnek Çıktı:
[ NTP Test Started ]
Target NTP Server: pool.ntp.org
Local Time      : Mon Jun 23 02:46:01 2025
NTP Time        : Mon Jun 23 02:46:01 2025
Round Trip Delay: 26.695 ms
Clock Offset    : 13.531 ms

NOTLAR:
- Saat sapması 100 ms üzerindeyse sistem saati senkronize olmayabilir.
- Bu betik sistem saatini değiştirmez, yalnızca ölçer.

# Analogue Video Specifications

[View the published documentation on GitHub Pages](https://simoninns.github.io/analogue-video-specifications/)

This repository collects useful specification and technical reference material for analogue television systems and LaserDisc formats, with coverage across PAL and NTSC workflows and related studio, interface, and disc-format standards.

## Documentation site

The repository includes an MkDocs Material configuration and a Nix flake for local preview and GitHub Pages publishing.

### Local preview

If you have Nix with flakes enabled:

```sh
nix develop path:. -c mkdocs serve
```

To produce a local build instead of running the preview server:

```sh
nix develop path:. -c mkdocs build --strict
```

The generated site is written to `site/`.

### Publishing

GitHub Actions publishes the site to GitHub Pages on pushes to the `main` branch and also supports manual runs through the Actions tab.

## Available specifications

### Television and video formats

- [ITU-R BT.1700 - Characteristics of composite video signals for conventional analogue television systems](docs/video_formats/BT-1700-E/BT-1700-E.md)  
	Defines composite analogue colour video signal characteristics used in production and programme interchange. Covers NTSC, PAL, and SECAM systems.

- [ITU-R BT.470-6 - Conventional television systems](docs/video_formats/BT-470-6-1998/BT-470-6-1998.md)  
	Summarises the basic characteristics of established conventional broadcast television systems, including line counts, timing, bandwidth, and signal levels. Covers 525-line and 625-line monochrome and colour systems, including NTSC, PAL, and SECAM variants.

- [ITU-R BT.601-5 - Studio encoding parameters of digital television for standard 4:3 and wide-screen 16:9 aspect ratios](docs/video_formats/BT-601-5-1995/BT-601-5-1995.md)  
	Defines digital component studio encoding parameters and sampling structures for television production. Covers both 525-line and 625-line systems in 4:3 and 16:9 formats.

- [CCIR Report 624-4 - Characteristics of television systems](docs/video_formats/BT-624-4-1990/BT-624-4-1990.md)  
	Reference report listing the operating characteristics of conventional monochrome and colour television systems in use at the time. Covers 525-line and 625-line systems, including NTSC, PAL, and SECAM families.

- [EBU Tech. 3213-E - Standard for chromaticity tolerances for studio monitors](docs/video_formats/EBU-Tech-3213-E/EBU-Tech-3213-E.md)  
	Specifies monitor phosphor chromaticity targets and tolerances to maintain consistent colour reproduction in broadcast environments. Focuses on 625-line/50-field studio systems used with PAL and SECAM.

- [EBU Tech. 3280-E - Specification of interfaces for 625-line digital PAL signals](docs/video_formats/EBU-Tech-3280-E/EBU-Tech-3280-E.md)  
	Defines parallel and serial interfaces for interconnecting equipment handling composite digital PAL video. Covers 625-line digital PAL systems.

- [SMPTE 170M-2004 - Composite analog video signal - NTSC for studio applications](docs/video_formats/SMPTE-170M-2004/SMPTE-170M-2004.md)  
	Specifies the studio composite analogue NTSC signal, including timing, levels, encoding, and colorimetry. Covers 525-line, 59.94-field, 4:3 NTSC studio applications.

- [SMPTE 244M-2003 - Bit-parallel digital interface for NTSC composite video signals](docs/video_formats/SMPTE-244M-2003/SMPTE-244M-2003.md)  
	Defines a bit-parallel digital interface and sampling structure for encoded NTSC composite video. Covers 525-line, 59.94 Hz NTSC systems sampled at four times colour subcarrier frequency.

- [SMPTE 272M-1994 - Formatting AES/EBU audio and auxiliary data into digital video ancillary data space](docs/video_formats/SMPTE-272M-1994/SMPTE-272M-1994.md)  
	Defines how AES/EBU digital audio, auxiliary data, and associated control information are mapped into the ancillary data space of serial digital video. Covers embedding of up to 16 audio channels in component and composite SDI streams.

### Video metadata

- [ANSI/CTA-608-E S-2019 - Line 21 Data Services](docs/video_metadata/ANSI-CTA-608-E-S-2019/ANSI-CTA-608-E-S-2019.md)  
	Specifies Line 21 closed captioning, text, and Extended Data Services (XDS) data formats, signal characteristics, packet definitions, encoder/decoder behavior, and related regulatory and implementation guidance.

- [EBU Tech. 3209 - Performance specification of equipment for E.B.U. insertion signals](docs/video_metadata/EBU-Tech-3209/EBU-Tech-3209.md)  
	Specifies generation, insertion, and erasure performance requirements for E.B.U. insertion test signals used in 625-line television systems.

- [IEC 60461:2010 - Time and control code](docs/video_metadata/IEC-60461-2010-Time-and-control-code/IEC-60461-2010-Time-and-control-code.md)  
	Specifies time address, flag bits, binary groups, and linear and vertical interval transport structures for time and control code across television, film, and audio systems.

- [ITU-R BT.1439-1 - Measurement methods applicable in the analogue television studio and the overall analogue television system](docs/video_metadata/R-REC-BT-1439-1-2006/R-REC-BT-1439-1-2006.md)  
	Defines baseband video parameter terminology, test signals, and measurement methods for monitoring analogue television studio and transmission chain performance.

- [ITU-T J.63 - Insertion of test signals in the field-blanking interval of monochrome and colour television signals](docs/video_metadata/T-REC-J-63-1990/T-REC-J-63-1990.md)  
	Recommends insertion test-signal structures and timing for 625-line and 525-line systems to support operational measurements during programme transmission.

- [Vertical Interval Test Signals - NTSC and PAL definitions](docs/video_metadata/VITS/index.md)  
	Documents [NTSC](docs/video_metadata/VITS/NTSC-VITS.md) and [PAL](docs/video_metadata/VITS/PAL-VITS.md) VITS waveforms, including NTC-7, FCC, VIRS, ITU, and UK national insertion test signals. The waveform diagrams are generated from YAML definitions in `resources/definitions/vits/` using `scripts/generate-vits-diagrams`.

### Teletext

- [Broadcast Teletext Specification 1976 - Joint BBC/IBA/BREMA specification for the UK Teletext system](docs/teletext/BBC-Broadcast-Teletext-1976/BBC-Broadcast-Teletext-1976.md)  
	Defines the Teletext system broadcast in the UK by the BBC and the Independent Television networks, as used by the Ceefax and Oracle services. Covers the data-line waveform, bit rate and timing within the field-blanking interval, Hamming-coded magazine, page and row addressing, page-header control bits and transmission sequencing, and the page display model including the alphanumerics and graphics character sets, display and background colour, double height, boxing, flash, conceal, and hold graphics.

- [ETSI EN 300 706 V1.2.1 - Enhanced Teletext specification](docs/teletext/ETSI-EN-300-706-2003/ETSI-EN-300-706-2003.md)  
	Specifies World System Teletext (CCIR System B) for 625-line, 50-field television systems, defining presentation Levels 1, 1.5, 2.5 and 3.5. Covers the data-line signalling and packet structure, odd parity, Hamming 8/4 and Hamming 24/18 error protection, page, magazine and service organisation, the coding of every packet type including X/26, X/27, X/28, M/29 and 8/30, spacing and non-spacing attributes, the colour map and side panels, objects, Dynamically Re-definable Character Sets (DRCS), the Latin, Cyrillic, Greek, Arabic and Hebrew character sets with their national option sub-sets, and the FLOF and TOP navigation systems.

- [ITU-R BT.653-3 - Teletext systems](docs/teletext/BT-653-3-1998/BT-653-3-1998.md)  
	Recommends four teletext systems (A, B, C and D) for use with the television systems of ITU-R BT.470, and describes them against a layered ISO reference model. Tabulates the essential elements of each system for both 625/50 and 525/60 television systems, including bit rate, data amplitude and positioning, framing and error protection, addressing and page classification, and lists the alphabet and character set repertoires along with the alphanumeric, mosaic, DRCS, geometric, photographic and musical source-coding modes.

### LaserDisc and Laservision

- [IEC 60856:1986 - Laservision PAL](docs/laserdisc/IEC-60856-1986-Laservision-PAL/IEC-60856-1986-Laservision-PAL.md)  
	Base mechanical, optical, and operational specification for prerecorded reflective optical videodiscs in the Laservision system. Covers 50 Hz, 625-line PAL-compatible LaserDisc media.

- [IEC 60856:1986 Amendment 1 - Laservision PAL](docs/laserdisc/IEC-60856-1986-Laservision-PAL-Amendment-1/IEC-60856-1986-Laservision-PAL-Amendment-1.md)  
	Adds push-pull radial differential tracking signal requirements to the PAL Laservision specification. Covers PAL LaserDisc tracking and measurement characteristics.

- [IEC 60856:1986 Amendment 2 - Laservision PAL](docs/laserdisc/IEC-60856-1986-Laservision-PAL-Amendment-2/IEC-60856-1986-Laservision-PAL-Amendment-2.md)  
	Updates PAL Laservision mechanical and optical requirements and adds provisions related to digital audio implementation. Covers PAL LaserDisc disc construction and extended format details.

- [IEC 60857:1986 - Laservision NTSC](docs/laserdisc/IEC-60857-1986-Laservision-NTSC/IEC-60857-1986-Laservision-NTSC.md)  
	Base mechanical, optical, and operational specification for prerecorded reflective optical videodiscs in the Laservision system. Covers 60 Hz, 525-line M/NTSC-compatible LaserDisc media.

- [IEC 60857:1986 Amendment 1 - Laservision NTSC](docs/laserdisc/IEC-60857-1986-Laservision-NTSC-Amendment-1/IEC-60857-1986-Laservision-NTSC-Amendment-1.md)  
	Adds push-pull radial differential tracking signal requirements to the NTSC Laservision specification. Covers NTSC LaserDisc tracking and measurement characteristics.

- [IEC 60857:1986 Amendment 2 - Laservision NTSC](docs/laserdisc/IEC-60857-1986-Laservision-NTSC-Amendment-2/IEC-60857-1986-Laservision-NTSC-Amendment-2.md)  
	Updates NTSC Laservision mechanical and optical requirements and adds provisions related to digital audio implementation. Covers NTSC LaserDisc disc construction and extended format details.

- [US 4,485,483 - FM stereophonic system incorporating companding of difference signal](docs/laserdisc/US4485483-2-FM-Stereophonic-System-Incorporating-Companding-of-Difference-Signal/us4485483.md)  
	Patent describing an FM stereophonic broadcasting system in which the L-R difference signal is compressed and carried on a quadrature-phased subcarrier alongside the conventional difference signal, then complementarily expanded at the receiver. Covers the composite baseband arrangement, transmitter and receiver block diagrams, and the resulting signal-to-noise and coverage improvements, while remaining compatible with existing monophonic and biphonic receivers.

### Compact Disc

- [ECMA-130 - Data interchange on read-only 120 mm optical data disks (CD-ROM)](docs/efm/ECMA-130/ECMA-130.md)  
	Specifies the mechanical, physical, and optical characteristics of read-only 120 mm optical data disks (CD-ROM), together with the recording format: sector structure, EDC/ECC, CIRC error correction, scrambling, and eight-to-fourteen (EFM) channel coding.

- [IEC 60908:1999 - Audio recording: Compact disc digital audio system](docs/efm/IEC-60908-1999/IEC-60908-1999.md)  
	Specifies the compact disc digital audio system: disc mechanical and optical parameters, high-frequency and tracking signals, eight-to-fourteen modulation (EFM), CIRC error correction, and the subcode control and display system including CD Graphics and CD TEXT modes.

### VHS

- [SMPTE 32M-2004 - Video Recording — 1/2-in Type H — Cassette, Tape and Records](docs/vhs/SMPTE-32M-2004/markdown.md)  
	Specifies cassette, tape, and recording characteristics for Type H helical-scan ½-in VHS video tape recorders, including SP, LP, and EP modes, optional FM audio, compact video cassette dimensions, and high-performance type H parameters. Covers 525-line, 59.94-field NTSC systems.

- [JVC Video Technical Guide VTG82063](docs/vhs/JVC-Video-Technical-Guide-VTG82063/index.md)  
	Technical guide covering VHS and S-VHS format operation, recording and playback systems, mechanism descriptions, servo and signal processing circuits, tuner and audio sections, and related service reference material.

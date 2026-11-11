# 7. Leveraging AWS Global Infrastructure

Beginner-friendly study notes for AWS Cloud Practitioner CLF-C02.

## Course videos covered

| Video | Topic | Duration |
|---|---|---:|
| 134 | Why Global Applications? | 6 min |
| 135–136 | Route 53 Overview + Hands On | 11 min |
| 137–138 | CloudFront Overview + Hands On | 11 min |
| 139 | S3 Transfer Acceleration | 2 min |
| 140 | AWS Global Accelerator | 5 min |
| 141 | AWS Outposts | 3 min |
| 142 | AWS Wavelength | 2 min |
| 143 | AWS Local Zones | 4 min |
| 144 | Global Applications Architecture | — |

## Folder guide

- `01-Why-Global-Applications.md` — why applications are deployed globally.
- `02-Route-53/` — DNS, records, routing policies and health checks.
- `03-CloudFront/` — CDN, edge locations and caching.
- `04-S3-Transfer-Acceleration.md` — faster long-distance uploads to S3.
- `05-AWS-Global-Accelerator.md` — fixed anycast IPs and AWS global network.
- `06-AWS-Outposts.md` — AWS infrastructure at your own location.
- `07-AWS-Wavelength.md` — applications close to 5G users.
- `08-AWS-Local-Zones.md` — AWS infrastructure near large cities.
- `Study-Resources/` — important notes, architecture examples, interview questions, hands-on labs and CLI examples.

## Recommended study order

1. Understand latency and why global applications are useful.
2. Learn DNS and Route 53.
3. Learn content delivery and CloudFront.
4. Compare S3 Transfer Acceleration with Global Accelerator.
5. Learn Outposts, Wavelength and Local Zones.
6. Revise the architecture examples and interview questions.

## Important reminder

A Region is a separate geographic area. An Availability Zone is an isolated location within a Region. An Edge Location is a point of presence used by services such as CloudFront to deliver content closer to users. These terms are related, but they are not interchangeable.

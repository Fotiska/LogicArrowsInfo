---
title: Расширенная кольцевая ячейка
icon: feed-issue-open
date: 2024-09-08
published: true
order: 99
---

Улучшенная кольцевая ячейка, может хранить более 1 байта в себе.
Второй тип ячеек, на данный момент самый компактный, позволяет хранить 1 байт в 8 стрелочках.
Байт в данном типе ячеек хранится с помощью кольца на 8/9 бит ( зависит от реализации ). При чтении байт достаётся из них, а при записи перезаписывается.
Есть 2 реализации ячеек:
- N Колец хранят по 8-9 бит на каждое. Синхронизация происходит при чтении и записи.
- N Колец хранит X байт. Синхронизация происходит при чтении и записи.

Примеры озу на данном типе ячеек:
==- 1 Килобайт | 2 Кольца по 8 Бит + Бит начала байта | От Gulg
[!file Скачать в виде txt](/static/schematics/ram/1kb_ring_2bpc_gulg/schematic.txt)
![Ячейка](/static/schematics/ram/1kb_ring_2bpc_gulg/cell.png)
![Полная память](/static/schematics/ram/1kb_ring_2bpc_gulg/full.png)
==- 256 Байт | 16 Колец по 16 Байт | От Gulg
[!file Скачать в виде txt](/static/schematics/ram/256b_ring_16bpc_fotis/schematic.txt)
![Ячейка](/static/schematics/ram/256b_ring_16bpc_fotis/cell.png)
![Полная память](/static/schematics/ram/256b_ring_16bpc_fotis/full.png)
===
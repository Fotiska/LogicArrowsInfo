---
title: Кольцевая ячейка
icon: sync
date: 2024-09-08
published: true
order: 99
---

Второй тип ячеек, на данный момент самый компактный, позволяет хранить 1 байт в 8 стрелочках.
Байт в данном типе ячеек хранится с помощью кольца на 8/9 бит ( зависит от реализации ). При чтении байт достаётся из них, а при записи перезаписывается.
Есть 2 типа ячеек:
- 2 Кольца, 1 кольцо для тайминга, 2 кольцо для самого байта, оба кольца по 8 бит. Синхронизация происходит при чтении.
- 1 Кольцо для байта но вместе с байтом идёт сигнал о начале/конце байта, это кольцо на 9 бит. Синхронизация происходит при чтении и записи.

==- Сравнение постоянной ячейки с кольцевой ячейкой ( без проводов )
![](/static/imgs/trigger_vs_ring.png)
===

Примеры озу на данном типе ячеек:
==- 256 Байт | 1 Кольцо по 8 Бит + Бит начала байта | От yndash
[!file Скачать в виде txt](/static/schematics/ram/256b_ring_1bpc_yndash/schematic.txt)
![Ячейка](/static/schematics/ram/256b_ring_1bpc_yndash/cell.png)
![Полная память](/static/schematics/ram/256b_ring_1bpc_yndash/full.png)
===
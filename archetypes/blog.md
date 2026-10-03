---
title: '{{ replace .File.ContentBaseName "-" " " | strings.TrimLeft "0123456789 " | title }}'
slug: '{{ .File.ContentBaseName | strings.TrimLeft "0123456789-" }}'
date: '{{ .Date }}'
draft: true
description: ""
categories:
  - Tecnologia
tags:
  -
---

---
date: '{{ .Date }}'
draft: true
title: '{{ replace .File.ContentBaseName "-" " " | title }}'
slug: '{{ .File.ContentBaseName }}'
description: ''
tags: []
categories: []
---

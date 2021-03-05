---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 61e38afcccccd6a96e92983d24442740351320ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016043"
---
# Get-AzProviderOperation

## SYNOPSIS
Azure RBAC를 사용하여 보안이 가능한 Azure 리소스 공급자에 대한 작업을 제공합니다.

## 구문

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
이 Get-AzProviderOperation Azure 리소스 공급자에 의해 노출되는 작업을 얻습니다.
작업을 구성하여 Azure RBAC에서 사용자 지정 역할을 만들 수 있습니다.
명령은 표시할 작업 세부 정보를 결정하는 작업 검색 문자열(가능한 와일드카드() 문자)를 입력으로 *합니다. Get-AzProviderOperation * 를 사용하여 모든 Azure 리소스 공급자에 대한 모든 작업을 얻습니다. Microsoft.Compute/Get-AzProviderOperation Microsoft.Compute* 리소스 공급자의 모든 작업을 얻습니다.

## 예제

### 예제 1: 모든 공급자에 대한 모든 작업 수행
```powershell
PS C:\> Get-AzProviderOperation *
```

### 예제 2: 특정 리소스 공급자에 대한 작업 얻기
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### 예제 3: 가상 머신에서 수행할 수 있는 모든 작업
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## 매개 변수

### -DefaultProfile
azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperationSearchString
작업 검색 문자열(와일드카드(*) 문자가 있는 경우)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation

## 참고 사항
키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포

## 관련 링크

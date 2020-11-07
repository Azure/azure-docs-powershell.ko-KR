---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: 51229c966c0e4c8b0ec74c3c940037aca5081b15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704008"
---
# Get-AzureRmProviderOperation

## SYNOPSIS
Azure RBAC를 사용 하 여 보안 할 수 있는 Azure resource provider에 대 한 작업을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
Get-AzureRmProviderOperation Azure 리소스 공급자가 제공 하는 작업을 가져옵니다.
Azure RBAC에서 사용자 지정 역할을 만들기 위해 작업을 구성할 수 있습니다.
명령이 표시할 작업 세부 정보를 결정 하는 작업 검색 문자열 (가능한 와일드 카드 (*) 문자)을 입력으로 사용 합니다.

Get-AzureRmProviderOperation *를 사용 하 여 모든 Azure 리소스 공급자에 대 한 모든 작업을 가져옵니다.

Microsoft. Compute/* Get-AzureRmProviderOperation를 사용 하 여 리소스 공급자의 모든 작업을 가져옵니다.

## 예제의

### 모든 공급자에 대 한 모든 작업 가져오기
```
PS C:\> Get-AzureRmProviderOperation *
```

### 특정 리소스 공급자에 대 한 작업 가져오기
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### 가상 컴퓨터에서 수행할 수 있는 모든 작업 가져오기
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperationSearchString
작업 검색 문자열 (와일드 카드 (*) 문자 사용 가능)

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 이름
' OperationSearchString ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.

## 출력

### Microsoft. PSResourceProviderOperation (.Resources)

## 상속자
키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포

## 관련 링크

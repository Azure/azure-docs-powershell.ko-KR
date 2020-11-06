---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
ms.openlocfilehash: a96d8d3d9025e473b5c08d84201fde2a10d8be34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537355"
---
# Get-AzureRmDataFactoryHub

## SYNOPSIS
Azure Data Factory의 허브에 대 한 정보를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByFactoryName (기본값)
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmDataFactoryHub** Cmdlet은 Azure Data Factory의 허브에 대 한 정보를 가져옵니다.
허브의 이름을 지정 하는 경우이 cmdlet은 해당 허브에 대 한 정보를 가져옵니다.
이름을 지정 하지 않으면이 cmdlet은 데이터 팩터리의 모든 허브에 대 한 정보를 가져옵니다.

## 예제의

### 예제 1: 모든 데이터 허브 가져오기
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

이 명령은 ADFResourceGroup 이라는 Azure 리소스 그룹의 모든 데이터 허브와 ADFDataFactory 이라는 data factory를 가져옵니다.

### 예제 2: 특정 데이터 허브 가져오기
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

이 명령은 ADFResourceGroup 이라는 Azure 리소스 그룹의 MyDataHub 라는 이름과 ADFDataFactory 이라는 data factory에 대 한 정보를 가져옵니다.

## 변수

### -DataFactory
**PSDataFactory** 개체를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 허브에 대 한 정보를 가져옵니다.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Data factory의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 허브에 대 한 정보를 가져옵니다.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
정보를 가져올 허브의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Azure 리소스 그룹의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 허브에 대 한 정보를 가져옵니다.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### DataFactories의 ' 1 [Microsoft Azure. PSHub] 목록입니다.

### DataFactories. PSHub/.

## 상속자
* 키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리

## 관련 링크

[새로운 AzureRmDataFactoryHub](./New-AzureRmDataFactoryHub.md)

[제거-AzureRmDataFactoryHub](./Remove-AzureRmDataFactoryHub.md)



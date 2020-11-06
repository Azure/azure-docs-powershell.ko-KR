---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 93ca812f726e036d195e83170153f7b2df4a2352
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536264"
---
# Get-AzureRmPowerBIWorkspaceCollection

## SYNOPSIS
Power BI 작업 영역 컬렉션을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ResourceGroupParameterSet
```
Get-AzureRmPowerBIWorkspaceCollection [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WorkspaceCollectionNameParameterSet
```
Get-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmPowerBIWorkspaceCollection** Cmdlet은 Azure 구독, 리소스 그룹 또는 컬렉션 이름에서 Power BI 작업 영역 컬렉션을 가져옵니다.

## 예제의

### 예제 1: 리소스 그룹의 모든 작업 영역 컬렉션 가져오기
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

이 명령은 ResourceGroup17 이라는 리소스 그룹에 속하는 작업 영역 컬렉션을 가져옵니다.

### 예제 2: 이름을 사용 하 여 작업 영역 컬렉션 가져오기
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

이 명령은 지정 된 리소스 그룹에서 WCN11 이라는 작업 영역 컬렉션을 가져옵니다.

## 변수

### -ResourceGroupName
이 cmdlet이 작업 영역 컬렉션을 가져오는 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WorkspaceCollectionName
이 cmdlet이 가져오는 Power BI workspace 컬렉션의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
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

### PSWorkspaceCollection. PowerBIEmbedded. *.

## 상속자

## 관련 링크

[새로운 AzureRmPowerBIWorkspaceCollection](./New-AzureRmPowerBIWorkspaceCollection.md)

[제거-AzureRmPowerBIWorkspaceCollection](./Remove-AzureRmPowerBIWorkspaceCollection.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: ac3a45f9e150d65829a222e75e7072c6a2bdcd1e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333645"
---
# Get-AzDataFactoryV2LinkedService

## SYNOPSIS
Data Factory의 연결된 서비스에 대한 정보를 얻습니다.

## 구문

### ByFactoryName(기본값)
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByResourceId
```
Get-AzDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
Get-AzDataFactoryV2LinkedService cmdlet은 Azure Data Factory의 연결된 서비스에 대한 정보를 얻습니다.
연결된 서비스의 이름을 지정하는 경우 이 cmdlet은 해당 연결된 서비스에 대한 정보를 얻습니다.
이름을 지정하지 않으면 이 cmdlet은 데이터 팩터리의 모든 연결된 서비스에 대한 정보를 얻습니다.

## 예제

### 예제 1: 모든 연결된 서비스에 대한 정보 얻기
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceHDIStorage
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

이 명령은 WikiADF라는 데이터 팩터리의 모든 연결된 서비스에 대한 정보를 구한 다음, 파이프라인 연산자를 사용하여 Format-List cmdlet에 연결된 서비스를 전달합니다.
이 Windows PowerShell 형식을 지정합니다.
자세한 내용은 서식 Get-Help 입력합니다.
다음 방법 중 하나를 사용할 수 있습니다.

### 예제 2: 특정 연결된 서비스에 대한 정보 얻기
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

이 명령은 WikiADF라는 데이터 팩터리에서 LinkedServiceCuratedWikiData라는 연결된 서비스에 대한 정보를 얻습니다.

### 예제 3: DataFactory 매개 변수를 지정하여 특정 연결된 서비스에 대한 정보 얻습니다.
```
PS C:\>$DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

첫 번째 명령은 Get-AzDataFactoryV2 cmdlet을 사용하여 ContosoFactory라는 데이터 팩터리를 한 다음, $DataFactory 변수에 저장합니다.
두 번째 명령은 파이프라인 연산자를 사용하여 $DataFactory 데이터 팩터리에 대한 연결된 서비스에 대한 정보를 Format-Table cmdlet에 전달합니다.
이 Format-Table cmdlet은 지정된 속성을 데이터 세트 열로 사용하여 출력을 데이터 세트로 포맷합니다.

## PARAMETERS

### -DataFactory
PSDataFactory 개체를 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 연결된 서비스를 얻습니다.

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DataFactoryName
데이터 팩터리의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 속하는 연결된 서비스를 얻습니다.

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

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -Name
정보를 얻을 연결된 서비스의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Azure 리소스 그룹의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 연결된 서비스를 얻습니다.

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

### -ResourceId
Azure 리소스 ID입니다.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

### Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory

## 출력

### Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService

## 참고 사항
키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리

## 관련 링크

[Set-AzDataFactoryV2LinkedService]()

[Remove-AzDataFactoryV2LinkedService]()

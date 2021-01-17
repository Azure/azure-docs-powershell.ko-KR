---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 5988aed4ca0560daedc1470198e0b02975f18196
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385939"
---
# New-AzMlWebService

## SYNOPSIS
새 웹 서비스를 만듭니다.

## 구문

### CreateFromFile
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateFromInstance
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
기존 리소스 그룹에 Azure Machine Learning 웹 서비스를 만듭니다.
동일한 이름의 웹 서비스가 리소스 그룹에 있는 경우 호출은 업데이트 작업으로 작동하고 기존 웹 서비스를 덮어 덮어습니다.

## 예제

### 예제 1: Json 파일 기반 정의에서 새 서비스 만들기
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

참조된 json 파일에 있는 정의에 따라 "myresourcegroup" 그룹 및 미국 중남부 지역에 "mywebservicename"이라는 새 Azure Machine Learning 웹 서비스를 만듭니다.

### 예제 2: 개체 인스턴스에서 새 서비스 만들기
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

Import-AzMlWebService cmdlet을 사용하여 리소스로 게시하기 전에 사용자 지정할 웹 서비스 개체 인스턴스를 얻을 수 있습니다.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -DefinitionFile
웹 서비스의 JSON 형식 정의를 포함하는 파일의 경로를 지정합니다.
웹 서비스 정의에 대한 최신 사양은 아래 swagger 사양에서 찾을 수 https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning 있습니다.

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
확인을 요청하지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
웹 서비스의 지역입니다.
Azure 데이터 센터 지역(예: "미국 서부" 또는 "동남 아시아")을 입력합니다.
해당 유형의 리소스를 지원하는 모든 지역에 웹 서비스를 사용할 수 있습니다.
웹 서비스는 Azure 구독 또는 해당 리소스 그룹과 동일한 지역에 있을 수 없습니다.
리소스 그룹은 다른 지역의 웹 서비스를 포함할 수 있습니다.
각 리소스 종류를 지원하는 지역을 결정하기 위해 ProviderNamespace 매개 Get-AzResourceProvider cmdlet과 함께 다음을 사용합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
웹 서비스의 이름입니다.
이름은 리소스 그룹에서 고유해야 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewWebServiceDefinition
서비스를 만드는 모든 속성을 포함하는 새 웹 서비스에 대한 정의입니다.
이 매개 변수는 필수로, Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService 클래스의 인스턴스를 나타냈습니다.
웹 서비스 정의에 대한 최신 사양은 아래 swagger 사양에서 찾을 수 https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json 있습니다.

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
웹 서비스를 두는 리소스 그룹입니다.
Azure 데이터 센터 지역(예: "미국 서부" 또는 "동남 아시아")을 입력합니다.
해당 유형의 리소스를 지원하는 모든 지역에 웹 서비스를 사용할 수 있습니다.
웹 서비스는 Azure 구독 또는 해당 리소스 그룹과 동일한 지역에 있을 수 없습니다.
리소스 그룹은 다른 지역의 웹 서비스를 포함할 수 있습니다.
각 리소스 종류를 지원하는 지역을 결정하기 위해 ProviderNamespace 매개 Get-AzResourceProvider cmdlet과 함께 다음을 사용합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## 출력

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## 참고 사항
키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 기계, 기계 학습, azureml

## 관련 링크

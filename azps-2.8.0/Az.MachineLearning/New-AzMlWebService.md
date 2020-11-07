---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 325888f510f967f93aca5b3ef50294dd83971213
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689429"
---
# New-AzMlWebService

## SYNOPSIS
새 웹 서비스를 만듭니다.

## 구문과

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

## 설명은
기존 리소스 그룹에 Azure 기계 학습 웹 서비스를 만듭니다.
리소스 그룹에 같은 이름의 웹 서비스가 있으면 해당 호출이 업데이트 작업으로 작동 하 고 기존 웹 서비스를 덮어씁니다.

## 예제의

### 예제 1: Json 파일 기반 정의에서 새 서비스 만들기
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

참조 된 json 파일에 있는 정의에 따라 "myresourcegroup" 그룹 및 미국 중앙 US 지역에 "mywebservicename" 이라는 새 Azure 기계 학습 웹 서비스를 만듭니다.

### 예제 2: 개체 인스턴스에서 새 서비스 만들기
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

Import-AzMlWebService cmdlet을 사용 하 여 리소스로 게시 하기 전에 웹 서비스 개체 인스턴스를 가져와 사용자 지정할 수 있습니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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
웹 서비스의 JSON 형식 정의를 포함 하는 파일에 대 한 경로를 지정 합니다.
의 swagger 사양에는 웹 서비스 정의에 대 한 최신 사양이 나와 있습니다 https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .

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
확인 메시지를 표시 하지 않습니다.

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

### -위치
웹 서비스의 영역입니다.
Azure 데이터 센터 지역 (예: "경기도 US" 또는 "동남 아시아")을 입력 합니다.
해당 형식의 리소스를 지 원하는 모든 지역에 웹 서비스를 배치할 수 있습니다.
웹 서비스는 Azure 구독 또는 리소스 그룹과 동일한 지역에 있을 필요가 없습니다.
리소스 그룹에는 다른 지역의 웹 서비스가 포함 될 수 있습니다.
각 리소스 형식을 지 원하는 영역을 확인 하려면 ProviderNamespace 매개 변수 cmdlet이 포함 된 Get-AzResourceProvider를 사용 합니다.

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

### -이름
웹 서비스의 이름입니다.
이름은 리소스 그룹에서 고유 해야 합니다.

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
서비스를 만드는 모든 속성이 포함 된 새 웹 서비스에 대 한 정의입니다.
이 매개 변수는 필수 이며 WebServices 클래스의 인스턴스를 나타냅니다. MachineLearning.
의 swagger 사양에는 웹 서비스 정의에 대 한 최신 사양이 나와 있습니다 https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .

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
웹 서비스를 배치할 리소스 그룹입니다.
Azure 데이터 센터 지역 (예: "경기도 US" 또는 "동남 아시아")을 입력 합니다.
해당 형식의 리소스를 지 원하는 모든 지역에 웹 서비스를 배치할 수 있습니다.
웹 서비스는 Azure 구독 또는 리소스 그룹과 동일한 지역에 있을 필요가 없습니다.
리소스 그룹에는 다른 지역의 웹 서비스가 포함 될 수 있습니다.
각 리소스 형식을 지 원하는 영역을 확인 하려면 ProviderNamespace 매개 변수 cmdlet이 포함 된 Get-AzResourceProvider를 사용 합니다.

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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### MachineLearning. WebServices의 웹 서비스

## 출력

### MachineLearning. WebServices의 웹 서비스

## 상속자
키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml

## 관련 링크

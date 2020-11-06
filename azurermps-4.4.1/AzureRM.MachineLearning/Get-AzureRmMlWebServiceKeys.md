---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: 694ac928d78cf64f500730c57e394a8e3a425456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537135"
---
# Get-AzureRmMlWebServiceKeys

## SYNOPSIS
웹 서비스의 키를 검색 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### 이름과 리소스 그룹이 지정 된 Azure ML 웹 서비스의 선택 키를 가져옵니다.
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 지정 된 웹 서비스 인스턴스에 대 한 access kesy를 가져옵니다.
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
Azure 기계 학습 웹 서비스의 런타임 Api에 대 한 선택 키를 가져옵니다.

## 예제의

### --------------------------예제 1-리소스 그룹 및 이름으로 지정 된 웹 서비스의 키 가져오기--------------------------
@ {paragraph = PS C: \\ \> }





```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### --------------------------예제 2-웹 서비스 인스턴스에 대 한 키 가져오기--------------------------
@ {paragraph = PS C: \\ \> }





```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

$mlService는 MachineLearning WebServices. i a m .와 같은 개체를 입력 합니다.

## 변수

### -MlWebService
선택 키가 검색 되는 웹 서비스의 이름입니다.

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Get the access kesy for the given web service instance.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -이름
선택 키가 검색 되는 웹 서비스의 이름입니다.

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
웹 서비스의 리소스 그룹입니다.

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### 용
' MlWebService ' 매개 변수는 파이프라인에서 ' WebService ' 형식의 값을 허용 합니다.

## 출력

### 않아야

## 상속자
키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml

## 관련 링크


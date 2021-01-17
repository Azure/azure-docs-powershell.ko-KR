---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: be34a81e28f2a11ed604afe922694872fedb5f0a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386023"
---
# Get-AzMlWebService

## SYNOPSIS
하나 이상의 웹 서비스에 대한 요약 정보를 검색합니다.

## 구문

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
웹 서비스 정의 정보를 검색합니다.
전달된 매개 변수에 따라 cmdlet은 특정 웹 서비스에 대한 정의, 현재 구독 내의 지정된 리소스 그룹에 대한 웹 서비스에 대한 정의 컬렉션 또는 현재 구독 내의 웹 서비스에 대한 정의 컬렉션을 반환합니다.

## 예제

### 예제 1: 특정 웹 서비스의 세부 정보 확인
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### 예제 2: 현재 구독의 모든 웹 서비스 리소스 얻기
```
Get-AzMlWebService
```

### 예제 3: 현재 구독 및 주어진 리소스 그룹의 모든 웹 서비스 얻기
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

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

### -Name
세부 정보를 검색할 웹 서비스의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Region
지역 이름

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
웹 서비스에 대한 세부 정보를 검색할 리소스 그룹입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### 없음

## 출력

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## 참고 사항
키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 기계, 기계 학습, azureml

## 관련 링크

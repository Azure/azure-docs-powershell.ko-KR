---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsamplingsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
ms.openlocfilehash: 2658e1af1865668adfa865cfc0bc7f09c7340251
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217091"
---
# New-AzApiManagementSamplingSetting

## SYNOPSIS
진단에 대 한 새 샘플링 설정 만들기

## 구문과

```
New-AzApiManagementSamplingSetting [-SamplingType <String>] [-SamplingPercentage <Double>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
Cmdlet **AzApiManagementSamplingSetting** 는 진단에 대 한 새 샘플링 설정을 만듭니다.

## 예제의

### 예제 1: 기본 샘플링 설정 만들기
```powershell
PS C:\> New-AzApiManagementSamplingSetting -SamplingType fixed -Percentage 100

SamplingType Percentage
------------ ----------
fixed               100
```

`Fixed`요청/응답의 100%에 대 한 로깅을 사용 하 여 유형의 샘플링 설정을 만듭니다.

### 예제 2

진단에 대 한 새 샘플링 설정을 만듭니다. 생성

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementSamplingSetting -SamplingPercentage 100 -SamplingType fixed
```

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -SamplingPercentage
고정 요금 샘플링에 대 한 샘플링 비율입니다. 이 매개 변수는 선택 사항입니다.

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SamplingType
표본 집단의 유형입니다.
이 매개 변수는 선택 사항입니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### 않아야

## 출력

### ApiManagement. ServiceManagement. \ PsApiManagementSamplingSetting

## 상속자

## 관련 링크

[Get-AzApiManagementDiagnostic](./Get-AzApiManagementDiagnostic.md)

[제거-AzApiManagementDiagnostic](./Remove-AzApiManagementDiagnostic.md)

[Set-AzApiManagementDiagnostic](./Set-AzApiManagementDiagnostic.md)

[새로운 AzApiManagementSamplingSetting](./New-AzApiManagementHttpMessageDiagnostic.md)

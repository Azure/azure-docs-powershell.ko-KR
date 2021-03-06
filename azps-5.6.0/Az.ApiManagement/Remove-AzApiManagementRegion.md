---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 2e6ae18054f7ad3e122169522d111adfe612b955
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010048"
---
# Remove-AzApiManagementRegion

## SYNOPSIS
PsApiManagement 인스턴스에서 기존 배포 지역을 제거합니다.

## 구문

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Remove-AzApiManagementRegion** cmdlet은 **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** 형식의 인스턴스를 **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement의** 추가Region 컬렉션에서 제거합니다. 
이 cmdlet은 배포 자체를 수정하지 않고 메모리 내 **PsApiManagement 인스턴스를** 업데이트합니다.
API Management의 배포를 업데이트하기 위해 수정된 **PsApiManagementInstance를** **Set-AzApiManagement** 에 전달합니다.

## 예제

### 예제 1: PsApiManagement 인스턴스에서 지역 제거
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

이 명령은 **PsApiManagement** 인스턴스에서 미국 동부라는 지역을 제거합니다.

### 예제 2: 일련의 명령을 사용하여 PsApiManagement 인스턴스에서 지역 제거
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

이 첫 번째 명령은 ContosoApi라는 Contoso라는 리소스 그룹에서 **PsApiManagement의** 인스턴스를 얻습니다.
그런 다음 최종 명령은 해당 인스턴스에서 미국 동부라는 지역을 제거한 다음 배포를 업데이트합니다.

## 매개 변수

### -ApiManagement
이 cmdlet에서 추가 배포 지역을 제거하는 **PsApiManagement** 인스턴스를 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile

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

### -Location
이 cmdlet이 제거한 지역의 위치를 지정합니다.
Api Management 서비스에 대해 지원되는 지역 사이에 새 배포 지역의 위치를 지정합니다.
유효한 위치를 얻게 Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | 여기서 {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object 위치

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

### System.String

## 출력

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## 참고 사항

## 관련 링크

[Add-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[Update-AzApiManagementRegion](./Update-AzApiManagementRegion.md)



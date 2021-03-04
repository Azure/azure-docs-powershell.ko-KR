---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: ce1183588458dc0213bff77493caf41a9b1d2766
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994639"
---
# Add-AzApiManagementRegion

## SYNOPSIS
PsApiManagement 인스턴스에 새 배포 지역을 추가합니다.

## 구문

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Add-AzApiManagementRegion** cmdlet은 **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement의** 제공된 인스턴스의 추가Regions 컬렉션에 **PsApiManagementRegion** 형식의 새 인스턴스를 추가합니다. 
이 cmdlet은 자체적으로 배포하지 않지만 메모리 내 **PsApiManagement** 인스턴스를 업데이트합니다.
API Management의 배포를 업데이트하기 위해 수정된 **PsApiManagement** 인스턴스를 Set-AzApiManagement로 전달합니다.

## 예제

### 예제 1: PsApiManagement 인스턴스에 새 배포 지역 추가
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

이 명령은 두 개의 프리미엄 SKU 단위와 미국 동부라는 지역을 **PsApiManagement 인스턴스에 추가합니다.**

### 예제 2: PsApiManagement 인스턴스에 새 배포 지역 추가 및 배포 업데이트
```powershell
PS C:\>$service = Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\>$service = Add-AzApiManagementRegion -ApiManagement $service -Location $secondarylocation -VirtualNetwork $additionalRegionVirtualNetwork
PS C:\>$service = Set-AzApiManagement -InputObject $service -PassThru
```

이 명령은 **PsApiManagement** 개체를, 미국 동부라는 지역에 대해 두 개의 프리미엄 SKU 단위를 추가한 다음 배포를 업데이트합니다.

## 매개 변수

### -ApiManagement
이 cmdlet에서 추가 배포 지역을 추가하는 **PsApiManagement** 인스턴스를 지정합니다.

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

### -Capacity
배포 지역의 SKU 용량을 지정합니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
Api Management 서비스에 대해 지원되는 지역 사이에 새 배포 지역의 위치를 지정합니다.
유효한 위치를 얻게 Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | 여기서 {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object 위치

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

### -Sku
배포 지역의 계층을 지정합니다.
유효한 값은: 
- 개발자
- 표준
- 프리미엄

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetwork
가상 네트워크 구성을 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## 출력

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## 참고 사항
* cmdlet은 파이프라인에 **업데이트된 PsApiManagement 인스턴스를** 작성합니다.

## 관련 링크

[Remove-AzApiManagementRegion](./Remove-AzApiManagementRegion.md)

[Update-AzApiManagementRegion](./Update-AzApiManagementRegion.md)

[Set-AzApiManagement](./Set-AzApiManagement.md)



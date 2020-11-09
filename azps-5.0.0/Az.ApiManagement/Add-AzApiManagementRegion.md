---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: 172bd1490b105b942dc706afe9440030d39d5c49
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307730"
---
# Add-AzApiManagementRegion

## SYNOPSIS
PsApiManagement 인스턴스에 새 배포 영역을 추가 합니다.

## 구문과

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzApiManagementRegion** Cmdlet은 **PsApiManagementRegion** 형식의 새 인스턴스를 **ApiManagement. PsApiManagement** 유형의 제공 된 **additionalregions** 컬렉션에 추가 합니다..
이 cmdlet은 자기 자신을 배포 하는 것이 아니라 메모리 내 **PsApiManagement** 인스턴스를 업데이트 합니다.
API Management의 배포를 업데이트 하려면 수정 된 **PsApiManagement** 인스턴스를 Set-AzApiManagement에 전달 합니다.

## 예제의

### 예제 1: PsApiManagement 인스턴스에 새 배포 영역 추가
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

이 명령은 2 개의 premium SKU 단위와 동부 US 라는 지역 번호를 **PsApiManagement** 인스턴스에 추가 합니다.

### 예제 2: PsApiManagement 인스턴스에 새 배포 영역 추가 후 배포 업데이트
```powershell
PS C:\>$service = Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\>$service = Add-AzApiManagementRegion -ApiManagement $service -Location $secondarylocation -VirtualNetwork $additionalRegionVirtualNetwork
PS C:\>$service = Set-AzApiManagement -InputObject $service -PassThru
```

이 명령은 **PsApiManagement** 개체를 가져오고 동부 US 이라는 지역에 대해 두 개의 premium SKU 단위를 추가한 다음 배포를 업데이트 합니다.

## 변수

### -ApiManagement
이 cmdlet이 추가 배포 영역을 추가 하는 **PsApiManagement** 인스턴스를 지정 합니다.

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

### 용량
배포 영역의 SKU 용량을 지정 합니다.

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

### -위치
Api Management 서비스에 대해 지원 되는 지역에서 새 배포 영역의 위치를 지정 합니다.
유효한 위치를 얻으려면 cmdlet Get-AzResourceProvider ProviderNamespace "ApiManagement" |을 (를) 사용 하세요. 여기서 {$ _. ResourceTypes [0]. ResourceTypeName-eq "서비스"} | Select-Object 위치

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
배포 영역의 계층을 지정 합니다.
유효한 값은 다음과 같습니다. 
- 디벨로퍼
- 표준이
- Premium

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
가상 네트워크 구성을 지정 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### ApiManagement. PsApiManagement/.

## 출력

### ApiManagement. PsApiManagement/.

## 상속자
* Cmdlet은 파이프라인에 업데이트 된 **PsApiManagement** 인스턴스를 씁니다.

## 관련 링크

[제거-AzApiManagementRegion](./Remove-AzApiManagementRegion.md)

[업데이트-AzApiManagementRegion](./Update-AzApiManagementRegion.md)

[Set-AzApiManagement](./Set-AzApiManagement.md)



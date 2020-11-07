---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: d6c97ac0fc948ba3ee4f86a2e657a1386c693f73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704041"
---
# Update-AzureRmApiManagementRegion

## SYNOPSIS
PsApiManagement 인스턴스에서 기존 배포 영역을 업데이트 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzureRmApiManagementRegion** Cmdlet은 ApiManagement. e **ApiManagement. PsApiManagement** 의 제공 된 인스턴스에 대 한 **additionalregions** 개체의 컬렉션에 있는 **PsApiManagementRegion** 형식의 기존 인스턴스를 업데이트 합니다.).
이 cmdlet은 모든 항목을 배포 하지는 않지만 메모리 내 **PsApiManagement** 인스턴스를 업데이트 합니다.
API Management의 배포를 업데이트 하려면 수정 된 **PsApiManagementInstance** 를 Update-AzureRmApiManagementDeployment cmdlet에 사용 합니다.

## 예제의

## 변수

### -ApiManagement
**PsApiManagement** 인스턴스를 지정 하 여의 기존 배포 영역을 업데이트 합니다.

```yaml
Type: PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### 용량
배포 영역의 새 SKU 용량 값을 지정 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -위치
업데이트할 배포 영역의 위치를 지정 합니다.

Api Management 서비스에 대해 지원 되는 지역에서 새 배포 영역의 위치를 지정 합니다.
유효한 위치를 얻으려면 cmdlet Get-AzureRmResourceProvider ProviderNamespace "ApiManagement" |을 (를) 사용 하세요. 여기서 {$ _. ResourceTypes [0]. ResourceTypeName-eq "서비스"} | Select-Object 위치

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sku
배포 영역의 새 계층 값을 지정 합니다.

유효한 값은 다음과 같습니다.

- 디벨로퍼
- 표준이
- Premium

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
배포 영역에 대 한 가상 네트워크 구성을 지정 합니다.
$Null를 전달 하면 해당 지역에 대 한 가상 네트워크 구성이 제거 됩니다.

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PsApiManagement
' ApiManagement ' 매개 변수는 파이프라인에서 ' PsApiManagement ' 형식의 값을 허용 합니다.

## 출력

### ApiManagement. PsApiManagement/.

## 상속자

## 관련 링크

[추가-AzureRmApiManagementRegion](./Add-AzureRmApiManagementRegion.md)

[제거-AzureRmApiManagementRegion](./Remove-AzureRmApiManagementRegion.md)

[업데이트-AzureRmApiManagementDeployment](./Update-AzureRmApiManagementDeployment.md)

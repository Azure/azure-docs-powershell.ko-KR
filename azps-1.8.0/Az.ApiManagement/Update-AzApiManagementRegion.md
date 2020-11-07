---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: fce2d356b7da56d2b93fa8634e737f96f54da178
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869302"
---
# Update-AzApiManagementRegion

## SYNOPSIS
PsApiManagement 인스턴스에서 기존 배포 영역을 업데이트 합니다.

## 구문과

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzApiManagementRegion** Cmdlet은 ApiManagement. e **ApiManagement. PsApiManagement** 의 제공 된 인스턴스에 대 한 **additionalregions** 개체의 컬렉션에 있는 **PsApiManagementRegion** 형식의 기존 인스턴스를 업데이트 합니다.).
이 cmdlet은 모든 항목을 배포 하지는 않지만 메모리 내 **PsApiManagement** 인스턴스를 업데이트 합니다.
API Management의 배포를 업데이트 하려면 수정 된 **PsApiManagementInstance** 를 Update-AzApiManagementDeployment cmdlet에 사용 합니다.

## 예제의

### 예제 1: PsApiManagement 인스턴스에서 추가 영역의 용량 증가
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium

# Set the ApiManagement service and Enable Msi idenity on the service
PS C:\>$updatedService = Set-AzApiManagement -InputObject $apimService -PassThru
```

이 명령은 중앙 미국 및 미국 중부의 국가를 포함 하는 API Management Premium SKU 서비스를 가져옵니다. 그런 다음 **업데이트-AzApiManagementRegion** 를 사용 하 여 북쪽 중앙 미국 지역의 용량을 2로 늘립니다. 다음 cmdlet Set-AzApiManagement는 구성 변경 사항을 Api Management 서비스에 적용 합니다.

## 변수

### -ApiManagement
**PsApiManagement** 인스턴스를 지정 하 여의 기존 배포 영역을 업데이트 합니다.

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
배포 영역의 새 SKU 용량 값을 지정 합니다.

```yaml
Type: System.Int32
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
업데이트할 배포 영역의 위치를 지정 합니다.
Api Management 서비스에 대해 지원 되는 지역에서 새 배포 영역의 위치를 지정 합니다.
유효한 위치를 얻으려면 cmdlet Get-AzResourceProvider ProviderNamespace "ApiManagement" |을 (를) 사용 하세요. 여기서 {$ _. ResourceTypes [0]. ResourceTypeName-eq "서비스"} | Select-Object 위치

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

### -Sku
배포 영역의 새 계층 값을 지정 합니다.
유효한 값은 다음과 같습니다.
- 디벨로퍼
- 표준이
- Premium

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

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
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
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

### ApiManagement. PsApiManagement/.

### System. 문자열

### ApiManagement. PsApiManagementSku/.

### 시스템. i i.

### ApiManagement. PsApiManagementVirtualNetwork/.

## 출력

### ApiManagement. PsApiManagement/.

## 상속자

## 관련 링크

[추가-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[제거-AzApiManagementRegion](./Remove-AzApiManagementRegion.md)

[업데이트-AzApiManagementDeployment](./Update-AzApiManagementDeployment.md)

---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: f8f0273ab624cd81488734f9b84debc045f6fed2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526360"
---
# Update-AzureRmApiManagementDeployment

## SYNOPSIS
API Management 서비스의 배포를 업데이트 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### UpdateSpecificService (기본값)
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### UpdateFromPsApiManagementInstance
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**업데이트 AzureRmApiManagementDeployment** CMDLET은 API Management 서비스의 현재 배포를 업데이트 합니다.

## 예제의

### 예제 1: ApiManagement 인스턴스의 배포 업데이트
```powershell
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

이 명령은 API Management 인스턴스의 배포를 세 가지 단위 용량 표준으로 업데이트 합니다.

### 예제 2: ApiManagement 인스턴스 가져오기 및 크기 조정
```powershell
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

이 예제에서는 Api Management 인스턴스를 가져오고, 5 개의 premium 단위로 크기를 조정 하 고, 프리미엄 영역에 3 단위를 추가로 추가 합니다.

### 예제 3: 업데이트 배포 (외부 VNET)
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

이 명령은 기존 API Management 배포를 업데이트 하 고 외부 *VpnType* 에 참가 합니다.

### 예제 4: 업데이트 배포 (내부 VNET)
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

이 명령은 기존 API Management 배포를 업데이트 하 고 내부 *VpnType* 에 참가 합니다.

## 변수

### -AdditionalRegions
Azure API Management의 추가 배포 영역을 지정 합니다.

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: UpdateSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApiManagement
배포 구성을 가져올 **PsApiManagement** 인스턴스를 지정 합니다.
인스턴스에 필요한 모든 변경 내용이 이미 있는 경우이 매개 변수를 사용 합니다.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: UpdateFromPsApiManagementInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### 용량
마스터 Azure API 관리 배포 영역의 SKU 용량을 지정 합니다.

```yaml
Type: System.Int32
Parameter Sets: UpdateSpecificService
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -위치
마스터 API 관리 배포 영역의 위치를 지정 합니다.
유효한 위치를 얻으려면 cmdlet Get-AzureRmResourceProvider ProviderNamespace "ApiManagement" |을 (를) 사용 하세요. 여기서 {$ _. ResourceTypes [0]. ResourceTypeName-eq "서비스"} | Select-Object 위치

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
이 cmdlet이 업데이트 하는 API 관리의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
작업 중인 항목을 나타내는 개체를 반환 합니다.
기본적으로이 cmdlet은 출력을 생성 하지 않습니다.

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

### -ResourceGroupName
API Management가 존재 하는 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sku
마스터 Azure API 관리 배포 영역의 계층을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 디벨로퍼
- 표준이
- Premium

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: UpdateSpecificService
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
마스터 Azure API 관리 배포 영역의 가상 네트워크 구성을 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: UpdateSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnType
API Management 배포의 가상 네트워크 유형을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 않아야.
API Management 구축은 가상 네트워크의 일부가 아닙니다.
이 값이 기본값입니다. 
- 내부.
API Management 배포에 외부 연결 가상 주소가 있습니다. 
- 내부용.
API Management 배포에 인트라넷 연결 가상 주소가 있습니다.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: UpdateSpecificService
Aliases:
Accepted values: None, External, Internal

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
매개 변수: ApiManagement (ByValue)

### System. 문자열

### ApiManagement. PsApiManagementSku/.

### 시스템. i i.

### ApiManagement. PsApiManagementVirtualNetwork/.

### ApiManagement. PsApiManagementVpnType/.

### System.webserver. IList ' 1 [[ApiManagement. PsApiManagementRegion, Microsoft azure. ApiManagement, Version = 6.1.2.0, Culture = 중립, PublicKeyToken = null]]

## 출력

### ApiManagement. PsApiManagement/.

## 상속자

## 관련 링크

[Get-AzureRmApiManagement](./Get-AzureRmApiManagement.md)



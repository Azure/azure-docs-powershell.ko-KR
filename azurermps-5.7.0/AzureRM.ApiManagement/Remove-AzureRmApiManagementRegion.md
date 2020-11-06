---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 0376c80e769153c448cdc23d8465966026584fcf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538091"
---
# Remove-AzureRmApiManagementRegion

## SYNOPSIS
PsApiManagement 인스턴스에서 기존 배포 영역을 제거 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmApiManagementRegion** Cmdlet은 ApiManagement의 인스턴스를 제공 하 고, **Additionalregions** 컬렉션에서 **PsApiManagementRegion** 형식의 인스턴스를 제거 합니다. **ApiManagement. PsApiManagement** 의 인스턴스가 있습니다.
이 cmdlet은 배포를 단독으로 수정 하지 않지만 메모리 내 **PsApiManagement** 인스턴스를 업데이트 합니다.
API Management의 배포를 업데이트 하려면 수정 된 **PsApiManagementInstance** 를 **update-AzureRmApiManagement** 에 전달 합니다.

## 예제의

### 예제 1: PsApiManagement 인스턴스에서 지역 제거
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

이 명령은 **PsApiManagement** 인스턴스에서 동부 라는 지역을 제거 합니다.

### 예제 2: 일련의 명령을 사용 하 여 PsApiManagement 인스턴스에서 지역 제거
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

첫 번째 명령은 ContosoApi 이라는 리소스 그룹에서 **PsApiManagement** 의 인스턴스를 가져옵니다.
마지막 명령은 해당 인스턴스에서 동부 라는 지역을 제거 하 고 배포를 업데이트 합니다.

## 변수

### -ApiManagement
이 cmdlet가 추가 배포 영역을 제거 하는 **PsApiManagement** 인스턴스를 지정 합니다.

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
이 cmdlet이 제거 하는 영역의 위치를 지정 합니다.

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

[업데이트-AzureRmApiManagementRegion](./Update-AzureRmApiManagementRegion.md)



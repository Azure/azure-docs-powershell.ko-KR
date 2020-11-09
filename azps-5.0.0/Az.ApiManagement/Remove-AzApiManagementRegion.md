---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 70816b054acc7667d2246ea72901c65890f9389e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307616"
---
# Remove-AzApiManagementRegion

## SYNOPSIS
PsApiManagement 인스턴스에서 기존 배포 영역을 제거 합니다.

## 구문과

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzApiManagementRegion** Cmdlet은 ApiManagement의 인스턴스를 제공 하 고, **Additionalregions** 컬렉션에서 **PsApiManagementRegion** 형식의 인스턴스를 제거 합니다. **ApiManagement. PsApiManagement** 의 인스턴스가 있습니다.
이 cmdlet은 배포를 단독으로 수정 하지 않지만 메모리 내 **PsApiManagement** 인스턴스를 업데이트 합니다.
API Management의 배포를 업데이트 하려면 수정 된 **PsApiManagementInstance** 를 **Set-AzApiManagement** 에 전달 합니다.

## 예제의

### 예제 1: PsApiManagement 인스턴스에서 지역 제거
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

이 명령은 **PsApiManagement** 인스턴스에서 동부 라는 지역을 제거 합니다.

### 예제 2: 일련의 명령을 사용 하 여 PsApiManagement 인스턴스에서 지역 제거
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

첫 번째 명령은 ContosoApi 이라는 리소스 그룹에서 **PsApiManagement** 의 인스턴스를 가져옵니다.
마지막 명령은 해당 인스턴스에서 동부 라는 지역을 제거 하 고 배포를 업데이트 합니다.

## 변수

### -ApiManagement
이 cmdlet가 추가 배포 영역을 제거 하는 **PsApiManagement** 인스턴스를 지정 합니다.

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

### -위치
이 cmdlet이 제거 하는 영역의 위치를 지정 합니다.
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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### ApiManagement. PsApiManagement/.

### System. 문자열

## 출력

### ApiManagement. PsApiManagement/.

## 상속자

## 관련 링크

[추가-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[업데이트-AzApiManagementRegion](./Update-AzApiManagementRegion.md)



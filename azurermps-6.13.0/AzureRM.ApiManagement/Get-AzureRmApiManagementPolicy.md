---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: fcf88fcb9b54adec01b8a04b50f557b6a74e7ca8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524751"
---
# Get-AzureRmApiManagementPolicy

## SYNOPSIS
지정 된 범위 정책을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### GetTenantLevel (기본값)
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Get제품 수준
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### GetApiLevel
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### GetOperationLevel
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmApiManagementPolicy** cmdlet은 지정 된 범위 정책을 가져옵니다.

## 예제의

### 예제 1: 테 넌 트 수준 정책 가져오기
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

이 명령은 테 넌 트 수준 정책을 가져와 tenantpolicy.xml 라는 파일에 저장 합니다.

### 예제 2: 제품 범위 정책 가져오기
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

이 명령은 제품 범위 정책을 가져옵니다.

### 예제 3: API 범위 정책 가져오기
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

이 명령은 API 범위 정책을 가져옵니다.

### 예제 4: 작업 범위 정책 가져오기
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

이 명령은 작업 범위 정책을 가져옵니다.

## 변수

### -ApiId
기존 API의 식별자를 지정 합니다.
이 매개 변수를 지정 하면 cmdlet이 API 범위 정책을 반환 합니다.

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApiRevision
API 개정판의 식별자입니다. 이 매개 변수는 선택 사항입니다. 지정 하지 않으면 현재 활성 api 개정판에서 정책이 검색 됩니다.

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -컨텍스트
**PsApiManagementContext** 의 인스턴스를 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
ps_force

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -형식
API 관리 정책의 형식을 지정 합니다.
이 매개 변수의 기본값은 "application/vnd. policy + xml"입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OperationId
기존 API 작업의 식별자를 지정 합니다.
*Apiid* 에이 매개 변수를 지정 하는 경우 cmdlet은 작업 범위 정책을 반환 합니다.

```yaml
Type: System.String
Parameter Sets: GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProductId
기존 제품의 식별자를 지정 합니다.
이 매개 변수를 지정 하는 경우 cmdlet은 제품 범위 정책을 반환 합니다.

```yaml
Type: System.String
Parameter Sets: GetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SaveAs
결과를 저장할 파일 경로를 지정 합니다.
이 매개 변수를 지정 하지 않으면 결과는 sting로 파이프라인 됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### ApiManagement. ServiceManagement. \ PsApiManagementContext

### System. 문자열

### System.webserver 매개 변수

## 출력

### System. 문자열

## 상속자

## 관련 링크

[제거-AzureRmApiManagementPolicy](./Remove-AzureRmApiManagementPolicy.md)

[Set-AzureRmApiManagementPolicy](./Set-AzureRmApiManagementPolicy.md)



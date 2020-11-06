---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 67cff03f8531ff71170fe565d5da411ca5b4f127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525403"
---
# Remove-AzureRmApiManagementPolicy

## SYNOPSIS
지정 된 범위에서 API 관리 정책을 제거 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### RemoveTenantLevel (기본값)
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Remove제품 수준
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveApiLevel
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveOperationLevel
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmApiManagementPolicy** cmdlet은 지정 된 범위에서 API 관리 정책을 제거 합니다.

## 예제의

### 예제 1: 테 넌 트 수준 정책 제거
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext
```

이 명령은 API Management에서 테 넌 트 수준 정책을 제거 합니다.

### 예제 2: 제품 범위 정책 제거
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

이 명령은 API Management에서 제품 범위 정책을 제거 합니다.

### 예제 3: API 범위 정책 제거
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

이 명령은 api 관리에서 API 범위 정책을 제거 합니다.

### 예제 4: 작업 범위 정책 제거
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

이 명령은 API Management에서 작업 범위 정책을 제거 합니다.

## 변수

### -ApiId
기존 API의 식별자를 지정 합니다.
이 매개 변수를 지정 하면 cmdlet이 API 범위 정책을 제거 합니다.

```yaml
Type: String
Parameter Sets: RemoveApiLevel, RemoveOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -컨텍스트
**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.

```yaml
Type: PsApiManagementContext
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

### -OperationId
기존 작업의 식별자를 지정 합니다.
*Apiid* 매개 변수를 사용 하 여이 매개 변수를 지정 하면이 cmdlet은 작업 범위 정책을 제거 합니다.

```yaml
Type: String
Parameter Sets: RemoveOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
이 cmdlet이 $True 값을 반환 하거나, 성공할 경우, $False의 값이 반환 됨을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProductId
기존 제품의 식별자를 지정 합니다.
이 매개 변수를 지정 하면 cmdlet이 제품 범위 정책을 제거 합니다.

```yaml
Type: String
Parameter Sets: RemoveProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### 나타내는

## 상속자

## 관련 링크

[Get-AzureRmApiManagementPolicy](./Get-AzureRmApiManagementPolicy.md)

[Set-AzureRmApiManagementPolicy](./Set-AzureRmApiManagementPolicy.md)



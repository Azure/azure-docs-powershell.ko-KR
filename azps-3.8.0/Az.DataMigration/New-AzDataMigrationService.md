---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
ms.openlocfilehash: c8e81cf727894adfa7378bbed996a1a476521148
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877553"
---
# New-AzDataMigrationService

## SYNOPSIS
Azure 데이터베이스 마이그레이션 서비스의 새 인스턴스를 만듭니다.

## 구문과

```
New-AzDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
New-AzDataMigrationService cmdlet은 Azure 데이터베이스 마이그레이션 서비스의 새 인스턴스를 만듭니다. 이 cmdlet은 기존 Azure 리소스 그룹의 이름, 만들려는 Azure Database 마이그레이션 서비스의 새 인스턴스에 대 한 고유 이름, 인스턴스가 프로 비전 된 지역, DMS 작업자 SKU의 이름, 서비스를 상주할 Azure 가상 서브넷의 이름에 적용 됩니다. 구독 이름에 대 한 매개 변수는 사용자가 Azure 로그인 세션의 기본 구독을 지정 하거나 Get-AzSubscription를 실행 하는 데 필요 하기 때문에 (SubscriptionName "MySubscription" |) 할 수 없습니다. 다른 구독을 선택 Select-AzSubscription.

## 예제의

### 예제 1
```
PS C:\> New-AzDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

위 예제에서는 중앙 US 지역에서 TestService 라는 Azure 데이터베이스 마이그레이션 서비스의 새 인스턴스를 만드는 방법을 보여 줍니다.

## 변수

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
만들 Azure 데이터베이스 마이그레이션 서비스 인스턴스의 위치 이며, Azure 지역에 해당 합니다.

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

### -이름
데이터베이스 마이그레이션 서비스 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름입니다.

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
Azure 데이터베이스 마이그레이션 서비스 인스턴스의 sku입니다. 사용할 수 있는 값은 현재 Basic_1vCore, Basic_2vCores GeneralPurpose_4vCores

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

### -VirtualSubnetId
Azure 데이터베이스 마이그레이션 서비스 인스턴스에 사용할 지정 된 가상 네트워크 아래 서브넷의 이름입니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService

## 상속자

## 관련 링크

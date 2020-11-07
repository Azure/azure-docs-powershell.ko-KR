---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: 46455cbf411228f008bdc15c27f78715ccea0e89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711175"
---
# New-AzureRmDataMigrationService

## SYNOPSIS
Azure 데이터베이스 마이그레이션 서비스의 새 인스턴스를 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Sku <String> -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>]
```

## 설명은
New-AzureRmDataMigrationService cmdlet은 Azure 데이터베이스 마이그레이션 서비스의 새 인스턴스를 만듭니다. 이 cmdlet은 기존 Azure 리소스 그룹의 이름, 만들려는 Azure Database 마이그레이션 서비스의 새 인스턴스에 대 한 고유 이름, 인스턴스가 프로 비전 된 지역, DMS 작업자 SKU의 이름, 서비스를 상주할 Azure 가상 서브넷의 이름에 적용 됩니다. 구독 이름에 대 한 매개 변수는 사용자가 Azure 로그인 세션의 기본 구독을 지정 하거나 실행 Get-AzureRmSubscription – SubscriptionName "MySubscription" | 다른 구독을 선택 Select-AzureRmSubscription.

## 예제의

### 예제 1
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -ServiceName TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

위 예제에서는 중앙 US 지역에서 TestService 라는 Azure 데이터베이스 마이그레이션 서비스의 새 인스턴스를 만드는 방법을 보여 줍니다.


## 변수

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
만들 Azure 데이터베이스 마이그레이션 서비스 인스턴스의 위치 이며, Azure 지역에 해당 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceName
Azure 데이터베이스 마이그레이션 서비스 인스턴스의 이름입니다.

```yaml
Type: String
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
Type: String
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
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## 출력

### Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService


## 상속자

## 관련 링크


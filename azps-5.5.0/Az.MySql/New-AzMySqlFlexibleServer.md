---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
ms.openlocfilehash: c544ce2ea5f02d5c0b3b7aee41e19992a0dc356d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192113"
---
# New-AzMySqlFlexibleServer

## SYNOPSIS
새 MySQL 유연한 서버를 만듭니다.

## 구문

```
New-AzMySqlFlexibleServer [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-AdministratorUserName <String>] [-BackupRetentionDay <Int32>]
 [-HighAvailability <Object>] [-Location <String>] [-PublicAccess <String>] [-Sku <String>]
 [-SkuTier <String>] [-StorageInMb <Int32>] [-Subnet <String>] [-SubnetPrefix <String>] [-Tag <Hashtable>]
 [-Version <ServerVersion>] [-Vnet <String>] [-VnetPrefix <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 설명
새 MySQL 유연한 서버를 만듭니다.

## 예제

### 예제 1: 인수를 사용하여 새 MySql 유연한 서버 만들기
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-Location eastus -AdministratorUserName mysqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240 -PublicAccess none

Checking the existence of the resource group PowershellMySqlTest ...
Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group MySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```



### 예제 2: 기본 설정을 사용하여 새 MySql 유연한 서버 만들기
```powershell
PS C:\> New-AzMySqlFlexibleServer

Creating resource group group00000000...
Creating new vnet VNETserver00000000 in resource group group00000000
Creating new subnet Subnetserver00000000 in resource group group00000000 and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group group00000000...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240
```

이 cmdlet은 기본 매개 변수 값을 사용하여 MySql 유연한 서버를 만들고 새 가상 네트워크 내에서 서버를 프로비전하고 서버에 위임된 서브넷이 있습니다.
위치의 기본값은 미국 서부 2, Sku는 Standard_B1ms, SKU 계층은 버스터블, 저장소 크기는 10GiB입니다.


서버에 대해 자동 생성된 암호를 찾으면 ConvertFrom-SecureString 'SecuredPassword' 속성을 일반 텍스트로 변환합니다.

(예: $server. SecuredPassword | ConvertFrom-SecureString -AsPlainText)

### 예제 3: 가상 네트워크를 사용하여 새 MySql 유연한 서버 만들기
```powershell
PS C:\> $Vnet = 'vnetname'
PS C:\> New-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Vnet $Vnet

or

PS C:\> $Vnet = '/subscriptions/00000000-0000-0000-0000-0000000000/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/vnetname'
PS C:\> New-AzMySqlFlexibleServer  -ResourceGroupName PowershellMySqlTest -Vnet $Vnet

Resource group PowershellMySqlTest exists ? : True
You have supplied a vnet Id/name. Verifying its existence...
Creating new vnet vnetname in resource group PowershellMySqlTest
Creating new subnet Subnetserver00000000 in resource group PowershellMySqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group PowershellMySqlTest...
Your server server00000000 is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

이 cmdlet은 사용자가 제공한 vnet ID 또는 vnet 이름을 통해 MySql 유연한 서버를 만듭니다.
가상 네트워크가 없는 경우 cmdlet에서 만듭니다.

### 예제 4: 가상 네트워크 및 서브넷 이름을 사용하여 새 MySql 유연한 서버 만들기
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Vnet mysql-vnet -Subnet mysql-subnet -VnetPrefix 10.0.0.0/16 -SubnetPrefix 10.0.0.0/24

Resource group PowershellMySqlTest exists ? : True
Creating new vnet mysql-vnet in resource group PowershellMySqlTest
Creating new subnet mysql-subnet in resource group PowershellMySqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

이 cmdlet은 vnet 이름, 서브넷 이름, vnet prefix 및 서브넷 prefix를 통해 MySql 유연한 서버를 만듭니다.
가상 네트워크 및 서브넷이 없는 경우 cmdlet에서 만듭니다.

### 예제 7: 모든 IP에 대한 공용 액세스 권한이 있는 새 MySql 유연한 서버 만들기
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -PublicAccess All

Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 0.0.0.0 to 255.255.255.255

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240
```

이 cmdlet은 모든 IP 주소에 열려 있는 MySql 유연한 서버를 만듭니다.

### 예제 8: 방화벽이 있는 새 MySql 유연한 서버 만들기
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -PublicAccess 10.10.10.10-10.10.10.12

Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 10.10.10.10 to 10.10.10.12

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

이 cmdlet은 지정된 IP 주소에 열려 있는 MySql 유연한 서버를 만듭니다.

## PARAMETERS

### -AdministratorLoginPassword
관리자의 암호입니다.
최소 8자 및 최대 128자입니다.
암호는 영어 대문자, 영어 소문자, 숫자 및 영문자 이 세 가지 범주의 문자를 포함해야 합니다.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdministratorUserName
서버에 대한 관리자 사용자 이름입니다.
설정하면 변경할 수 없습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
명령을 작업으로 실행합니다.

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

### -BackupRetentionDay
서버에 대한 백업 보존 기간입니다.
일 수는 7에서 35 사이입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HighAvailability
고가용성 기능을 사용 또는 사용하지 않도록 설정
기본값은 Disabled입니다.
기본값: 사용 안 합니다.

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
리소스가 있는 위치입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
서버의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
명령을 비동기적으로 실행합니다.

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

### -PublicAccess
공용 액세스를 결정 합니다.
허용되는 IP 목록에 포함될 단일 또는 IP 주소 범위를 입력합니다.
IP 주소 범위는 대시로 구분되어야 합니다. 공백은 포함하지 않습니다.
0.0.0.0을 지정하면 Azure 내에 배포된 모든 리소스에서 공용으로 서버에 액세스할 수 있습니다.
IP 주소를 지정하지 않으면 공용 액세스 모드에서 서버가 설정되지만 방화벽 규칙은 생성되지 않습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스가 포함된 리소스 그룹의 이름입니다. Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sku
SKU의 이름(일반적으로 계층 + 패밀리 + 코어)입니다(예: Standard_B1ms, Standard_D2ds_v4.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuTier
서버의 계산 계층입니다.
허용되는 값: 버스터블, GeneralPurpose, 메모리 최적화.
기본값: 버스터블.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageInMb
서버에 허용되는 최대 저장소입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnet
기존 서브넷의 이름 또는 ID 또는 만들 새 서브넷의 이름입니다.
서브넷은 Microsoft.DBforMySQL/flexibleServers에 위임됩니다.
위임 후 이 서브넷은 다른 유형의 Azure 리소스에 사용할 수 없습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetPrefix
CIDR 형식으로 새 vnet을 만들 때 사용할 서브넷 IP 주소 주소입니다.
기본값은 10.0.0.0/24입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Azure 구독을 식별하는 구독 ID입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
서버 버전입니다.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vnet
기존 가상 네트워크의 이름 또는 ID 또는 만들 새 가상 네트워크의 이름입니다.
이름은 2~64자 사이입니다.
이름은 문자 또는 숫자로 시작하고 문자, 숫자 또는 밑면으로 끝나야하며 문자, 숫자, 밑말, 마주보는 하이픈만 포함할 수 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VnetPrefix
CIDR 형식으로 새 vnet을 만들 때 사용할 IP 주소 연결입니다.
기본값은 10.0.0.0/16입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

## 출력

### Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated

## 참고 사항

별칭

## 관련 링크


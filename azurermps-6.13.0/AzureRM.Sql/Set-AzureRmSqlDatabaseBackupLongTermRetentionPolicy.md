---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: a9389999bdbd93b332a3186ede1003c896552d1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527780"
---
# <span data-ttu-id="6e780-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6e780-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="6e780-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e780-102">SYNOPSIS</span></span>
<span data-ttu-id="6e780-103">서버 장기간 보존 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-103">Sets a server long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e780-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e780-104">SYNTAX</span></span>

### <span data-ttu-id="6e780-105">WeeklyRetentionRequired (기본값)</span><span class="sxs-lookup"><span data-stu-id="6e780-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e780-106">레거시</span><span class="sxs-lookup"><span data-stu-id="6e780-106">Legacy</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -State <String> -ResourceId <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e780-107">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="6e780-107">RemovePolicy</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e780-108">Monthly Required</span><span class="sxs-lookup"><span data-stu-id="6e780-108">MonthlyRetentionRequired</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e780-109">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="6e780-109">YearlyRetentionRequired</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e780-110">설명은</span><span class="sxs-lookup"><span data-stu-id="6e780-110">DESCRIPTION</span></span>
<span data-ttu-id="6e780-111">**AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet은이 데이터베이스에 등록 된 장기 보존 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-111">The **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="6e780-112">정책은 백업 저장소 정책을 정의 하는 데 사용 되는 Azure Backup 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-112">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="6e780-113">예제의</span><span class="sxs-lookup"><span data-stu-id="6e780-113">EXAMPLES</span></span>

### <span data-ttu-id="6e780-114">예제 1: 장기 보존 정책의 현재 버전에 대 한 주 보존 설정</span><span class="sxs-lookup"><span data-stu-id="6e780-114">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="6e780-115">이렇게 하면 database01의 장기 보존 정책이 2 주 동안 매주 전체 백업을 모두 저장 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-115">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="6e780-116">예제 2: 현재 버전의 장기 보존 정책에 대 한 월간 보존 설정</span><span class="sxs-lookup"><span data-stu-id="6e780-116">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="6e780-117">이렇게 하면 database01의 장기 보존 정책이 각 월의 첫 번째 전체 백업을 5 년 동안 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-117">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="6e780-118">예제 3: 현재 버전의 장기 보존 정책에 대 한 연간 보존 설정</span><span class="sxs-lookup"><span data-stu-id="6e780-118">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="6e780-119">이렇게 하면 database01의 장기 보존 정책이 10 년 동안 해당 연도의 26th 주에 수행 된 전체 백업을 저장할 수 있도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-119">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="6e780-120">예제 4: 장기 보존 정책의 현재 버전에 대 한 보존 설정</span><span class="sxs-lookup"><span data-stu-id="6e780-120">Example 4: Set each retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="6e780-121">이렇게 하면 database01의 장기 보존 정책이 각각의 전체 백업을 14 일간 저장 하 고, 각 월의 첫 번째 전체 백업을 24 주 동안 또는 해당 연도의 26th 주에 대해 수행한 전체 백업을 10 년 동안 실행 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-121">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="6e780-122">예제 4: 장기 보존 정책 제거</span><span class="sxs-lookup"><span data-stu-id="6e780-122">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="6e780-123">더 이상 장기 보존 백업을 저장 하지 않도록 database01에 대 한 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-123">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="6e780-124">이미 취한 백업에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-124">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="6e780-125">예제 4: 장기 보존 정책 제거</span><span class="sxs-lookup"><span data-stu-id="6e780-125">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="6e780-126">이는 더 이상 장기 보존 백업을 저장 하지 않도록 database01에 대 한 정책을 제거 하는 또 다른 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-126">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="6e780-127">이미 취한 백업에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-127">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="6e780-128">변수</span><span class="sxs-lookup"><span data-stu-id="6e780-128">PARAMETERS</span></span>

### <span data-ttu-id="6e780-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6e780-129">-DatabaseName</span></span>
<span data-ttu-id="6e780-130">사용할 Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-130">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e780-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e780-131">-DefaultProfile</span></span>
<span data-ttu-id="6e780-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e780-133">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="6e780-133">-MonthlyRetention</span></span>
<span data-ttu-id="6e780-134">월 보존입니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-134">The Monthly Retention.</span></span>
<span data-ttu-id="6e780-135">ISO 8601 문자열 대신 숫자만 전달 되는 경우 days는 단위로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-135">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="6e780-136">Minumum는 7 일이 고 최대 10 년입니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-136">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e780-137">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="6e780-137">-RemovePolicy</span></span>
<span data-ttu-id="6e780-138">제공 하는 경우 데이터베이스에 대 한 정책이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-138">If provided, the policy for the database will be removed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e780-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e780-139">-ResourceGroupName</span></span>
<span data-ttu-id="6e780-140">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-140">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e780-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e780-141">-ResourceId</span></span>
<span data-ttu-id="6e780-142">백업 장기 보존 정책의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-142">The Resource ID of the backup long term retention policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Legacy
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e780-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6e780-143">-ServerName</span></span>
<span data-ttu-id="6e780-144">데이터베이스가 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-144">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e780-145">-상태</span><span class="sxs-lookup"><span data-stu-id="6e780-145">-State</span></span>
<span data-ttu-id="6e780-146">장기 보존 백업 정책, ' 사용 ' 또는 ' 사용 안 함 '의 상태</span><span class="sxs-lookup"><span data-stu-id="6e780-146">The state of the long term retention backup policy, 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: Legacy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e780-147">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="6e780-147">-WeeklyRetention</span></span>
<span data-ttu-id="6e780-148">주간 보존입니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-148">The Weekly Retention.</span></span>
<span data-ttu-id="6e780-149">ISO 8601 문자열 대신 숫자만 전달 되는 경우 days는 단위로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-149">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="6e780-150">Minumum는 7 일이 고 최대 10 년입니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-150">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e780-151">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="6e780-151">-WeekOfYear</span></span>
<span data-ttu-id="6e780-152">연간 보존을 위해 저장할 연간 주 (1 ~ 52)입니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-152">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e780-153">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="6e780-153">-YearlyRetention</span></span>
<span data-ttu-id="6e780-154">연간 보존.</span><span class="sxs-lookup"><span data-stu-id="6e780-154">The Yearly Retention.</span></span>
<span data-ttu-id="6e780-155">ISO 8601 문자열 대신 숫자만 전달 되는 경우 days는 단위로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-155">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="6e780-156">Minumum는 7 일이 고 최대 10 년입니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-156">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e780-157">-확인</span><span class="sxs-lookup"><span data-stu-id="6e780-157">-Confirm</span></span>
<span data-ttu-id="6e780-158">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e780-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e780-159">-WhatIf</span></span>
<span data-ttu-id="6e780-160">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e780-161">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-161">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e780-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e780-162">CommonParameters</span></span>
<span data-ttu-id="6e780-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e780-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e780-164">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e780-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e780-165">입력</span><span class="sxs-lookup"><span data-stu-id="6e780-165">INPUTS</span></span>

### <span data-ttu-id="6e780-166">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6e780-166">System.String</span></span>

### <span data-ttu-id="6e780-167">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="6e780-167">System.Int32</span></span>

## <span data-ttu-id="6e780-168">출력</span><span class="sxs-lookup"><span data-stu-id="6e780-168">OUTPUTS</span></span>

### <span data-ttu-id="6e780-169">AzureSqlDatabaseBackupLongTermRetentionPolicyModel (Microsoft.).</span><span class="sxs-lookup"><span data-stu-id="6e780-169">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="6e780-170">상속자</span><span class="sxs-lookup"><span data-stu-id="6e780-170">NOTES</span></span>

## <span data-ttu-id="6e780-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e780-171">RELATED LINKS</span></span>

[<span data-ttu-id="6e780-172">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6e780-172">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="6e780-173">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="6e780-173">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="6e780-174">제거-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="6e780-174">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="6e780-175">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="6e780-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

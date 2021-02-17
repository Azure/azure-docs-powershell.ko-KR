---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 2bae2753861f182943e4ced142f6a2b3ac84bb1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188012"
---
# <span data-ttu-id="462bb-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="462bb-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="462bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="462bb-102">SYNOPSIS</span></span>
<span data-ttu-id="462bb-103">서버 장기 보존 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-103">Sets a server long term retention policy.</span></span>

## <span data-ttu-id="462bb-104">구문</span><span class="sxs-lookup"><span data-stu-id="462bb-104">SYNTAX</span></span>

### <span data-ttu-id="462bb-105">WeeklyRetentionRequired(기본값)</span><span class="sxs-lookup"><span data-stu-id="462bb-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="462bb-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="462bb-106">RemovePolicy</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="462bb-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="462bb-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="462bb-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="462bb-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="462bb-109">설명</span><span class="sxs-lookup"><span data-stu-id="462bb-109">DESCRIPTION</span></span>
<span data-ttu-id="462bb-110">**Set-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet은 이 데이터베이스에 등록된 장기 보존 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-110">The **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="462bb-111">정책은 백업 저장소 정책을 정의하는 데 사용되는 Azure Backup 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-111">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="462bb-112">예제</span><span class="sxs-lookup"><span data-stu-id="462bb-112">EXAMPLES</span></span>

### <span data-ttu-id="462bb-113">예제 1: 현재 버전의 장기 보존 정책에 대한 주간 보존 설정</span><span class="sxs-lookup"><span data-stu-id="462bb-113">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="462bb-114">데이터베이스01의 장기 보존 정책을 설정하여 매주 전체 백업을 2주 동안 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-114">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="462bb-115">예제 2: 현재 버전의 장기 보존 정책에 대한 월별 보존 설정</span><span class="sxs-lookup"><span data-stu-id="462bb-115">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="462bb-116">데이터베이스01의 장기 보존 정책을 설정하여 매월 첫 번째 전체 백업을 5년 동안 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-116">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="462bb-117">예제 3: 현재 버전의 장기 보존 정책에 대한 연도 보존 설정</span><span class="sxs-lookup"><span data-stu-id="462bb-117">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

<span data-ttu-id="462bb-118">이렇게 하면 데이터베이스01의 장기 보존 정책을 설정하여 10년 동안 연도의 26번째 주에 수행된 전체 백업을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-118">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="462bb-119">예제 4: 현재 버전의 장기 보존 정책에 대한 각 보존 설정</span><span class="sxs-lookup"><span data-stu-id="462bb-119">Example 4: Set each retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

<span data-ttu-id="462bb-120">데이터베이스01의 장기 보존 정책을 설정하여 각 전체 백업을 14일 동안 저장하고, 24주 동안 매월 첫 번째 전체 백업을, 10년 동안 연도의 26번째 주에 수행된 전체 백업을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-120">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="462bb-121">예제 5: 장기 보존 정책 제거</span><span class="sxs-lookup"><span data-stu-id="462bb-121">Example 5: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="462bb-122">더 이상 장기 보존 백업을 저장하지 못하게 database01에 대한 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-122">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="462bb-123">이미 수행된 백업에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-123">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="462bb-124">예제 6: 장기 보존 정책 제거</span><span class="sxs-lookup"><span data-stu-id="462bb-124">Example 6: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="462bb-125">이는 더 이상 장기 보존 백업을 저장하지 못하게 database01에 대한 정책을 제거하는 또 다른 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-125">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="462bb-126">이미 수행된 백업에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-126">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="462bb-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="462bb-127">PARAMETERS</span></span>

### <span data-ttu-id="462bb-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="462bb-128">-DatabaseName</span></span>
<span data-ttu-id="462bb-129">사용할 Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-129">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="462bb-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="462bb-130">-DefaultProfile</span></span>
<span data-ttu-id="462bb-131">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="462bb-132">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="462bb-132">-MonthlyRetention</span></span>
<span data-ttu-id="462bb-133">월별 보존입니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-133">The Monthly Retention.</span></span>
<span data-ttu-id="462bb-134">ISO 8601 문자열 대신 숫자만 전달되는 경우 일 수를 단위로 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-134">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="462bb-135">최소 7일 및 최대 10년이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-135">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="462bb-136">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="462bb-136">-RemovePolicy</span></span>
<span data-ttu-id="462bb-137">제공된 경우 데이터베이스에 대한 정책이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-137">If provided, the policy for the database will be removed.</span></span>

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

### <span data-ttu-id="462bb-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="462bb-138">-ResourceGroupName</span></span>
<span data-ttu-id="462bb-139">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="462bb-140">-ServerName</span><span class="sxs-lookup"><span data-stu-id="462bb-140">-ServerName</span></span>
<span data-ttu-id="462bb-141">데이터베이스가 있는 azure SQL Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-141">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="462bb-142">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="462bb-142">-WeeklyRetention</span></span>
<span data-ttu-id="462bb-143">주간 보존.</span><span class="sxs-lookup"><span data-stu-id="462bb-143">The Weekly Retention.</span></span>
<span data-ttu-id="462bb-144">ISO 8601 문자열 대신 숫자만 전달되는 경우 일 수를 단위로 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-144">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="462bb-145">최소 7일 및 최대 10년이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-145">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="462bb-146">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="462bb-146">-WeekOfYear</span></span>
<span data-ttu-id="462bb-147">연도 보존을 위해 절약할 연도의 주,1-52입니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-147">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="462bb-148">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="462bb-148">-YearlyRetention</span></span>
<span data-ttu-id="462bb-149">연도 보존.</span><span class="sxs-lookup"><span data-stu-id="462bb-149">The Yearly Retention.</span></span>
<span data-ttu-id="462bb-150">ISO 8601 문자열 대신 숫자만 전달되는 경우 일 수를 단위로 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-150">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="462bb-151">최소 7일 및 최대 10년이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-151">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="462bb-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="462bb-152">-Confirm</span></span>
<span data-ttu-id="462bb-153">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="462bb-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="462bb-154">-WhatIf</span></span>
<span data-ttu-id="462bb-155">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="462bb-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="462bb-156">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="462bb-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="462bb-157">CommonParameters</span></span>
<span data-ttu-id="462bb-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="462bb-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="462bb-159">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="462bb-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="462bb-160">입력</span><span class="sxs-lookup"><span data-stu-id="462bb-160">INPUTS</span></span>

### <span data-ttu-id="462bb-161">System.String</span><span class="sxs-lookup"><span data-stu-id="462bb-161">System.String</span></span>

### <span data-ttu-id="462bb-162">System.Int32</span><span class="sxs-lookup"><span data-stu-id="462bb-162">System.Int32</span></span>

## <span data-ttu-id="462bb-163">출력</span><span class="sxs-lookup"><span data-stu-id="462bb-163">OUTPUTS</span></span>

### <span data-ttu-id="462bb-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="462bb-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="462bb-165">참고 사항</span><span class="sxs-lookup"><span data-stu-id="462bb-165">NOTES</span></span>

## <span data-ttu-id="462bb-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="462bb-166">RELATED LINKS</span></span>

[<span data-ttu-id="462bb-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="462bb-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="462bb-168">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="462bb-168">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="462bb-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="462bb-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="462bb-170">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="462bb-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 6e78a6f76a037b639177d69830cf6b7d191c69dc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034420"
---
# <span data-ttu-id="b10ef-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b10ef-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="b10ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b10ef-102">SYNOPSIS</span></span>
<span data-ttu-id="b10ef-103">서버 장기간 보존 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-103">Sets a server long term retention policy.</span></span>

## <span data-ttu-id="b10ef-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b10ef-104">SYNTAX</span></span>

### <span data-ttu-id="b10ef-105">WeeklyRetentionRequired (기본값)</span><span class="sxs-lookup"><span data-stu-id="b10ef-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b10ef-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="b10ef-106">RemovePolicy</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b10ef-107">Monthly Required</span><span class="sxs-lookup"><span data-stu-id="b10ef-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b10ef-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="b10ef-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b10ef-109">설명은</span><span class="sxs-lookup"><span data-stu-id="b10ef-109">DESCRIPTION</span></span>
<span data-ttu-id="b10ef-110">**AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet은이 데이터베이스에 등록 된 장기 보존 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-110">The **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="b10ef-111">정책은 백업 저장소 정책을 정의 하는 데 사용 되는 Azure Backup 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-111">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="b10ef-112">예제의</span><span class="sxs-lookup"><span data-stu-id="b10ef-112">EXAMPLES</span></span>

### <span data-ttu-id="b10ef-113">예제 1: 장기 보존 정책의 현재 버전에 대 한 주 보존 설정</span><span class="sxs-lookup"><span data-stu-id="b10ef-113">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="b10ef-114">이렇게 하면 database01의 장기 보존 정책이 2 주 동안 매주 전체 백업을 모두 저장 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-114">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="b10ef-115">예제 2: 현재 버전의 장기 보존 정책에 대 한 월간 보존 설정</span><span class="sxs-lookup"><span data-stu-id="b10ef-115">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="b10ef-116">이렇게 하면 database01의 장기 보존 정책이 각 월의 첫 번째 전체 백업을 5 년 동안 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-116">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="b10ef-117">예제 3: 현재 버전의 장기 보존 정책에 대 한 연간 보존 설정</span><span class="sxs-lookup"><span data-stu-id="b10ef-117">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="b10ef-118">이렇게 하면 database01의 장기 보존 정책이 10 년 동안 해당 연도의 26th 주에 수행 된 전체 백업을 저장할 수 있도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-118">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="b10ef-119">예제 4: 장기 보존 정책의 현재 버전에 대 한 보존 설정</span><span class="sxs-lookup"><span data-stu-id="b10ef-119">Example 4: Set each retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="b10ef-120">이렇게 하면 database01의 장기 보존 정책이 각각의 전체 백업을 14 일간 저장 하 고, 각 월의 첫 번째 전체 백업을 24 주 동안 또는 해당 연도의 26th 주에 대해 수행한 전체 백업을 10 년 동안 실행 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-120">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="b10ef-121">예제 4: 장기 보존 정책 제거</span><span class="sxs-lookup"><span data-stu-id="b10ef-121">Example 4: Remove the long term retention policy</span></span>
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

<span data-ttu-id="b10ef-122">더 이상 장기 보존 백업을 저장 하지 않도록 database01에 대 한 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-122">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="b10ef-123">이미 취한 백업에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-123">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="b10ef-124">예제 4: 장기 보존 정책 제거</span><span class="sxs-lookup"><span data-stu-id="b10ef-124">Example 4: Remove the long term retention policy</span></span>
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

<span data-ttu-id="b10ef-125">이는 더 이상 장기 보존 백업을 저장 하지 않도록 database01에 대 한 정책을 제거 하는 또 다른 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-125">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="b10ef-126">이미 취한 백업에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-126">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="b10ef-127">변수</span><span class="sxs-lookup"><span data-stu-id="b10ef-127">PARAMETERS</span></span>

### <span data-ttu-id="b10ef-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b10ef-128">-DatabaseName</span></span>
<span data-ttu-id="b10ef-129">사용할 Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-129">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="b10ef-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b10ef-130">-DefaultProfile</span></span>
<span data-ttu-id="b10ef-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b10ef-132">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="b10ef-132">-MonthlyRetention</span></span>
<span data-ttu-id="b10ef-133">월 보존입니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-133">The Monthly Retention.</span></span>
<span data-ttu-id="b10ef-134">ISO 8601 문자열 대신 숫자만 전달 되는 경우 days는 단위로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-134">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="b10ef-135">최소 7 일과 최대 10 년입니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-135">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="b10ef-136">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="b10ef-136">-RemovePolicy</span></span>
<span data-ttu-id="b10ef-137">제공 하는 경우 데이터베이스에 대 한 정책이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-137">If provided, the policy for the database will be removed.</span></span>

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

### <span data-ttu-id="b10ef-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b10ef-138">-ResourceGroupName</span></span>
<span data-ttu-id="b10ef-139">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="b10ef-140">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b10ef-140">-ServerName</span></span>
<span data-ttu-id="b10ef-141">데이터베이스가 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-141">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="b10ef-142">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="b10ef-142">-WeeklyRetention</span></span>
<span data-ttu-id="b10ef-143">주간 보존입니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-143">The Weekly Retention.</span></span>
<span data-ttu-id="b10ef-144">ISO 8601 문자열 대신 숫자만 전달 되는 경우 days는 단위로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-144">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="b10ef-145">최소 7 일과 최대 10 년입니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-145">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="b10ef-146">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="b10ef-146">-WeekOfYear</span></span>
<span data-ttu-id="b10ef-147">연간 보존을 위해 저장할 연간 주 (1 ~ 52)입니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-147">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="b10ef-148">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="b10ef-148">-YearlyRetention</span></span>
<span data-ttu-id="b10ef-149">연간 보존.</span><span class="sxs-lookup"><span data-stu-id="b10ef-149">The Yearly Retention.</span></span>
<span data-ttu-id="b10ef-150">ISO 8601 문자열 대신 숫자만 전달 되는 경우 days는 단위로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-150">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="b10ef-151">최소 7 일과 최대 10 년입니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-151">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="b10ef-152">-확인</span><span class="sxs-lookup"><span data-stu-id="b10ef-152">-Confirm</span></span>
<span data-ttu-id="b10ef-153">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b10ef-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b10ef-154">-WhatIf</span></span>
<span data-ttu-id="b10ef-155">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b10ef-156">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b10ef-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b10ef-157">CommonParameters</span></span>
<span data-ttu-id="b10ef-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b10ef-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b10ef-159">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b10ef-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b10ef-160">입력</span><span class="sxs-lookup"><span data-stu-id="b10ef-160">INPUTS</span></span>

### <span data-ttu-id="b10ef-161">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b10ef-161">System.String</span></span>

### <span data-ttu-id="b10ef-162">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="b10ef-162">System.Int32</span></span>

## <span data-ttu-id="b10ef-163">출력</span><span class="sxs-lookup"><span data-stu-id="b10ef-163">OUTPUTS</span></span>

### <span data-ttu-id="b10ef-164">AzureSqlDatabaseBackupLongTermRetentionPolicyModel (Microsoft.).</span><span class="sxs-lookup"><span data-stu-id="b10ef-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="b10ef-165">상속자</span><span class="sxs-lookup"><span data-stu-id="b10ef-165">NOTES</span></span>

## <span data-ttu-id="b10ef-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b10ef-166">RELATED LINKS</span></span>

[<span data-ttu-id="b10ef-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b10ef-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="b10ef-168">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b10ef-168">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="b10ef-169">제거-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b10ef-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="b10ef-170">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="b10ef-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
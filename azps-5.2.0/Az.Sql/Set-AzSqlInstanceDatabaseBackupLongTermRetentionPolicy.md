---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: cf7cf1dcd91bc1c9f703e4fc5ca613ad6407e575
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346485"
---
# <span data-ttu-id="b1e1d-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b1e1d-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="b1e1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1e1d-102">SYNOPSIS</span></span>
<span data-ttu-id="b1e1d-103">**Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet은 관리되는 데이터베이스의 장기 보존 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="b1e1d-104">구문</span><span class="sxs-lookup"><span data-stu-id="b1e1d-104">SYNTAX</span></span>

### <span data-ttu-id="b1e1d-105">WeeklyRetentionRequired(기본값)</span><span class="sxs-lookup"><span data-stu-id="b1e1d-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1e1d-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="b1e1d-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1e1d-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="b1e1d-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1e1d-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="b1e1d-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1e1d-109">설명</span><span class="sxs-lookup"><span data-stu-id="b1e1d-109">DESCRIPTION</span></span>
<span data-ttu-id="b1e1d-110">**Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet은 이 관리되는 데이터베이스에 대한 장기 보존 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="b1e1d-111">예제</span><span class="sxs-lookup"><span data-stu-id="b1e1d-111">EXAMPLES</span></span>

### <span data-ttu-id="b1e1d-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="b1e1d-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -WeeklyRetention "P1W"


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P1W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="b1e1d-113">데이터베이스의 장기 보존 주간 정책을 1주로 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="b1e1d-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="b1e1d-114">Example 2</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName target1 -RemovePolicy


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : target1
WeeklyRetention     : PT0S
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="b1e1d-115">이 명령은 데이터베이스에서 장기 보존 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-115">This command removes the long term retention policy from the database.</span></span>

### <span data-ttu-id="b1e1d-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="b1e1d-116">Example 3</span></span>

<span data-ttu-id="b1e1d-117">이 Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet은 관리되는 데이터베이스의 장기 보존 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-117">The Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet sets a managed database's long term retention policy.</span></span> <span data-ttu-id="b1e1d-118">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="b1e1d-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -DatabaseName target1 -InstanceName testInstance -MonthlyRetention P24W -ResourceGroupName testResourceGroup -WeekOfYear 26 -WeeklyRetention 'P1W' -YearlyRetention P10Y
```

## <span data-ttu-id="b1e1d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1e1d-119">PARAMETERS</span></span>

### <span data-ttu-id="b1e1d-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b1e1d-120">-DatabaseName</span></span>
<span data-ttu-id="b1e1d-121">사용할 Azure Managed Database의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-121">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="b1e1d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1e1d-122">-DefaultProfile</span></span>
<span data-ttu-id="b1e1d-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1e1d-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b1e1d-124">-InstanceName</span></span>
<span data-ttu-id="b1e1d-125">데이터베이스가 속한 Azure Managed Instance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-125">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="b1e1d-126">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="b1e1d-126">-MonthlyRetention</span></span>
<span data-ttu-id="b1e1d-127">월별 보존입니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-127">The Monthly Retention.</span></span>
<span data-ttu-id="b1e1d-128">ISO 8601 문자열 대신 숫자만 전달되는 경우 일 수를 단위로 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-128">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="b1e1d-129">최소 7일 및 최대 10년이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-129">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="b1e1d-130">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="b1e1d-130">-RemovePolicy</span></span>
<span data-ttu-id="b1e1d-131">제공된 경우 데이터베이스에 대한 정책이 지워지게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-131">If provided, the policy for the database will be cleared.</span></span>

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

### <span data-ttu-id="b1e1d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1e1d-132">-ResourceGroupName</span></span>
<span data-ttu-id="b1e1d-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="b1e1d-134">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="b1e1d-134">-WeeklyRetention</span></span>
<span data-ttu-id="b1e1d-135">주간 보존.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-135">The Weekly Retention.</span></span>
<span data-ttu-id="b1e1d-136">ISO 8601 문자열 대신 숫자만 전달되는 경우 일 수를 단위로 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-136">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="b1e1d-137">최소 7일 및 최대 10년이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-137">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="b1e1d-138">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="b1e1d-138">-WeekOfYear</span></span>
<span data-ttu-id="b1e1d-139">연도 보존을 위해 절약할 연도의 주,1-52입니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-139">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="b1e1d-140">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="b1e1d-140">-YearlyRetention</span></span>
<span data-ttu-id="b1e1d-141">연도 보존.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-141">The Yearly Retention.</span></span>
<span data-ttu-id="b1e1d-142">ISO 8601 문자열 대신 숫자만 전달되는 경우 일 수를 단위로 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-142">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="b1e1d-143">최소 7일 및 최대 10년이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-143">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="b1e1d-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1e1d-144">-Confirm</span></span>
<span data-ttu-id="b1e1d-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1e1d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1e1d-146">-WhatIf</span></span>
<span data-ttu-id="b1e1d-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b1e1d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1e1d-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1e1d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1e1d-149">CommonParameters</span></span>
<span data-ttu-id="b1e1d-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1e1d-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b1e1d-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1e1d-152">입력</span><span class="sxs-lookup"><span data-stu-id="b1e1d-152">INPUTS</span></span>

### <span data-ttu-id="b1e1d-153">System.String</span><span class="sxs-lookup"><span data-stu-id="b1e1d-153">System.String</span></span>

### <span data-ttu-id="b1e1d-154">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b1e1d-154">System.Int32</span></span>

## <span data-ttu-id="b1e1d-155">출력</span><span class="sxs-lookup"><span data-stu-id="b1e1d-155">OUTPUTS</span></span>

### <span data-ttu-id="b1e1d-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b1e1d-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="b1e1d-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b1e1d-157">NOTES</span></span>

## <span data-ttu-id="b1e1d-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1e1d-158">RELATED LINKS</span></span>

[<span data-ttu-id="b1e1d-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b1e1d-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="b1e1d-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b1e1d-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="b1e1d-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b1e1d-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="b1e1d-162">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="b1e1d-162">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
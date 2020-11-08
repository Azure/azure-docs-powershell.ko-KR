---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: cf7cf1dcd91bc1c9f703e4fc5ca613ad6407e575
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204754"
---
# <span data-ttu-id="f5788-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f5788-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="f5788-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5788-102">SYNOPSIS</span></span>
<span data-ttu-id="f5788-103">**Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet은 관리 데이터베이스의 장기 보존 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="f5788-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5788-104">SYNTAX</span></span>

### <span data-ttu-id="f5788-105">WeeklyRetentionRequired (기본값)</span><span class="sxs-lookup"><span data-stu-id="f5788-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5788-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="f5788-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5788-107">Monthly Required</span><span class="sxs-lookup"><span data-stu-id="f5788-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5788-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="f5788-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5788-109">설명은</span><span class="sxs-lookup"><span data-stu-id="f5788-109">DESCRIPTION</span></span>
<span data-ttu-id="f5788-110">**AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet은이 관리 데이터베이스에 대 한 장기 보존 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="f5788-111">예제의</span><span class="sxs-lookup"><span data-stu-id="f5788-111">EXAMPLES</span></span>

### <span data-ttu-id="f5788-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="f5788-112">Example 1</span></span>
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

<span data-ttu-id="f5788-113">데이터베이스의 장기 보존 주간 정책을 1 주로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="f5788-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="f5788-114">Example 2</span></span>
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

<span data-ttu-id="f5788-115">이 명령은 데이터베이스에서 장기간 보존 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-115">This command removes the long term retention policy from the database.</span></span>

### <span data-ttu-id="f5788-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="f5788-116">Example 3</span></span>

<span data-ttu-id="f5788-117">Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet은 관리 데이터베이스의 장기 보존 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-117">The Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet sets a managed database's long term retention policy.</span></span> <span data-ttu-id="f5788-118">생성</span><span class="sxs-lookup"><span data-stu-id="f5788-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -DatabaseName target1 -InstanceName testInstance -MonthlyRetention P24W -ResourceGroupName testResourceGroup -WeekOfYear 26 -WeeklyRetention 'P1W' -YearlyRetention P10Y
```

## <span data-ttu-id="f5788-119">변수</span><span class="sxs-lookup"><span data-stu-id="f5788-119">PARAMETERS</span></span>

### <span data-ttu-id="f5788-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f5788-120">-DatabaseName</span></span>
<span data-ttu-id="f5788-121">사용할 Azure 관리 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-121">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="f5788-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5788-122">-DefaultProfile</span></span>
<span data-ttu-id="f5788-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5788-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f5788-124">-InstanceName</span></span>
<span data-ttu-id="f5788-125">데이터베이스가 속한 Azure 관리 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-125">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="f5788-126">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="f5788-126">-MonthlyRetention</span></span>
<span data-ttu-id="f5788-127">월 보존입니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-127">The Monthly Retention.</span></span>
<span data-ttu-id="f5788-128">ISO 8601 문자열 대신 숫자만 전달 되는 경우 days는 단위로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-128">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="f5788-129">최소 7 일과 최대 10 년입니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-129">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="f5788-130">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="f5788-130">-RemovePolicy</span></span>
<span data-ttu-id="f5788-131">제공 하는 경우 데이터베이스에 대 한 정책이 지워집니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-131">If provided, the policy for the database will be cleared.</span></span>

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

### <span data-ttu-id="f5788-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5788-132">-ResourceGroupName</span></span>
<span data-ttu-id="f5788-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="f5788-134">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="f5788-134">-WeeklyRetention</span></span>
<span data-ttu-id="f5788-135">주간 보존입니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-135">The Weekly Retention.</span></span>
<span data-ttu-id="f5788-136">ISO 8601 문자열 대신 숫자만 전달 되는 경우 days는 단위로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-136">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="f5788-137">최소 7 일과 최대 10 년입니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-137">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="f5788-138">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="f5788-138">-WeekOfYear</span></span>
<span data-ttu-id="f5788-139">연간 보존을 위해 저장할 연간 주 (1 ~ 52)입니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-139">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="f5788-140">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="f5788-140">-YearlyRetention</span></span>
<span data-ttu-id="f5788-141">연간 보존.</span><span class="sxs-lookup"><span data-stu-id="f5788-141">The Yearly Retention.</span></span>
<span data-ttu-id="f5788-142">ISO 8601 문자열 대신 숫자만 전달 되는 경우 days는 단위로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-142">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="f5788-143">최소 7 일과 최대 10 년입니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-143">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="f5788-144">-확인</span><span class="sxs-lookup"><span data-stu-id="f5788-144">-Confirm</span></span>
<span data-ttu-id="f5788-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5788-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5788-146">-WhatIf</span></span>
<span data-ttu-id="f5788-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5788-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5788-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5788-149">CommonParameters</span></span>
<span data-ttu-id="f5788-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5788-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5788-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f5788-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5788-152">입력</span><span class="sxs-lookup"><span data-stu-id="f5788-152">INPUTS</span></span>

### <span data-ttu-id="f5788-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f5788-153">System.String</span></span>

### <span data-ttu-id="f5788-154">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="f5788-154">System.Int32</span></span>

## <span data-ttu-id="f5788-155">출력</span><span class="sxs-lookup"><span data-stu-id="f5788-155">OUTPUTS</span></span>

### <span data-ttu-id="f5788-156">AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel (\*). m. ManagedDatabaseBackup.</span><span class="sxs-lookup"><span data-stu-id="f5788-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="f5788-157">상속자</span><span class="sxs-lookup"><span data-stu-id="f5788-157">NOTES</span></span>

## <span data-ttu-id="f5788-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5788-158">RELATED LINKS</span></span>

[<span data-ttu-id="f5788-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f5788-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="f5788-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="f5788-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="f5788-161">제거-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="f5788-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="f5788-162">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="f5788-162">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
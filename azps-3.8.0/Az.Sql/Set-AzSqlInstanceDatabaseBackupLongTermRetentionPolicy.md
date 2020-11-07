---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 5d734836f822b61ac37ca0ba567eda4473e0292e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878822"
---
# <span data-ttu-id="52efa-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="52efa-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="52efa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52efa-102">SYNOPSIS</span></span>
<span data-ttu-id="52efa-103">**Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet은 관리 데이터베이스의 장기 보존 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="52efa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="52efa-104">SYNTAX</span></span>

### <span data-ttu-id="52efa-105">WeeklyRetentionRequired (기본값)</span><span class="sxs-lookup"><span data-stu-id="52efa-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52efa-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="52efa-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52efa-107">Monthly Required</span><span class="sxs-lookup"><span data-stu-id="52efa-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52efa-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="52efa-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52efa-109">설명은</span><span class="sxs-lookup"><span data-stu-id="52efa-109">DESCRIPTION</span></span>
<span data-ttu-id="52efa-110">**AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet은이 관리 데이터베이스에 대 한 장기 보존 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="52efa-111">예제의</span><span class="sxs-lookup"><span data-stu-id="52efa-111">EXAMPLES</span></span>

### <span data-ttu-id="52efa-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="52efa-112">Example 1</span></span>
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

<span data-ttu-id="52efa-113">데이터베이스의 장기 보존 주간 정책을 1 주로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="52efa-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="52efa-114">Example 2</span></span>
```
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


<span data-ttu-id="52efa-115">이 명령은 데이터베이스에서 장기간 보존 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-115">This command removes the long term retention policy from the database.</span></span>
## <span data-ttu-id="52efa-116">변수</span><span class="sxs-lookup"><span data-stu-id="52efa-116">PARAMETERS</span></span>

### <span data-ttu-id="52efa-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="52efa-117">-DatabaseName</span></span>
<span data-ttu-id="52efa-118">사용할 Azure 관리 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-118">The name of the Azure Managed Database to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52efa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52efa-119">-DefaultProfile</span></span>
<span data-ttu-id="52efa-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52efa-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="52efa-121">-InstanceName</span></span>
<span data-ttu-id="52efa-122">데이터베이스가 속한 Azure 관리 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-122">The name of the Azure Managed Instance the database belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52efa-123">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="52efa-123">-MonthlyRetention</span></span>
<span data-ttu-id="52efa-124">월 보존입니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-124">The Monthly Retention.</span></span>
<span data-ttu-id="52efa-125">ISO 8601 문자열 대신 숫자만 전달 되는 경우 days는 단위로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-125">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="52efa-126">최소 7 일과 최대 10 년입니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-126">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52efa-127">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="52efa-127">-RemovePolicy</span></span>
<span data-ttu-id="52efa-128">제공 하는 경우 데이터베이스에 대 한 정책이 지워집니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-128">If provided, the policy for the database will be cleared.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52efa-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52efa-129">-ResourceGroupName</span></span>
<span data-ttu-id="52efa-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-130">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52efa-131">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="52efa-131">-WeeklyRetention</span></span>
<span data-ttu-id="52efa-132">주간 보존입니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-132">The Weekly Retention.</span></span>
<span data-ttu-id="52efa-133">ISO 8601 문자열 대신 숫자만 전달 되는 경우 days는 단위로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-133">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="52efa-134">최소 7 일과 최대 10 년입니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-134">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52efa-135">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="52efa-135">-WeekOfYear</span></span>
<span data-ttu-id="52efa-136">연간 보존을 위해 저장할 연간 주 (1 ~ 52)입니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-136">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52efa-137">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="52efa-137">-YearlyRetention</span></span>
<span data-ttu-id="52efa-138">연간 보존.</span><span class="sxs-lookup"><span data-stu-id="52efa-138">The Yearly Retention.</span></span>
<span data-ttu-id="52efa-139">ISO 8601 문자열 대신 숫자만 전달 되는 경우 days는 단위로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-139">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="52efa-140">최소 7 일과 최대 10 년입니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-140">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52efa-141">-확인</span><span class="sxs-lookup"><span data-stu-id="52efa-141">-Confirm</span></span>
<span data-ttu-id="52efa-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52efa-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52efa-143">-WhatIf</span></span>
<span data-ttu-id="52efa-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52efa-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52efa-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52efa-146">CommonParameters</span></span>
<span data-ttu-id="52efa-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="52efa-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52efa-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="52efa-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52efa-149">입력</span><span class="sxs-lookup"><span data-stu-id="52efa-149">INPUTS</span></span>

### <span data-ttu-id="52efa-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="52efa-150">System.String</span></span>

### <span data-ttu-id="52efa-151">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="52efa-151">System.Int32</span></span>

## <span data-ttu-id="52efa-152">출력</span><span class="sxs-lookup"><span data-stu-id="52efa-152">OUTPUTS</span></span>

### <span data-ttu-id="52efa-153">AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel (\*). m. ManagedDatabaseBackup.</span><span class="sxs-lookup"><span data-stu-id="52efa-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="52efa-154">상속자</span><span class="sxs-lookup"><span data-stu-id="52efa-154">NOTES</span></span>

## <span data-ttu-id="52efa-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52efa-155">RELATED LINKS</span></span>

[<span data-ttu-id="52efa-156">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="52efa-156">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="52efa-157">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="52efa-157">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="52efa-158">제거-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="52efa-158">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="52efa-159">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="52efa-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
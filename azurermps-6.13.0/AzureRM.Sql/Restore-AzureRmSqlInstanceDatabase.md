---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: 61fe76eba8d1f8faf0ab45d0a24f56a8dabf3641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536496"
---
# <span data-ttu-id="59b4d-101">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="59b4d-101">Restore-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="59b4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59b4d-102">SYNOPSIS</span></span>
<span data-ttu-id="59b4d-103">Azure SQL 관리 인스턴스 데이터베이스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-103">Restores an Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59b4d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59b4d-104">SYNTAX</span></span>

### <span data-ttu-id="59b4d-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="59b4d-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59b4d-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="59b4d-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59b4d-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="59b4d-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59b4d-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="59b4d-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59b4d-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="59b4d-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59b4d-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="59b4d-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59b4d-111">설명은</span><span class="sxs-lookup"><span data-stu-id="59b4d-111">DESCRIPTION</span></span>
<span data-ttu-id="59b4d-112">**Restore-AzureRmSqlInstanceDatabase** cmdlet은 라이브 데이터베이스의 특정 시점에서 인스턴스 데이터베이스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-112">The **Restore-AzureRmSqlInstanceDatabase** cmdlet restores an instance database from a point in time in a live database.</span></span>
<span data-ttu-id="59b4d-113">복원 된 데이터베이스는 새 인스턴스 데이터베이스로 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-113">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="59b4d-114">예제의</span><span class="sxs-lookup"><span data-stu-id="59b4d-114">EXAMPLES</span></span>

### <span data-ttu-id="59b4d-115">예제 1: 지정 된 시점에서 인스턴스 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="59b4d-115">Example 1: Restore a instance database from a point in time</span></span>
```
PS C:\> Restore-AzureRmSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="59b4d-116">이 명령은 지정 된 특정 시점 백업에서 인스턴스 데이터베이스 Database01를 Database01_restored 라는 인스턴스 데이터베이스로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-116">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="59b4d-117">예제 2: 다른 리소스 그룹의 특정 시점에서 다른 인스턴스로 인스턴스 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="59b4d-117">Example 2: Restore a instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzureRmSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="59b4d-118">이 명령은 managedInstance1에서 리소스 그룹 ResourceGroup02의 인스턴스 데이터베이스 Database01를 지정 된 특정 시점 백업에서 ResourceGroup01 인스턴스에 있는 인스턴스 Database01_restored 데이터베이스 ($ managedInstance2)로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-118">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

## <span data-ttu-id="59b4d-119">변수</span><span class="sxs-lookup"><span data-stu-id="59b4d-119">PARAMETERS</span></span>

### <span data-ttu-id="59b4d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59b4d-120">-AsJob</span></span>
<span data-ttu-id="59b4d-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="59b4d-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b4d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59b4d-122">-DefaultProfile</span></span>
<span data-ttu-id="59b4d-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59b4d-124">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="59b4d-124">-FromPointInTimeBackup</span></span>
<span data-ttu-id="59b4d-125">지정 시간 백업에서 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-125">Restore from a point-in-time backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b4d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59b4d-126">-InputObject</span></span>
<span data-ttu-id="59b4d-127">복원할 인스턴스 데이터베이스 개체</span><span class="sxs-lookup"><span data-stu-id="59b4d-127">The Instance Database object to restore</span></span>

```yaml
Type: AzureSqlManagedDatabaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59b4d-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="59b4d-128">-InstanceName</span></span>
<span data-ttu-id="59b4d-129">인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-129">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b4d-130">-이름</span><span class="sxs-lookup"><span data-stu-id="59b4d-130">-Name</span></span>
<span data-ttu-id="59b4d-131">복원할 인스턴스 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-131">The instance database name to restore.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b4d-132">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="59b4d-132">-PointInTime</span></span>
<span data-ttu-id="59b4d-133">데이터베이스를 복원할 시점을 지정 하는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-133">The point in time to restore the database to.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b4d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59b4d-134">-ResourceGroupName</span></span>
<span data-ttu-id="59b4d-135">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-135">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b4d-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59b4d-136">-ResourceId</span></span>
<span data-ttu-id="59b4d-137">복원할 인스턴스 데이터베이스 개체의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-137">The resource id of Instance Database object to restore</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59b4d-138">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="59b4d-138">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="59b4d-139">복원할 대상 인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-139">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="59b4d-140">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="59b4d-140">-TargetInstanceName</span></span>
<span data-ttu-id="59b4d-141">복원할 대상 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-141">The name of the target instance to restore to.</span></span>
<span data-ttu-id="59b4d-142">지정 하지 않으면 대상 인스턴스가 원본 인스턴스와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-142">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b4d-143">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59b4d-143">-TargetResourceGroupName</span></span>
<span data-ttu-id="59b4d-144">복원할 대상 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-144">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="59b4d-145">지정 하지 않으면 대상 리소스 그룹이 원본 리소스 그룹과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-145">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b4d-146">-확인</span><span class="sxs-lookup"><span data-stu-id="59b4d-146">-Confirm</span></span>
<span data-ttu-id="59b4d-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59b4d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59b4d-148">-WhatIf</span></span>
<span data-ttu-id="59b4d-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59b4d-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59b4d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b4d-151">CommonParameters</span></span>
<span data-ttu-id="59b4d-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59b4d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b4d-153">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59b4d-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b4d-154">입력</span><span class="sxs-lookup"><span data-stu-id="59b4d-154">INPUTS</span></span>

### <span data-ttu-id="59b4d-155">AzureSqlManagedDatabaseModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="59b4d-155">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>
<span data-ttu-id="59b4d-156">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="59b4d-156">System.String</span></span>

## <span data-ttu-id="59b4d-157">출력</span><span class="sxs-lookup"><span data-stu-id="59b4d-157">OUTPUTS</span></span>

### <span data-ttu-id="59b4d-158">AzureSqlManagedDatabaseModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="59b4d-158">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="59b4d-159">상속자</span><span class="sxs-lookup"><span data-stu-id="59b4d-159">NOTES</span></span>

## <span data-ttu-id="59b4d-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59b4d-160">RELATED LINKS</span></span>

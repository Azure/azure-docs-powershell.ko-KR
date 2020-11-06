---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Get-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
ms.openlocfilehash: caab43824c63e73e7011c0377d0bd7665befe5dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532013"
---
# <span data-ttu-id="aefa4-101">Get-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="aefa4-101">Get-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="aefa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aefa4-102">SYNOPSIS</span></span>
<span data-ttu-id="aefa4-103">Azure 데이터베이스 마이그레이션 서비스 마이그레이션 작업과 연결 된 PSProjectTask 개체를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="aefa4-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aefa4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aefa4-104">SYNTAX</span></span>

### <span data-ttu-id="aefa4-105">ListByComponent (기본값)</span><span class="sxs-lookup"><span data-stu-id="aefa4-105">ListByComponent (Default)</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aefa4-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="aefa4-106">ListByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aefa4-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="aefa4-107">GetByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aefa4-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="aefa4-108">GetByInputObjectResultType</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aefa4-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="aefa4-109">ListByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aefa4-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="aefa4-110">GetByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aefa4-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="aefa4-111">GetByResourceIdResultType</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aefa4-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="aefa4-112">GetByComponent</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aefa4-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="aefa4-113">GetByComponentResultType</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aefa4-114">설명은</span><span class="sxs-lookup"><span data-stu-id="aefa4-114">DESCRIPTION</span></span>
<span data-ttu-id="aefa4-115">Get-AzureRmDataMigrationTask cmdlet은 Azure 데이터베이스 마이그레이션 서비스 마이그레이션 작업과 연결 된 속성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="aefa4-115">The Get-AzureRmDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="aefa4-116">예제의</span><span class="sxs-lookup"><span data-stu-id="aefa4-116">EXAMPLES</span></span>

### <span data-ttu-id="aefa4-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="aefa4-117">Example 1</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="aefa4-118">위의 예제에서는 Get-AzureRmDataMigrationTask cmdlet을 사용 하 여 입력 매개 변수로 전달 된 작업 이름을 기반으로 Azure 데이터베이스 마이그레이션 서비스 마이그레이션 작업과 연결 된 속성을 검색 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aefa4-118">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="aefa4-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="aefa4-119">Example 2</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -Project $myProject
```

<span data-ttu-id="aefa4-120">위 예제에서는 Get-AzureRmDataMigrationTask cmdlet을 사용 하 여 입력 매개 변수로 전달 된 PSProject 개체와 관련 된 모든 마이그레이션 작업을 검색 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aefa4-120">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="aefa4-121">변수</span><span class="sxs-lookup"><span data-stu-id="aefa4-121">PARAMETERS</span></span>

### <span data-ttu-id="aefa4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aefa4-122">-DefaultProfile</span></span>
<span data-ttu-id="aefa4-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aefa4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aefa4-124">-확장</span><span class="sxs-lookup"><span data-stu-id="aefa4-124">-Expand</span></span>
<span data-ttu-id="aefa4-125">출력 확장</span><span class="sxs-lookup"><span data-stu-id="aefa4-125">Expand output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefa4-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aefa4-126">-InputObject</span></span>
<span data-ttu-id="aefa4-127">PSProject 개체.</span><span class="sxs-lookup"><span data-stu-id="aefa4-127">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aefa4-128">-이름</span><span class="sxs-lookup"><span data-stu-id="aefa4-128">-Name</span></span>
<span data-ttu-id="aefa4-129">작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aefa4-129">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefa4-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="aefa4-130">-ProjectName</span></span>
<span data-ttu-id="aefa4-131">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aefa4-131">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefa4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aefa4-132">-ResourceGroupName</span></span>
<span data-ttu-id="aefa4-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aefa4-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefa4-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aefa4-134">-ResourceId</span></span>
<span data-ttu-id="aefa4-135">프로젝트 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="aefa4-135">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aefa4-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="aefa4-136">-ResultType</span></span>
<span data-ttu-id="aefa4-137">지정 된 결과 형식의 출력을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="aefa4-137">Expand output of given result type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput, LoginLevelOutput, AgentJobLevelOutput

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefa4-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="aefa4-138">-ServiceName</span></span>
<span data-ttu-id="aefa4-139">데이터베이스 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aefa4-139">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefa4-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="aefa4-140">-TaskType</span></span>
<span data-ttu-id="aefa4-141">TaskType을 기준으로 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="aefa4-141">Filter by TaskType.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum]
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefa4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aefa4-142">CommonParameters</span></span>
<span data-ttu-id="aefa4-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aefa4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aefa4-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aefa4-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aefa4-145">입력</span><span class="sxs-lookup"><span data-stu-id="aefa4-145">INPUTS</span></span>

### <span data-ttu-id="aefa4-146">DataMigration. a i m. PSProject</span><span class="sxs-lookup"><span data-stu-id="aefa4-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="aefa4-147">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aefa4-147">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="aefa4-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aefa4-148">System.String</span></span>

## <span data-ttu-id="aefa4-149">출력</span><span class="sxs-lookup"><span data-stu-id="aefa4-149">OUTPUTS</span></span>

### <span data-ttu-id="aefa4-150">DataMigration. a i m.</span><span class="sxs-lookup"><span data-stu-id="aefa4-150">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="aefa4-151">상속자</span><span class="sxs-lookup"><span data-stu-id="aefa4-151">NOTES</span></span>

## <span data-ttu-id="aefa4-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aefa4-152">RELATED LINKS</span></span>

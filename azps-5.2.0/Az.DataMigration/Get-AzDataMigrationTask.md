---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
ms.openlocfilehash: bcc1c39af722d5f12c333152e8458228f583a842
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327697"
---
# <span data-ttu-id="700f2-101">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="700f2-101">Get-AzDataMigrationTask</span></span>

## <span data-ttu-id="700f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="700f2-102">SYNOPSIS</span></span>
<span data-ttu-id="700f2-103">Azure Database Migration Service 마이그레이션 작업과 연결된 PSProjectTask 개체를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="700f2-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="700f2-104">구문</span><span class="sxs-lookup"><span data-stu-id="700f2-104">SYNTAX</span></span>

### <span data-ttu-id="700f2-105">ListByComponent(기본값)</span><span class="sxs-lookup"><span data-stu-id="700f2-105">ListByComponent (Default)</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="700f2-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="700f2-106">ListByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="700f2-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="700f2-107">GetByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="700f2-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="700f2-108">GetByInputObjectResultType</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="700f2-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="700f2-109">ListByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="700f2-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="700f2-110">GetByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="700f2-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="700f2-111">GetByResourceIdResultType</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="700f2-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="700f2-112">GetByComponent</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="700f2-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="700f2-113">GetByComponentResultType</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="700f2-114">설명</span><span class="sxs-lookup"><span data-stu-id="700f2-114">DESCRIPTION</span></span>
<span data-ttu-id="700f2-115">Get-AzDataMigrationTask cmdlet은 Azure Database Migration Service 마이그레이션 작업과 연결된 속성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="700f2-115">The Get-AzDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="700f2-116">예제</span><span class="sxs-lookup"><span data-stu-id="700f2-116">EXAMPLES</span></span>

### <span data-ttu-id="700f2-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="700f2-117">Example 1</span></span>
```
PS C:\> Get -AzDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="700f2-118">위의 예제에서는 Get-AzDataMigrationTask 매개 변수로 전달된 작업 이름에 따라 Azure Database Migration Service 마이그레이션 작업과 연결된 속성을 검색하는 데 Get-AzDataMigrationTask cmdlet을 사용하는 방법을 보여 주는 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="700f2-118">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="700f2-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="700f2-119">Example 2</span></span>
```
PS C:\> Get -AzDataMigrationTask -Project $myProject
```

<span data-ttu-id="700f2-120">위의 예제에서는 Get-AzDataMigrationTask 매개 변수로 전달된 PSProject 개체와 연결된 모든 마이그레이션 작업을 검색하기 위해 Get-AzDataMigrationTask cmdlet을 사용하는 방법을 보여 주는 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="700f2-120">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="700f2-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="700f2-121">PARAMETERS</span></span>

### <span data-ttu-id="700f2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="700f2-122">-DefaultProfile</span></span>
<span data-ttu-id="700f2-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="700f2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="700f2-124">-Expand</span><span class="sxs-lookup"><span data-stu-id="700f2-124">-Expand</span></span>
<span data-ttu-id="700f2-125">출력 확장</span><span class="sxs-lookup"><span data-stu-id="700f2-125">Expand output</span></span>

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

### <span data-ttu-id="700f2-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="700f2-126">-InputObject</span></span>
<span data-ttu-id="700f2-127">PSProject 개체.</span><span class="sxs-lookup"><span data-stu-id="700f2-127">PSProject Object.</span></span>

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

### <span data-ttu-id="700f2-128">-Name</span><span class="sxs-lookup"><span data-stu-id="700f2-128">-Name</span></span>
<span data-ttu-id="700f2-129">작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="700f2-129">The name of the task.</span></span>

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

### <span data-ttu-id="700f2-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="700f2-130">-ProjectName</span></span>
<span data-ttu-id="700f2-131">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="700f2-131">The name of the project.</span></span>

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

### <span data-ttu-id="700f2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="700f2-132">-ResourceGroupName</span></span>
<span data-ttu-id="700f2-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="700f2-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="700f2-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="700f2-134">-ResourceId</span></span>
<span data-ttu-id="700f2-135">프로젝트 자원 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="700f2-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="700f2-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="700f2-136">-ResultType</span></span>
<span data-ttu-id="700f2-137">주어진 결과 형식의 출력을 확장합니다.</span><span class="sxs-lookup"><span data-stu-id="700f2-137">Expand output of given result type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput, LoginLevelOutput, AgentJobLevelOutput, Command

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="700f2-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="700f2-138">-ServiceName</span></span>
<span data-ttu-id="700f2-139">Database Migration Service 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="700f2-139">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="700f2-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="700f2-140">-TaskType</span></span>
<span data-ttu-id="700f2-141">TaskType으로 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="700f2-141">Filter by TaskType.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum]
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="700f2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="700f2-142">CommonParameters</span></span>
<span data-ttu-id="700f2-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="700f2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="700f2-144">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="700f2-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="700f2-145">입력</span><span class="sxs-lookup"><span data-stu-id="700f2-145">INPUTS</span></span>

### <span data-ttu-id="700f2-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="700f2-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="700f2-147">System.String</span><span class="sxs-lookup"><span data-stu-id="700f2-147">System.String</span></span>

## <span data-ttu-id="700f2-148">출력</span><span class="sxs-lookup"><span data-stu-id="700f2-148">OUTPUTS</span></span>

### <span data-ttu-id="700f2-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="700f2-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="700f2-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="700f2-150">NOTES</span></span>

## <span data-ttu-id="700f2-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="700f2-151">RELATED LINKS</span></span>

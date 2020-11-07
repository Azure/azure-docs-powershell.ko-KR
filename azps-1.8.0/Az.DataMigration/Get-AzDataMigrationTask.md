---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
ms.openlocfilehash: 65330f1024820c725cfb9a6b142000866063dc37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701040"
---
# <span data-ttu-id="2511e-101">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="2511e-101">Get-AzDataMigrationTask</span></span>

## <span data-ttu-id="2511e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2511e-102">SYNOPSIS</span></span>
<span data-ttu-id="2511e-103">Azure 데이터베이스 마이그레이션 서비스 마이그레이션 작업과 연결 된 PSProjectTask 개체를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="2511e-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="2511e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2511e-104">SYNTAX</span></span>

### <span data-ttu-id="2511e-105">ListByComponent (기본값)</span><span class="sxs-lookup"><span data-stu-id="2511e-105">ListByComponent (Default)</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2511e-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="2511e-106">ListByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2511e-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="2511e-107">GetByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2511e-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="2511e-108">GetByInputObjectResultType</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2511e-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="2511e-109">ListByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2511e-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2511e-110">GetByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2511e-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="2511e-111">GetByResourceIdResultType</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2511e-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="2511e-112">GetByComponent</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2511e-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="2511e-113">GetByComponentResultType</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2511e-114">설명은</span><span class="sxs-lookup"><span data-stu-id="2511e-114">DESCRIPTION</span></span>
<span data-ttu-id="2511e-115">Get-AzDataMigrationTask cmdlet은 Azure 데이터베이스 마이그레이션 서비스 마이그레이션 작업과 연결 된 속성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="2511e-115">The Get-AzDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="2511e-116">예제의</span><span class="sxs-lookup"><span data-stu-id="2511e-116">EXAMPLES</span></span>

### <span data-ttu-id="2511e-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="2511e-117">Example 1</span></span>
```
PS C:\> Get -AzDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="2511e-118">위의 예제에서는 Get-AzDataMigrationTask cmdlet을 사용 하 여 입력 매개 변수로 전달 된 작업 이름을 기반으로 Azure 데이터베이스 마이그레이션 서비스 마이그레이션 작업과 연결 된 속성을 검색 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2511e-118">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="2511e-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="2511e-119">Example 2</span></span>
```
PS C:\> Get -AzDataMigrationTask -Project $myProject
```

<span data-ttu-id="2511e-120">위 예제에서는 Get-AzDataMigrationTask cmdlet을 사용 하 여 입력 매개 변수로 전달 된 PSProject 개체와 관련 된 모든 마이그레이션 작업을 검색 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2511e-120">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="2511e-121">변수</span><span class="sxs-lookup"><span data-stu-id="2511e-121">PARAMETERS</span></span>

### <span data-ttu-id="2511e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2511e-122">-DefaultProfile</span></span>
<span data-ttu-id="2511e-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2511e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2511e-124">-확장</span><span class="sxs-lookup"><span data-stu-id="2511e-124">-Expand</span></span>
<span data-ttu-id="2511e-125">출력 확장</span><span class="sxs-lookup"><span data-stu-id="2511e-125">Expand output</span></span>

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

### <span data-ttu-id="2511e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2511e-126">-InputObject</span></span>
<span data-ttu-id="2511e-127">PSProject 개체.</span><span class="sxs-lookup"><span data-stu-id="2511e-127">PSProject Object.</span></span>

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

### <span data-ttu-id="2511e-128">-이름</span><span class="sxs-lookup"><span data-stu-id="2511e-128">-Name</span></span>
<span data-ttu-id="2511e-129">작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2511e-129">The name of the task.</span></span>

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

### <span data-ttu-id="2511e-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="2511e-130">-ProjectName</span></span>
<span data-ttu-id="2511e-131">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2511e-131">The name of the project.</span></span>

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

### <span data-ttu-id="2511e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2511e-132">-ResourceGroupName</span></span>
<span data-ttu-id="2511e-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2511e-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="2511e-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2511e-134">-ResourceId</span></span>
<span data-ttu-id="2511e-135">프로젝트 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="2511e-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="2511e-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="2511e-136">-ResultType</span></span>
<span data-ttu-id="2511e-137">지정 된 결과 형식의 출력을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2511e-137">Expand output of given result type.</span></span>

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

### <span data-ttu-id="2511e-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2511e-138">-ServiceName</span></span>
<span data-ttu-id="2511e-139">데이터베이스 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2511e-139">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="2511e-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="2511e-140">-TaskType</span></span>
<span data-ttu-id="2511e-141">TaskType을 기준으로 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="2511e-141">Filter by TaskType.</span></span>

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

### <span data-ttu-id="2511e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2511e-142">CommonParameters</span></span>
<span data-ttu-id="2511e-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2511e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2511e-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2511e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2511e-145">입력</span><span class="sxs-lookup"><span data-stu-id="2511e-145">INPUTS</span></span>

### <span data-ttu-id="2511e-146">DataMigration. a i m. PSProject</span><span class="sxs-lookup"><span data-stu-id="2511e-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="2511e-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2511e-147">System.String</span></span>

## <span data-ttu-id="2511e-148">출력</span><span class="sxs-lookup"><span data-stu-id="2511e-148">OUTPUTS</span></span>

### <span data-ttu-id="2511e-149">DataMigration. a i m.</span><span class="sxs-lookup"><span data-stu-id="2511e-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="2511e-150">상속자</span><span class="sxs-lookup"><span data-stu-id="2511e-150">NOTES</span></span>

## <span data-ttu-id="2511e-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2511e-151">RELATED LINKS</span></span>
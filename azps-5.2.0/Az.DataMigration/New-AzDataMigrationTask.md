---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
ms.openlocfilehash: 0222900be337cfe9eab97da31fc9d2dd84744e43
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357666"
---
# <span data-ttu-id="4eb1f-101">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="4eb1f-101">New-AzDataMigrationTask</span></span>

## <span data-ttu-id="4eb1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eb1f-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb1f-103">Azure Database Migration Service에서 데이터 마이그레이션 작업을 만들고 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

## <span data-ttu-id="4eb1f-104">구문</span><span class="sxs-lookup"><span data-stu-id="4eb1f-104">SYNTAX</span></span>

### <span data-ttu-id="4eb1f-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4eb1f-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4eb1f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eb1f-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eb1f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eb1f-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eb1f-108">설명</span><span class="sxs-lookup"><span data-stu-id="4eb1f-108">DESCRIPTION</span></span>
<span data-ttu-id="4eb1f-109">New-AzDataMigrationTask cmdlet은 데이터 마이그레이션 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-109">The New-AzDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="4eb1f-110">이 cmdlet은 작업 유형 열기자, Azure 리소스 그룹, 연결된 Azure Database Migration Service의 이름 및 Project에 대한 매개 변수를 입력으로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="4eb1f-111">예제</span><span class="sxs-lookup"><span data-stu-id="4eb1f-111">EXAMPLES</span></span>

### <span data-ttu-id="4eb1f-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="4eb1f-112">Example 1</span></span>
```
PS C:\> New-AzDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs -MigrationValidation $validationTask
```

<span data-ttu-id="4eb1f-113">이 예제 스크립트는 myDMSProject라는 프로젝트 및 TestService라는 서비스에 MyMigrationTask라는 새 데이터 마이그레이션 작업을 만드는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="4eb1f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4eb1f-114">PARAMETERS</span></span>

### <span data-ttu-id="4eb1f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb1f-115">-DefaultProfile</span></span>
<span data-ttu-id="4eb1f-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4eb1f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4eb1f-117">-InputObject</span></span>
<span data-ttu-id="4eb1f-118">PSProject 개체.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-118">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4eb1f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4eb1f-119">-Name</span></span>
<span data-ttu-id="4eb1f-120">작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-120">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb1f-121">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="4eb1f-121">-ProjectName</span></span>
<span data-ttu-id="4eb1f-122">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-122">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb1f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eb1f-123">-ResourceGroupName</span></span>
<span data-ttu-id="4eb1f-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb1f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4eb1f-125">-ResourceId</span></span>
<span data-ttu-id="4eb1f-126">프로젝트 자원 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-126">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eb1f-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4eb1f-127">-ServiceName</span></span>
<span data-ttu-id="4eb1f-128">Database Migration Service 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-128">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb1f-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="4eb1f-129">-TaskType</span></span>
<span data-ttu-id="4eb1f-130">작업 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-130">Task Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync, ConnectToSourceMongoDb, ConnectToTargetMongoDb, MigrateMongoDb, ValidateMongoDbMigration, ConnectToTargetSqlDbMiSync, ValidateSqlServerSqlDbMiSync, MigrateSqlServerSqlDbMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb1f-131">-MigrationValidation</span><span class="sxs-lookup"><span data-stu-id="4eb1f-131">-MigrationValidation</span></span> 
<span data-ttu-id="4eb1f-132">유효성 검사 호출을 통해 작업 응답 개체는 선택 사항이지만 권장됩니다.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-132">Task response object by validation call, optional but recommended.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb1f-133">-Wait</span><span class="sxs-lookup"><span data-stu-id="4eb1f-133">-Wait</span></span>
<span data-ttu-id="4eb1f-134">작업이 완료될 때까지 기다릴지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-134">Whether to wait for task to finish.</span></span> <span data-ttu-id="4eb1f-135">플래그가 설정된 경우 태스크가 완료될까지 1초마다 검사하고 출력 또는 오류를 검사할 수 있는 작업 속성으로 돌아와야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-135">If the flag is set, checks every one seconds till the task finishes and return to user the task properties where output or error can be inspected.</span></span> 
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb1f-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4eb1f-136">-Confirm</span></span>
<span data-ttu-id="4eb1f-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eb1f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eb1f-138">-WhatIf</span></span>
<span data-ttu-id="4eb1f-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4eb1f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eb1f-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eb1f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb1f-141">CommonParameters</span></span>
<span data-ttu-id="4eb1f-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb1f-143">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb1f-144">입력</span><span class="sxs-lookup"><span data-stu-id="4eb1f-144">INPUTS</span></span>

### <span data-ttu-id="4eb1f-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="4eb1f-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="4eb1f-146">System.String</span><span class="sxs-lookup"><span data-stu-id="4eb1f-146">System.String</span></span>

## <span data-ttu-id="4eb1f-147">출력</span><span class="sxs-lookup"><span data-stu-id="4eb1f-147">OUTPUTS</span></span>

### <span data-ttu-id="4eb1f-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="4eb1f-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="4eb1f-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4eb1f-149">NOTES</span></span>

## <span data-ttu-id="4eb1f-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4eb1f-150">RELATED LINKS</span></span>

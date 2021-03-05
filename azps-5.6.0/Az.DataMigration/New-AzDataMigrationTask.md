---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
ms.openlocfilehash: 5e9e121e3210510ed073cacfe93d6ec196888db6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991396"
---
# <span data-ttu-id="996da-101">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="996da-101">New-AzDataMigrationTask</span></span>

## <span data-ttu-id="996da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="996da-102">SYNOPSIS</span></span>
<span data-ttu-id="996da-103">Azure Database Migration Service에서 데이터 마이그레이션 작업을 만들고 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="996da-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

## <span data-ttu-id="996da-104">구문</span><span class="sxs-lookup"><span data-stu-id="996da-104">SYNTAX</span></span>

### <span data-ttu-id="996da-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="996da-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="996da-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="996da-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="996da-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="996da-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="996da-108">설명</span><span class="sxs-lookup"><span data-stu-id="996da-108">DESCRIPTION</span></span>
<span data-ttu-id="996da-109">New-AzDataMigrationTask cmdlet은 데이터 마이그레이션 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="996da-109">The New-AzDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="996da-110">이 cmdlet은 작업 유형 열제기, Azure Resource Group, 연결된 Azure Database Migration Service 및 Project의 이름에 대한 매개 변수를 입력으로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="996da-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="996da-111">예제</span><span class="sxs-lookup"><span data-stu-id="996da-111">EXAMPLES</span></span>

### <span data-ttu-id="996da-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="996da-112">Example 1</span></span>
```
PS C:\> New-AzDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs -MigrationValidation $validationTask
```

<span data-ttu-id="996da-113">이 예제 스크립트는 myDMSProject라는 프로젝트에서 MyMigrationTask라는 새 데이터 마이그레이션 작업을 만들고 TestService라는 서비스를 만드는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="996da-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="996da-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="996da-114">PARAMETERS</span></span>

### <span data-ttu-id="996da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="996da-115">-DefaultProfile</span></span>
<span data-ttu-id="996da-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="996da-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="996da-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="996da-117">-InputObject</span></span>
<span data-ttu-id="996da-118">PSProject 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="996da-118">PSProject Object.</span></span>

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

### <span data-ttu-id="996da-119">-Name</span><span class="sxs-lookup"><span data-stu-id="996da-119">-Name</span></span>
<span data-ttu-id="996da-120">작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="996da-120">The name of the task.</span></span>

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

### <span data-ttu-id="996da-121">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="996da-121">-ProjectName</span></span>
<span data-ttu-id="996da-122">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="996da-122">The name of the project.</span></span>

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

### <span data-ttu-id="996da-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="996da-123">-ResourceGroupName</span></span>
<span data-ttu-id="996da-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="996da-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="996da-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="996da-125">-ResourceId</span></span>
<span data-ttu-id="996da-126">프로젝트 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="996da-126">Project Resource Id.</span></span>

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

### <span data-ttu-id="996da-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="996da-127">-ServiceName</span></span>
<span data-ttu-id="996da-128">데이터베이스 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="996da-128">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="996da-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="996da-129">-TaskType</span></span>
<span data-ttu-id="996da-130">작업 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="996da-130">Task Type.</span></span>

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

### <span data-ttu-id="996da-131">-MigrationValidation</span><span class="sxs-lookup"><span data-stu-id="996da-131">-MigrationValidation</span></span> 
<span data-ttu-id="996da-132">유효성 검사 호출을 통해 작업 응답 개체는 선택적이지만 권장됩니다.</span><span class="sxs-lookup"><span data-stu-id="996da-132">Task response object by validation call, optional but recommended.</span></span>

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

### <span data-ttu-id="996da-133">-Wait</span><span class="sxs-lookup"><span data-stu-id="996da-133">-Wait</span></span>
<span data-ttu-id="996da-134">작업이 완료될 때까지 기다릴지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="996da-134">Whether to wait for task to finish.</span></span> <span data-ttu-id="996da-135">플래그가 설정되어 있는 경우 작업이 완료될 때마다 1초마다 검사하고 출력 또는 오류를 검사할 수 있는 작업 속성을 사용자에게 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="996da-135">If the flag is set, checks every one seconds till the task finishes and return to user the task properties where output or error can be inspected.</span></span> 
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

### <span data-ttu-id="996da-136">-확인</span><span class="sxs-lookup"><span data-stu-id="996da-136">-Confirm</span></span>
<span data-ttu-id="996da-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="996da-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="996da-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="996da-138">-WhatIf</span></span>
<span data-ttu-id="996da-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="996da-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="996da-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="996da-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="996da-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="996da-141">CommonParameters</span></span>
<span data-ttu-id="996da-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="996da-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="996da-143">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="996da-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="996da-144">입력</span><span class="sxs-lookup"><span data-stu-id="996da-144">INPUTS</span></span>

### <span data-ttu-id="996da-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="996da-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="996da-146">System.String</span><span class="sxs-lookup"><span data-stu-id="996da-146">System.String</span></span>

## <span data-ttu-id="996da-147">출력</span><span class="sxs-lookup"><span data-stu-id="996da-147">OUTPUTS</span></span>

### <span data-ttu-id="996da-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="996da-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="996da-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="996da-149">NOTES</span></span>

## <span data-ttu-id="996da-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="996da-150">RELATED LINKS</span></span>

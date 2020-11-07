---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
ms.openlocfilehash: 0222900be337cfe9eab97da31fc9d2dd84744e43
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877545"
---
# <span data-ttu-id="c4dd1-101">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="c4dd1-101">New-AzDataMigrationTask</span></span>

## <span data-ttu-id="c4dd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4dd1-102">SYNOPSIS</span></span>
<span data-ttu-id="c4dd1-103">Azure 데이터베이스 마이그레이션 서비스에서 데이터 마이그레이션 작업을 만들고 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

## <span data-ttu-id="c4dd1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c4dd1-104">SYNTAX</span></span>

### <span data-ttu-id="c4dd1-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c4dd1-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4dd1-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4dd1-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4dd1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4dd1-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4dd1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c4dd1-108">DESCRIPTION</span></span>
<span data-ttu-id="c4dd1-109">New-AzDataMigrationTask cmdlet은 데이터 마이그레이션 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-109">The New-AzDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="c4dd1-110">이 cmdlet은 작업 유형 열거자, Azure 리소스 그룹, 연결 된 Azure 데이터베이스 마이그레이션 서비스의 이름 및 프로젝트의 입력에 대 한 매개 변수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="c4dd1-111">예제의</span><span class="sxs-lookup"><span data-stu-id="c4dd1-111">EXAMPLES</span></span>

### <span data-ttu-id="c4dd1-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="c4dd1-112">Example 1</span></span>
```
PS C:\> New-AzDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs -MigrationValidation $validationTask
```

<span data-ttu-id="c4dd1-113">이 예제 스크립트는 myDMSProject 및 TestService 라는 프로젝트에서 MyMigrationTask 이라는 새 데이터 마이그레이션 작업을 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="c4dd1-114">변수</span><span class="sxs-lookup"><span data-stu-id="c4dd1-114">PARAMETERS</span></span>

### <span data-ttu-id="c4dd1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4dd1-115">-DefaultProfile</span></span>
<span data-ttu-id="c4dd1-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4dd1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4dd1-117">-InputObject</span></span>
<span data-ttu-id="c4dd1-118">PSProject 개체.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-118">PSProject Object.</span></span>

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

### <span data-ttu-id="c4dd1-119">-이름</span><span class="sxs-lookup"><span data-stu-id="c4dd1-119">-Name</span></span>
<span data-ttu-id="c4dd1-120">작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-120">The name of the task.</span></span>

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

### <span data-ttu-id="c4dd1-121">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="c4dd1-121">-ProjectName</span></span>
<span data-ttu-id="c4dd1-122">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-122">The name of the project.</span></span>

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

### <span data-ttu-id="c4dd1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4dd1-123">-ResourceGroupName</span></span>
<span data-ttu-id="c4dd1-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="c4dd1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4dd1-125">-ResourceId</span></span>
<span data-ttu-id="c4dd1-126">프로젝트 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-126">Project Resource Id.</span></span>

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

### <span data-ttu-id="c4dd1-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c4dd1-127">-ServiceName</span></span>
<span data-ttu-id="c4dd1-128">데이터베이스 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-128">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="c4dd1-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="c4dd1-129">-TaskType</span></span>
<span data-ttu-id="c4dd1-130">작업 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-130">Task Type.</span></span>

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

### <span data-ttu-id="c4dd1-131">-MigrationValidation</span><span class="sxs-lookup"><span data-stu-id="c4dd1-131">-MigrationValidation</span></span> 
<span data-ttu-id="c4dd1-132">유효성 검사 호출 별 작업 응답 개체, 선택 사항 이지만 권장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-132">Task response object by validation call, optional but recommended.</span></span>

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

### <span data-ttu-id="c4dd1-133">-대기</span><span class="sxs-lookup"><span data-stu-id="c4dd1-133">-Wait</span></span>
<span data-ttu-id="c4dd1-134">작업이 완료 될 때까지 기다릴지 여부</span><span class="sxs-lookup"><span data-stu-id="c4dd1-134">Whether to wait for task to finish.</span></span> <span data-ttu-id="c4dd1-135">플래그가 설정 된 경우 작업이 완료 될 때까지 1 초 마다 확인 하 고, 출력이 나 오류를 검사할 수 있는 작업 속성을 사용자에 게 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-135">If the flag is set, checks every one seconds till the task finishes and return to user the task properties where output or error can be inspected.</span></span> 
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

### <span data-ttu-id="c4dd1-136">-확인</span><span class="sxs-lookup"><span data-stu-id="c4dd1-136">-Confirm</span></span>
<span data-ttu-id="c4dd1-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4dd1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4dd1-138">-WhatIf</span></span>
<span data-ttu-id="c4dd1-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4dd1-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4dd1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4dd1-141">CommonParameters</span></span>
<span data-ttu-id="c4dd1-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4dd1-143">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4dd1-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4dd1-144">입력</span><span class="sxs-lookup"><span data-stu-id="c4dd1-144">INPUTS</span></span>

### <span data-ttu-id="c4dd1-145">DataMigration. a i m. PSProject</span><span class="sxs-lookup"><span data-stu-id="c4dd1-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="c4dd1-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c4dd1-146">System.String</span></span>

## <span data-ttu-id="c4dd1-147">출력</span><span class="sxs-lookup"><span data-stu-id="c4dd1-147">OUTPUTS</span></span>

### <span data-ttu-id="c4dd1-148">DataMigration. a i m.</span><span class="sxs-lookup"><span data-stu-id="c4dd1-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="c4dd1-149">상속자</span><span class="sxs-lookup"><span data-stu-id="c4dd1-149">NOTES</span></span>

## <span data-ttu-id="c4dd1-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4dd1-150">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
ms.openlocfilehash: 1bdf66311acd1b8ff1de43b5ea199d5d0a17c394
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702649"
---
# <span data-ttu-id="10d25-101">New-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="10d25-101">New-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="10d25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10d25-102">SYNOPSIS</span></span>
<span data-ttu-id="10d25-103">Azure 데이터베이스 마이그레이션 서비스에서 데이터 마이그레이션 작업을 만들고 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="10d25-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10d25-104">구문과</span><span class="sxs-lookup"><span data-stu-id="10d25-104">SYNTAX</span></span>

### <span data-ttu-id="10d25-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="10d25-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="10d25-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10d25-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="10d25-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10d25-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="10d25-108">설명은</span><span class="sxs-lookup"><span data-stu-id="10d25-108">DESCRIPTION</span></span>
<span data-ttu-id="10d25-109">New-AzureRmDataMigrationTask cmdlet은 데이터 마이그레이션 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="10d25-109">The New-AzureRmDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="10d25-110">이 cmdlet은 작업 유형 열거자, Azure 리소스 그룹, 연결 된 Azure 데이터 마이그레이션 서비스의 이름 및 프로젝트의 입력에 대 한 매개 변수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="10d25-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Data Migration Service and Project as input.</span></span> 

## <span data-ttu-id="10d25-111">예제의</span><span class="sxs-lookup"><span data-stu-id="10d25-111">EXAMPLES</span></span>

### <span data-ttu-id="10d25-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="10d25-112">Example 1</span></span>
```
PS C:\> New-AzureRmDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs
```
<span data-ttu-id="10d25-113">이 예제 스크립트는 myDMSProject 및 TestService 라는 프로젝트에서 MyMigrationTask 이라는 새 데이터 마이그레이션 작업을 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="10d25-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="10d25-114">변수</span><span class="sxs-lookup"><span data-stu-id="10d25-114">PARAMETERS</span></span>

### <span data-ttu-id="10d25-115">-확인</span><span class="sxs-lookup"><span data-stu-id="10d25-115">-Confirm</span></span>
<span data-ttu-id="10d25-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="10d25-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10d25-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10d25-117">-DefaultProfile</span></span>
<span data-ttu-id="10d25-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10d25-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10d25-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10d25-119">-InputObject</span></span>
<span data-ttu-id="10d25-120">PSProject 개체.</span><span class="sxs-lookup"><span data-stu-id="10d25-120">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10d25-121">-이름</span><span class="sxs-lookup"><span data-stu-id="10d25-121">-Name</span></span>
<span data-ttu-id="10d25-122">작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10d25-122">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d25-123">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="10d25-123">-ProjectName</span></span>
<span data-ttu-id="10d25-124">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10d25-124">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d25-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10d25-125">-ResourceGroupName</span></span>
<span data-ttu-id="10d25-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10d25-126">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d25-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10d25-127">-ResourceId</span></span>
<span data-ttu-id="10d25-128">프로젝트 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="10d25-128">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10d25-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="10d25-129">-ServiceName</span></span>
<span data-ttu-id="10d25-130">데이터 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10d25-130">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d25-131">-TaskType</span><span class="sxs-lookup"><span data-stu-id="10d25-131">-TaskType</span></span>
<span data-ttu-id="10d25-132">작업 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="10d25-132">Task Type.</span></span>

```yaml
Type: TaskTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d25-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10d25-133">-WhatIf</span></span>
<span data-ttu-id="10d25-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="10d25-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10d25-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10d25-135">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="10d25-136">입력</span><span class="sxs-lookup"><span data-stu-id="10d25-136">INPUTS</span></span>

### <span data-ttu-id="10d25-137">DataMigration. a i m. PSProject</span><span class="sxs-lookup"><span data-stu-id="10d25-137">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="10d25-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="10d25-138">System.String</span></span>


## <span data-ttu-id="10d25-139">출력</span><span class="sxs-lookup"><span data-stu-id="10d25-139">OUTPUTS</span></span>

### <span data-ttu-id="10d25-140">DataMigration. a i m.</span><span class="sxs-lookup"><span data-stu-id="10d25-140">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>


## <span data-ttu-id="10d25-141">상속자</span><span class="sxs-lookup"><span data-stu-id="10d25-141">NOTES</span></span>

## <span data-ttu-id="10d25-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10d25-142">RELATED LINKS</span></span>



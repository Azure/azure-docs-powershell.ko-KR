---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
ms.openlocfilehash: d192b7f422557b4d4373f794e98cdb2556db3c63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531723"
---
# <span data-ttu-id="f6953-101">Remove-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="f6953-101">Remove-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="f6953-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6953-102">SYNOPSIS</span></span>
<span data-ttu-id="f6953-103">Azure에서 Azure 데이터베이스 마이그레이션 서비스 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6953-103">Removes an Azure Database Migration Service task from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6953-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f6953-104">SYNTAX</span></span>

### <span data-ttu-id="f6953-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f6953-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f6953-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6953-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f6953-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6953-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f6953-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f6953-108">DESCRIPTION</span></span>
<span data-ttu-id="f6953-109">Remove-AzureRmDataMigrationTask cmdlet은 Azure에서 Azure 데이터베이스 마이그레이션 서비스 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6953-109">The Remove-AzureRmDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="f6953-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f6953-110">EXAMPLES</span></span>

### <span data-ttu-id="f6953-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f6953-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask –TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup

```

<span data-ttu-id="f6953-112">앞의 예제에서는 작업 이름 매개 변수를 기준으로 Azure에서 TestTask 라는 Azure 데이터베이스 마이그레이션 서비스 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6953-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="f6953-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="f6953-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask –InputObject $TestTask

```

<span data-ttu-id="f6953-114">앞의 예제에서는 전달 된 PSProjectTask 개체를 기반으로 하는 Azure 데이터베이스 마이그레이션 서비스 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6953-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="f6953-115">변수</span><span class="sxs-lookup"><span data-stu-id="f6953-115">PARAMETERS</span></span>

### <span data-ttu-id="f6953-116">-확인</span><span class="sxs-lookup"><span data-stu-id="f6953-116">-Confirm</span></span>
<span data-ttu-id="f6953-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6953-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6953-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6953-118">-DefaultProfile</span></span>
<span data-ttu-id="f6953-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f6953-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6953-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f6953-120">-Force</span></span>
<span data-ttu-id="f6953-121">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="f6953-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="f6953-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6953-122">-InputObject</span></span>
<span data-ttu-id="f6953-123">PSProjectTask 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f6953-123">PSProjectTask Object.</span></span>

```yaml
Type: PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6953-124">-이름</span><span class="sxs-lookup"><span data-stu-id="f6953-124">-Name</span></span>
<span data-ttu-id="f6953-125">작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f6953-125">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6953-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6953-126">-PassThru</span></span>
<span data-ttu-id="f6953-127">True/false를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6953-127">Returns an true/false.</span></span>
<span data-ttu-id="f6953-128">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f6953-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f6953-129">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="f6953-129">-ProjectName</span></span>
<span data-ttu-id="f6953-130">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f6953-130">The name of the project.</span></span>

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

### <span data-ttu-id="f6953-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6953-131">-ResourceGroupName</span></span>
<span data-ttu-id="f6953-132">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f6953-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="f6953-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6953-133">-ResourceId</span></span>
<span data-ttu-id="f6953-134">프로젝트 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="f6953-134">Project Resource Id.</span></span>

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

### <span data-ttu-id="f6953-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f6953-135">-ServiceName</span></span>
<span data-ttu-id="f6953-136">데이터 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f6953-136">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="f6953-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6953-137">-WhatIf</span></span>
<span data-ttu-id="f6953-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f6953-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6953-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f6953-139">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="f6953-140">입력</span><span class="sxs-lookup"><span data-stu-id="f6953-140">INPUTS</span></span>

### <span data-ttu-id="f6953-141">DataMigration. a i m.</span><span class="sxs-lookup"><span data-stu-id="f6953-141">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="f6953-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f6953-142">System.String</span></span>


## <span data-ttu-id="f6953-143">출력</span><span class="sxs-lookup"><span data-stu-id="f6953-143">OUTPUTS</span></span>

### <span data-ttu-id="f6953-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f6953-144">System.Boolean</span></span>


## <span data-ttu-id="f6953-145">상속자</span><span class="sxs-lookup"><span data-stu-id="f6953-145">NOTES</span></span>

## <span data-ttu-id="f6953-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6953-146">RELATED LINKS</span></span>



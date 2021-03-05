---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Remove-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
ms.openlocfilehash: acb7e9b453b94381f4f5a2a0edf49e32258809ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996758"
---
# <span data-ttu-id="1dbdf-101">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="1dbdf-101">Remove-AzDataMigrationTask</span></span>

## <span data-ttu-id="1dbdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dbdf-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbdf-103">Azure에서 Azure Database Migration Service 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1dbdf-103">Removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="1dbdf-104">구문</span><span class="sxs-lookup"><span data-stu-id="1dbdf-104">SYNTAX</span></span>

### <span data-ttu-id="1dbdf-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1dbdf-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1dbdf-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dbdf-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dbdf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dbdf-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dbdf-108">설명</span><span class="sxs-lookup"><span data-stu-id="1dbdf-108">DESCRIPTION</span></span>
<span data-ttu-id="1dbdf-109">Remove-AzDataMigrationTask cmdlet은 Azure에서 Azure Database Migration Service 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1dbdf-109">The Remove-AzDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="1dbdf-110">예제</span><span class="sxs-lookup"><span data-stu-id="1dbdf-110">EXAMPLES</span></span>

### <span data-ttu-id="1dbdf-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1dbdf-111">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="1dbdf-112">이전 예제에서는 작업 이름 매개 변수를 기반으로 Azure에서 TestTask라는 Azure Database Migration Service 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1dbdf-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="1dbdf-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="1dbdf-113">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="1dbdf-114">위의 예제에서는 전달된 PSProjectTask 개체를 기반으로 Azure Database Migration Service 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1dbdf-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="1dbdf-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1dbdf-115">PARAMETERS</span></span>

### <span data-ttu-id="1dbdf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbdf-116">-DefaultProfile</span></span>
<span data-ttu-id="1dbdf-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1dbdf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dbdf-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1dbdf-118">-Force</span></span>
<span data-ttu-id="1dbdf-119">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="1dbdf-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1dbdf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dbdf-120">-InputObject</span></span>
<span data-ttu-id="1dbdf-121">PSProjectTask 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1dbdf-121">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbdf-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1dbdf-122">-Name</span></span>
<span data-ttu-id="1dbdf-123">작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1dbdf-123">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbdf-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1dbdf-124">-PassThru</span></span>
<span data-ttu-id="1dbdf-125">true/false를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1dbdf-125">Returns an true/false.</span></span>
<span data-ttu-id="1dbdf-126">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dbdf-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1dbdf-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="1dbdf-127">-ProjectName</span></span>
<span data-ttu-id="1dbdf-128">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1dbdf-128">The name of the project.</span></span>

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

### <span data-ttu-id="1dbdf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dbdf-129">-ResourceGroupName</span></span>
<span data-ttu-id="1dbdf-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1dbdf-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="1dbdf-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dbdf-131">-ResourceId</span></span>
<span data-ttu-id="1dbdf-132">프로젝트 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1dbdf-132">Project Resource Id.</span></span>

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

### <span data-ttu-id="1dbdf-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1dbdf-133">-ServiceName</span></span>
<span data-ttu-id="1dbdf-134">데이터베이스 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1dbdf-134">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="1dbdf-135">-확인</span><span class="sxs-lookup"><span data-stu-id="1dbdf-135">-Confirm</span></span>
<span data-ttu-id="1dbdf-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dbdf-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dbdf-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dbdf-137">-WhatIf</span></span>
<span data-ttu-id="1dbdf-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1dbdf-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dbdf-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dbdf-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dbdf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbdf-140">CommonParameters</span></span>
<span data-ttu-id="1dbdf-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1dbdf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbdf-142">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1dbdf-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbdf-143">입력</span><span class="sxs-lookup"><span data-stu-id="1dbdf-143">INPUTS</span></span>

### <span data-ttu-id="1dbdf-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="1dbdf-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="1dbdf-145">System.String</span><span class="sxs-lookup"><span data-stu-id="1dbdf-145">System.String</span></span>

## <span data-ttu-id="1dbdf-146">출력</span><span class="sxs-lookup"><span data-stu-id="1dbdf-146">OUTPUTS</span></span>

### <span data-ttu-id="1dbdf-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1dbdf-147">System.Boolean</span></span>

## <span data-ttu-id="1dbdf-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1dbdf-148">NOTES</span></span>

## <span data-ttu-id="1dbdf-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1dbdf-149">RELATED LINKS</span></span>

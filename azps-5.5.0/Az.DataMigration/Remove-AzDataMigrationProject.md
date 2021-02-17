---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
ms.openlocfilehash: f45134cae9c77108aca4084470fd7f919fde02a4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180849"
---
# <span data-ttu-id="14fd0-101">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="14fd0-101">Remove-AzDataMigrationProject</span></span>

## <span data-ttu-id="14fd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="14fd0-103">Azure에서 Azure Database Migration Service 프로젝트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="14fd0-103">Removes an Azure Database Migration Service project from Azure.</span></span>

## <span data-ttu-id="14fd0-104">구문</span><span class="sxs-lookup"><span data-stu-id="14fd0-104">SYNTAX</span></span>

### <span data-ttu-id="14fd0-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="14fd0-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14fd0-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14fd0-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14fd0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14fd0-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14fd0-108">설명</span><span class="sxs-lookup"><span data-stu-id="14fd0-108">DESCRIPTION</span></span>
<span data-ttu-id="14fd0-109">이 Remove-AzDataMigrationProject cmdlet은 Azure에서 Azure Database Migration Service 프로젝트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="14fd0-109">The Remove-AzDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="14fd0-110">DeleteRunningTask 매개 변수를 제공하면 제거되는 프로젝트와 연결된 모든 Azure Database Migration Service 작업이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="14fd0-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="14fd0-111">예제</span><span class="sxs-lookup"><span data-stu-id="14fd0-111">EXAMPLES</span></span>

### <span data-ttu-id="14fd0-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="14fd0-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="14fd0-113">위의 예제에서는 입력 매개 변수로 이름을 기반으로 Azure에서 myDMProject라는 Azure Database Migration Service 프로젝트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="14fd0-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="14fd0-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="14fd0-114">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="14fd0-115">위의 예제에서는 PSProject 개체를 기반으로 하는 Azure Database Migration Service 프로젝트를 입력 매개 변수로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="14fd0-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="14fd0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14fd0-116">PARAMETERS</span></span>

### <span data-ttu-id="14fd0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14fd0-117">-DefaultProfile</span></span>
<span data-ttu-id="14fd0-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14fd0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14fd0-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="14fd0-119">-DeleteRunningTask</span></span>
<span data-ttu-id="14fd0-120">실행 중인 모든 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="14fd0-120">Delete any running task</span></span>

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

### <span data-ttu-id="14fd0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="14fd0-121">-Force</span></span>
<span data-ttu-id="14fd0-122">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="14fd0-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="14fd0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14fd0-123">-InputObject</span></span>
<span data-ttu-id="14fd0-124">PSProject 개체.</span><span class="sxs-lookup"><span data-stu-id="14fd0-124">PSProject Object.</span></span>

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

### <span data-ttu-id="14fd0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="14fd0-125">-Name</span></span>
<span data-ttu-id="14fd0-126">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14fd0-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14fd0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14fd0-127">-PassThru</span></span>
<span data-ttu-id="14fd0-128">true/false를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="14fd0-128">Returns an true/false.</span></span>
<span data-ttu-id="14fd0-129">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14fd0-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="14fd0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14fd0-130">-ResourceGroupName</span></span>
<span data-ttu-id="14fd0-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14fd0-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="14fd0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14fd0-132">-ResourceId</span></span>
<span data-ttu-id="14fd0-133">프로젝트 자원 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="14fd0-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="14fd0-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="14fd0-134">-ServiceName</span></span>
<span data-ttu-id="14fd0-135">Database Migration Service 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14fd0-135">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="14fd0-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14fd0-136">-Confirm</span></span>
<span data-ttu-id="14fd0-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="14fd0-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14fd0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14fd0-138">-WhatIf</span></span>
<span data-ttu-id="14fd0-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="14fd0-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14fd0-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14fd0-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14fd0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14fd0-141">CommonParameters</span></span>
<span data-ttu-id="14fd0-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="14fd0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14fd0-143">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="14fd0-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14fd0-144">입력</span><span class="sxs-lookup"><span data-stu-id="14fd0-144">INPUTS</span></span>

### <span data-ttu-id="14fd0-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="14fd0-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="14fd0-146">System.String</span><span class="sxs-lookup"><span data-stu-id="14fd0-146">System.String</span></span>

## <span data-ttu-id="14fd0-147">출력</span><span class="sxs-lookup"><span data-stu-id="14fd0-147">OUTPUTS</span></span>

### <span data-ttu-id="14fd0-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="14fd0-148">System.Boolean</span></span>

## <span data-ttu-id="14fd0-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="14fd0-149">NOTES</span></span>

## <span data-ttu-id="14fd0-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14fd0-150">RELATED LINKS</span></span>

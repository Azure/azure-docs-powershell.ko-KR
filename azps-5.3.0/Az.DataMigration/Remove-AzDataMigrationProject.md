---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
ms.openlocfilehash: f45134cae9c77108aca4084470fd7f919fde02a4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377623"
---
# <span data-ttu-id="01e83-101">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="01e83-101">Remove-AzDataMigrationProject</span></span>

## <span data-ttu-id="01e83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01e83-102">SYNOPSIS</span></span>
<span data-ttu-id="01e83-103">Azure에서 Azure Database Migration Service 프로젝트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="01e83-103">Removes an Azure Database Migration Service project from Azure.</span></span>

## <span data-ttu-id="01e83-104">구문</span><span class="sxs-lookup"><span data-stu-id="01e83-104">SYNTAX</span></span>

### <span data-ttu-id="01e83-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="01e83-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01e83-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01e83-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01e83-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01e83-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01e83-108">설명</span><span class="sxs-lookup"><span data-stu-id="01e83-108">DESCRIPTION</span></span>
<span data-ttu-id="01e83-109">이 Remove-AzDataMigrationProject cmdlet은 Azure에서 Azure Database Migration Service 프로젝트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="01e83-109">The Remove-AzDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="01e83-110">DeleteRunningTask 매개 변수를 제공하면 제거되는 프로젝트와 연결된 모든 Azure Database Migration Service 작업이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="01e83-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="01e83-111">예제</span><span class="sxs-lookup"><span data-stu-id="01e83-111">EXAMPLES</span></span>

### <span data-ttu-id="01e83-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="01e83-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="01e83-113">위의 예제에서는 입력 매개 변수로 이름을 기반으로 Azure에서 myDMProject라는 Azure Database Migration Service 프로젝트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="01e83-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="01e83-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="01e83-114">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="01e83-115">위의 예제에서는 PSProject 개체를 기반으로 하는 Azure Database Migration Service 프로젝트를 입력 매개 변수로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="01e83-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="01e83-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01e83-116">PARAMETERS</span></span>

### <span data-ttu-id="01e83-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01e83-117">-DefaultProfile</span></span>
<span data-ttu-id="01e83-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01e83-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01e83-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="01e83-119">-DeleteRunningTask</span></span>
<span data-ttu-id="01e83-120">실행 중인 모든 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="01e83-120">Delete any running task</span></span>

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

### <span data-ttu-id="01e83-121">-Force</span><span class="sxs-lookup"><span data-stu-id="01e83-121">-Force</span></span>
<span data-ttu-id="01e83-122">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="01e83-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="01e83-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01e83-123">-InputObject</span></span>
<span data-ttu-id="01e83-124">PSProject 개체.</span><span class="sxs-lookup"><span data-stu-id="01e83-124">PSProject Object.</span></span>

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

### <span data-ttu-id="01e83-125">-Name</span><span class="sxs-lookup"><span data-stu-id="01e83-125">-Name</span></span>
<span data-ttu-id="01e83-126">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01e83-126">The name of the project.</span></span>

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

### <span data-ttu-id="01e83-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01e83-127">-PassThru</span></span>
<span data-ttu-id="01e83-128">true/false를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="01e83-128">Returns an true/false.</span></span>
<span data-ttu-id="01e83-129">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01e83-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="01e83-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01e83-130">-ResourceGroupName</span></span>
<span data-ttu-id="01e83-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01e83-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="01e83-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01e83-132">-ResourceId</span></span>
<span data-ttu-id="01e83-133">프로젝트 자원 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="01e83-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="01e83-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="01e83-134">-ServiceName</span></span>
<span data-ttu-id="01e83-135">Database Migration Service 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01e83-135">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="01e83-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01e83-136">-Confirm</span></span>
<span data-ttu-id="01e83-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="01e83-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01e83-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01e83-138">-WhatIf</span></span>
<span data-ttu-id="01e83-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="01e83-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01e83-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01e83-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01e83-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01e83-141">CommonParameters</span></span>
<span data-ttu-id="01e83-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="01e83-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01e83-143">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="01e83-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01e83-144">입력</span><span class="sxs-lookup"><span data-stu-id="01e83-144">INPUTS</span></span>

### <span data-ttu-id="01e83-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="01e83-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="01e83-146">System.String</span><span class="sxs-lookup"><span data-stu-id="01e83-146">System.String</span></span>

## <span data-ttu-id="01e83-147">출력</span><span class="sxs-lookup"><span data-stu-id="01e83-147">OUTPUTS</span></span>

### <span data-ttu-id="01e83-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="01e83-148">System.Boolean</span></span>

## <span data-ttu-id="01e83-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="01e83-149">NOTES</span></span>

## <span data-ttu-id="01e83-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01e83-150">RELATED LINKS</span></span>

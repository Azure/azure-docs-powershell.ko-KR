---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Remove-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
ms.openlocfilehash: 449a1cfc3156b647eccee6fc320f41fa9e53549c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010608"
---
# <span data-ttu-id="151e8-101">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="151e8-101">Remove-AzDataMigrationProject</span></span>

## <span data-ttu-id="151e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="151e8-102">SYNOPSIS</span></span>
<span data-ttu-id="151e8-103">Azure에서 Azure Database Migration Service 프로젝트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="151e8-103">Removes an Azure Database Migration Service project from Azure.</span></span>

## <span data-ttu-id="151e8-104">구문</span><span class="sxs-lookup"><span data-stu-id="151e8-104">SYNTAX</span></span>

### <span data-ttu-id="151e8-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="151e8-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="151e8-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="151e8-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="151e8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="151e8-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="151e8-108">설명</span><span class="sxs-lookup"><span data-stu-id="151e8-108">DESCRIPTION</span></span>
<span data-ttu-id="151e8-109">Remove-AzDataMigrationProject cmdlet은 Azure에서 Azure Database Migration Service 프로젝트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="151e8-109">The Remove-AzDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="151e8-110">DeleteRunningTask 매개 변수를 제공하면 제거되는 프로젝트와 연결된 모든 Azure Database Migration Service 작업이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="151e8-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="151e8-111">예제</span><span class="sxs-lookup"><span data-stu-id="151e8-111">EXAMPLES</span></span>

### <span data-ttu-id="151e8-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="151e8-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="151e8-113">위의 예제에서는 입력 매개 변수로 이름을 기반으로 Azure에서 myDMProject라는 Azure Database Migration Service 프로젝트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="151e8-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="151e8-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="151e8-114">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="151e8-115">위의 예제에서는 PSProject 개체를 기반으로 하는 Azure Database Migration Service 프로젝트를 입력 매개 변수로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="151e8-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="151e8-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="151e8-116">PARAMETERS</span></span>

### <span data-ttu-id="151e8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="151e8-117">-DefaultProfile</span></span>
<span data-ttu-id="151e8-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="151e8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="151e8-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="151e8-119">-DeleteRunningTask</span></span>
<span data-ttu-id="151e8-120">실행 중인 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="151e8-120">Delete any running task</span></span>

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

### <span data-ttu-id="151e8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="151e8-121">-Force</span></span>
<span data-ttu-id="151e8-122">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="151e8-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="151e8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="151e8-123">-InputObject</span></span>
<span data-ttu-id="151e8-124">PSProject 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="151e8-124">PSProject Object.</span></span>

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

### <span data-ttu-id="151e8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="151e8-125">-Name</span></span>
<span data-ttu-id="151e8-126">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="151e8-126">The name of the project.</span></span>

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

### <span data-ttu-id="151e8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="151e8-127">-PassThru</span></span>
<span data-ttu-id="151e8-128">true/false를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="151e8-128">Returns an true/false.</span></span>
<span data-ttu-id="151e8-129">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="151e8-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="151e8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="151e8-130">-ResourceGroupName</span></span>
<span data-ttu-id="151e8-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="151e8-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="151e8-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="151e8-132">-ResourceId</span></span>
<span data-ttu-id="151e8-133">프로젝트 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="151e8-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="151e8-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="151e8-134">-ServiceName</span></span>
<span data-ttu-id="151e8-135">데이터베이스 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="151e8-135">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="151e8-136">-확인</span><span class="sxs-lookup"><span data-stu-id="151e8-136">-Confirm</span></span>
<span data-ttu-id="151e8-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="151e8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="151e8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="151e8-138">-WhatIf</span></span>
<span data-ttu-id="151e8-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="151e8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="151e8-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="151e8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="151e8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="151e8-141">CommonParameters</span></span>
<span data-ttu-id="151e8-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="151e8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="151e8-143">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="151e8-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="151e8-144">입력</span><span class="sxs-lookup"><span data-stu-id="151e8-144">INPUTS</span></span>

### <span data-ttu-id="151e8-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="151e8-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="151e8-146">System.String</span><span class="sxs-lookup"><span data-stu-id="151e8-146">System.String</span></span>

## <span data-ttu-id="151e8-147">출력</span><span class="sxs-lookup"><span data-stu-id="151e8-147">OUTPUTS</span></span>

### <span data-ttu-id="151e8-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="151e8-148">System.Boolean</span></span>

## <span data-ttu-id="151e8-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="151e8-149">NOTES</span></span>

## <span data-ttu-id="151e8-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="151e8-150">RELATED LINKS</span></span>

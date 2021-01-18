---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E3D7A3FE-40D4-4495-BA39-493F85F304AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsapplicationinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
ms.openlocfilehash: 0f238a417ac83cac82305ceb9c9ce20586328976
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496348"
---
# <span data-ttu-id="44146-101">New-AzOperationalInsightsApplicationInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="44146-101">New-AzOperationalInsightsApplicationInsightsDataSource</span></span>

## <span data-ttu-id="44146-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44146-102">SYNOPSIS</span></span>
<span data-ttu-id="44146-103">주어진 애플리케이션에서 로그를 Application-Insights 수집합니다.</span><span class="sxs-lookup"><span data-stu-id="44146-103">Collect logs from given Application-Insights application.</span></span>

## <span data-ttu-id="44146-104">구문</span><span class="sxs-lookup"><span data-stu-id="44146-104">SYNTAX</span></span>

### <span data-ttu-id="44146-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="44146-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44146-106">ByWorkspaceObjectByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="44146-106">ByWorkspaceObjectByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44146-107">ByWorkspaceObjectByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="44146-107">ByWorkspaceObjectByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44146-108">ByWorkspaceNameByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="44146-108">ByWorkspaceNameByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44146-109">ByWorkspaceNameByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="44146-109">ByWorkspaceNameByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44146-110">설명</span><span class="sxs-lookup"><span data-stu-id="44146-110">DESCRIPTION</span></span>
<span data-ttu-id="44146-111">**New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet을 사용하면 주어진 Application-Insights 애플리케이션에서 로그를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44146-111">The **New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet enables the collection of logs from a given Application-Insights application.</span></span>

## <span data-ttu-id="44146-112">예제</span><span class="sxs-lookup"><span data-stu-id="44146-112">EXAMPLES</span></span>

### <span data-ttu-id="44146-113">예제 1: 작업 영역의 application-insights 데이터 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="44146-113">Example 1: Create application-insights data source in workspace</span></span>
```
PS C:\> New-AzOperationalInsightsApplicationInsightsDataSource -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -ApplicationSubscriptionId "e791a474-ee54-46a2-bb06-5e058302d234" -ApplicationResourceGroupName "ContosoResourceGroup" -ApplicationName "MyAIApplication"

Name              : subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="44146-114">이 명령은 주어진 로그 분석 작업 영역에서 주어진 애플리케이션의 application-insights 데이터 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="44146-114">This command creates an application-insights data source of a given application in a given log analytics workspace.</span></span> <span data-ttu-id="44146-115">이렇게 하면 주어진 애플리케이션에서 로그 분석 작업 영역으로 로그를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44146-115">This enables the collection of logs from given application to the log analytics workspace.</span></span>

### <span data-ttu-id="44146-116">예제 2: 작업 영역 개체를 만들고 애플리케이션 리소스 ID로 application-insights 데이터 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="44146-116">Example 2: Get workspace object and create application-insights data source by the application resource id</span></span>
```
PS C:\> Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup" | New-AzOperationalInsightsApplicationInsightsDataSource -ApplicationResourceId "/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication"

Name              : subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="44146-117">이 명령은 로그 분석 작업 영역 개체를 확보한 다음, 출력을 전달하여 애플리케이션 리소스 ID에 의해 연결된 application-insights 데이터 원본을 만드는 것을 보여 합니다.</span><span class="sxs-lookup"><span data-stu-id="44146-117">This command demonstrates getting a log analytics workspace object and then passing the output to create an associated application-insights data source by the application resource id.</span></span> 

## <span data-ttu-id="44146-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44146-118">PARAMETERS</span></span>

### <span data-ttu-id="44146-119">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="44146-119">-ApplicationName</span></span>
<span data-ttu-id="44146-120">연결된 애플리케이션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44146-120">The name of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44146-121">-ApplicationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44146-121">-ApplicationResourceGroupName</span></span>
<span data-ttu-id="44146-122">연결된 애플리케이션의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44146-122">The resource group name of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44146-123">-ApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="44146-123">-ApplicationResourceId</span></span>
<span data-ttu-id="44146-124">연결된 애플리케이션 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="44146-124">The linked application resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationResourceId, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44146-125">-ApplicationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44146-125">-ApplicationSubscriptionId</span></span>
<span data-ttu-id="44146-126">연결된 애플리케이션의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="44146-126">The subscription id of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44146-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44146-127">-DefaultProfile</span></span>
<span data-ttu-id="44146-128">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44146-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44146-129">-Force</span><span class="sxs-lookup"><span data-stu-id="44146-129">-Force</span></span>
<span data-ttu-id="44146-130">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44146-130">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="44146-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44146-131">-ResourceGroupName</span></span>
<span data-ttu-id="44146-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44146-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByApplicationParameters, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44146-133">-Workspace</span><span class="sxs-lookup"><span data-stu-id="44146-133">-Workspace</span></span>
<span data-ttu-id="44146-134">데이터 원본을 포함할 작업 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="44146-134">The workspace that will contain the data source.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceObjectByApplicationResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44146-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="44146-135">-WorkspaceName</span></span>
<span data-ttu-id="44146-136">데이터 원본을 포함할 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44146-136">The name of the workspace that will contain the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByApplicationParameters, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44146-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44146-137">-Confirm</span></span>
<span data-ttu-id="44146-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="44146-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44146-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44146-139">-WhatIf</span></span>
<span data-ttu-id="44146-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="44146-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44146-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44146-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44146-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44146-142">CommonParameters</span></span>
<span data-ttu-id="44146-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="44146-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44146-144">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="44146-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44146-145">입력</span><span class="sxs-lookup"><span data-stu-id="44146-145">INPUTS</span></span>

### <span data-ttu-id="44146-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="44146-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="44146-147">System.String</span><span class="sxs-lookup"><span data-stu-id="44146-147">System.String</span></span>

## <span data-ttu-id="44146-148">출력</span><span class="sxs-lookup"><span data-stu-id="44146-148">OUTPUTS</span></span>

### <span data-ttu-id="44146-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="44146-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="44146-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="44146-150">NOTES</span></span>

## <span data-ttu-id="44146-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44146-151">RELATED LINKS</span></span>

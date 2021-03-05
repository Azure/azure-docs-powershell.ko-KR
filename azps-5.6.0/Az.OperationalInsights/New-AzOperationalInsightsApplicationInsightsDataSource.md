---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E3D7A3FE-40D4-4495-BA39-493F85F304AD
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightsapplicationinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
ms.openlocfilehash: 21de9e423134c78302adf5c172dee0869b9501bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011803"
---
# <span data-ttu-id="6e70d-101">New-AzOperationalInsightsApplicationInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="6e70d-101">New-AzOperationalInsightsApplicationInsightsDataSource</span></span>

## <span data-ttu-id="6e70d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e70d-102">SYNOPSIS</span></span>
<span data-ttu-id="6e70d-103">주어진 애플리케이션에서 로그를 Application-Insights 수집합니다.</span><span class="sxs-lookup"><span data-stu-id="6e70d-103">Collect logs from given Application-Insights application.</span></span>

## <span data-ttu-id="6e70d-104">구문</span><span class="sxs-lookup"><span data-stu-id="6e70d-104">SYNTAX</span></span>

### <span data-ttu-id="6e70d-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="6e70d-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e70d-106">ByWorkspaceObjectByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="6e70d-106">ByWorkspaceObjectByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e70d-107">ByWorkspaceObjectByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="6e70d-107">ByWorkspaceObjectByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e70d-108">ByWorkspaceNameByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="6e70d-108">ByWorkspaceNameByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e70d-109">ByWorkspaceNameByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="6e70d-109">ByWorkspaceNameByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e70d-110">설명</span><span class="sxs-lookup"><span data-stu-id="6e70d-110">DESCRIPTION</span></span>
<span data-ttu-id="6e70d-111">**New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet을 사용하면 주어진 애플리케이션에서 로그를 Application-Insights 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e70d-111">The **New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet enables the collection of logs from a given Application-Insights application.</span></span>

## <span data-ttu-id="6e70d-112">예제</span><span class="sxs-lookup"><span data-stu-id="6e70d-112">EXAMPLES</span></span>

### <span data-ttu-id="6e70d-113">예제 1: 작업 영역의 application-insights 데이터 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="6e70d-113">Example 1: Create application-insights data source in workspace</span></span>
```
PS C:\> New-AzOperationalInsightsApplicationInsightsDataSource -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -ApplicationSubscriptionId "e791a474-ee54-46a2-bb06-5e058302d234" -ApplicationResourceGroupName "ContosoResourceGroup" -ApplicationName "MyAIApplication"

Name              : subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="6e70d-114">이 명령은 주어진 로그 분석 작업 영역에서 주어진 애플리케이션의 application-insights 데이터 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e70d-114">This command creates an application-insights data source of a given application in a given log analytics workspace.</span></span> <span data-ttu-id="6e70d-115">이렇게 하면 주어진 애플리케이션에서 로그 분석 작업 영역으로 로그를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e70d-115">This enables the collection of logs from given application to the log analytics workspace.</span></span>

### <span data-ttu-id="6e70d-116">예제 2: 작업 영역 개체를 만들고 애플리케이션 리소스 ID로 application-insights 데이터 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="6e70d-116">Example 2: Get workspace object and create application-insights data source by the application resource id</span></span>
```
PS C:\> Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup" | New-AzOperationalInsightsApplicationInsightsDataSource -ApplicationResourceId "/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication"

Name              : subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="6e70d-117">이 명령은 로그 분석 작업 영역 개체를 받고 출력을 전달하여 애플리케이션 리소스 ID로 연결된 애플리케이션-insights 데이터 원본을 만드는 것을 보여 니다.</span><span class="sxs-lookup"><span data-stu-id="6e70d-117">This command demonstrates getting a log analytics workspace object and then passing the output to create an associated application-insights data source by the application resource id.</span></span> 

## <span data-ttu-id="6e70d-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6e70d-118">PARAMETERS</span></span>

### <span data-ttu-id="6e70d-119">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="6e70d-119">-ApplicationName</span></span>
<span data-ttu-id="6e70d-120">연결된 애플리케이션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e70d-120">The name of the linked application.</span></span>

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

### <span data-ttu-id="6e70d-121">-ApplicationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e70d-121">-ApplicationResourceGroupName</span></span>
<span data-ttu-id="6e70d-122">연결된 애플리케이션의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e70d-122">The resource group name of the linked application.</span></span>

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

### <span data-ttu-id="6e70d-123">-ApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="6e70d-123">-ApplicationResourceId</span></span>
<span data-ttu-id="6e70d-124">연결된 애플리케이션 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6e70d-124">The linked application resource id.</span></span>

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

### <span data-ttu-id="6e70d-125">-ApplicationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6e70d-125">-ApplicationSubscriptionId</span></span>
<span data-ttu-id="6e70d-126">연결된 애플리케이션의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6e70d-126">The subscription id of the linked application.</span></span>

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

### <span data-ttu-id="6e70d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e70d-127">-DefaultProfile</span></span>
<span data-ttu-id="6e70d-128">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e70d-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e70d-129">-Force</span><span class="sxs-lookup"><span data-stu-id="6e70d-129">-Force</span></span>
<span data-ttu-id="6e70d-130">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e70d-130">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6e70d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e70d-131">-ResourceGroupName</span></span>
<span data-ttu-id="6e70d-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e70d-132">The resource group name.</span></span>

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

### <span data-ttu-id="6e70d-133">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="6e70d-133">-Workspace</span></span>
<span data-ttu-id="6e70d-134">데이터 원본을 포함하는 작업 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="6e70d-134">The workspace that will contain the data source.</span></span>

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

### <span data-ttu-id="6e70d-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6e70d-135">-WorkspaceName</span></span>
<span data-ttu-id="6e70d-136">데이터 원본을 포함할 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e70d-136">The name of the workspace that will contain the data source.</span></span>

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

### <span data-ttu-id="6e70d-137">-확인</span><span class="sxs-lookup"><span data-stu-id="6e70d-137">-Confirm</span></span>
<span data-ttu-id="6e70d-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e70d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e70d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e70d-139">-WhatIf</span></span>
<span data-ttu-id="6e70d-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6e70d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e70d-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e70d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e70d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e70d-142">CommonParameters</span></span>
<span data-ttu-id="6e70d-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6e70d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e70d-144">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6e70d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e70d-145">입력</span><span class="sxs-lookup"><span data-stu-id="6e70d-145">INPUTS</span></span>

### <span data-ttu-id="6e70d-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="6e70d-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="6e70d-147">System.String</span><span class="sxs-lookup"><span data-stu-id="6e70d-147">System.String</span></span>

## <span data-ttu-id="6e70d-148">출력</span><span class="sxs-lookup"><span data-stu-id="6e70d-148">OUTPUTS</span></span>

### <span data-ttu-id="6e70d-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="6e70d-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="6e70d-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6e70d-150">NOTES</span></span>

## <span data-ttu-id="6e70d-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e70d-151">RELATED LINKS</span></span>

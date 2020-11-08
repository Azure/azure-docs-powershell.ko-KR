---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E3D7A3FE-40D4-4495-BA39-493F85F304AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsapplicationinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
ms.openlocfilehash: 0f238a417ac83cac82305ceb9c9ce20586328976
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218238"
---
# <span data-ttu-id="22ead-101">New-AzOperationalInsightsApplicationInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="22ead-101">New-AzOperationalInsightsApplicationInsightsDataSource</span></span>

## <span data-ttu-id="22ead-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22ead-102">SYNOPSIS</span></span>
<span data-ttu-id="22ead-103">지정 된 Application-Insights 응용 프로그램에서 로그를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="22ead-103">Collect logs from given Application-Insights application.</span></span>

## <span data-ttu-id="22ead-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22ead-104">SYNTAX</span></span>

### <span data-ttu-id="22ead-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="22ead-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22ead-106">ByWorkspaceObjectByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="22ead-106">ByWorkspaceObjectByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22ead-107">ByWorkspaceObjectByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="22ead-107">ByWorkspaceObjectByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22ead-108">ByWorkspaceNameByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="22ead-108">ByWorkspaceNameByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22ead-109">ByWorkspaceNameByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="22ead-109">ByWorkspaceNameByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22ead-110">설명은</span><span class="sxs-lookup"><span data-stu-id="22ead-110">DESCRIPTION</span></span>
<span data-ttu-id="22ead-111">**AzOperationalInsightsApplicationInsightsDataSource** cmdlet을 사용 하면 지정 된 Application-Insights 응용 프로그램에서 로그를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22ead-111">The **New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet enables the collection of logs from a given Application-Insights application.</span></span>

## <span data-ttu-id="22ead-112">예제의</span><span class="sxs-lookup"><span data-stu-id="22ead-112">EXAMPLES</span></span>

### <span data-ttu-id="22ead-113">예제 1: 작업 영역에 application insights 데이터 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="22ead-113">Example 1: Create application-insights data source in workspace</span></span>
```
PS C:\> New-AzOperationalInsightsApplicationInsightsDataSource -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -ApplicationSubscriptionId "e791a474-ee54-46a2-bb06-5e058302d234" -ApplicationResourceGroupName "ContosoResourceGroup" -ApplicationName "MyAIApplication"

Name              : subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="22ead-114">이 명령은 지정 된 로그 분석 작업 영역에서 지정 된 응용 프로그램의 application insights 데이터 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22ead-114">This command creates an application-insights data source of a given application in a given log analytics workspace.</span></span> <span data-ttu-id="22ead-115">이렇게 하면 지정 된 응용 프로그램에서 로그 분석 작업 영역으로 로그를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22ead-115">This enables the collection of logs from given application to the log analytics workspace.</span></span>

### <span data-ttu-id="22ead-116">예제 2: 응용 프로그램 리소스 id를 기준으로 작업 영역 개체 가져오기 및 application insights 데이터 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="22ead-116">Example 2: Get workspace object and create application-insights data source by the application resource id</span></span>
```
PS C:\> Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup" | New-AzOperationalInsightsApplicationInsightsDataSource -ApplicationResourceId "/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication"

Name              : subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="22ead-117">이 명령은 로그 분석 작업 영역 개체를 가져온 다음 출력을 전달 하 여 응용 프로그램 리소스 id를 기준으로 연결 된 application insights 데이터 원본을 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="22ead-117">This command demonstrates getting a log analytics workspace object and then passing the output to create an associated application-insights data source by the application resource id.</span></span> 

## <span data-ttu-id="22ead-118">변수</span><span class="sxs-lookup"><span data-stu-id="22ead-118">PARAMETERS</span></span>

### <span data-ttu-id="22ead-119">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="22ead-119">-ApplicationName</span></span>
<span data-ttu-id="22ead-120">연결 된 응용 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22ead-120">The name of the linked application.</span></span>

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

### <span data-ttu-id="22ead-121">-ApplicationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22ead-121">-ApplicationResourceGroupName</span></span>
<span data-ttu-id="22ead-122">연결 된 응용 프로그램의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22ead-122">The resource group name of the linked application.</span></span>

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

### <span data-ttu-id="22ead-123">-ApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="22ead-123">-ApplicationResourceId</span></span>
<span data-ttu-id="22ead-124">연결 된 응용 프로그램 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="22ead-124">The linked application resource id.</span></span>

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

### <span data-ttu-id="22ead-125">-ApplicationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="22ead-125">-ApplicationSubscriptionId</span></span>
<span data-ttu-id="22ead-126">연결 된 응용 프로그램의 구독 id입니다.</span><span class="sxs-lookup"><span data-stu-id="22ead-126">The subscription id of the linked application.</span></span>

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

### <span data-ttu-id="22ead-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ead-127">-DefaultProfile</span></span>
<span data-ttu-id="22ead-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="22ead-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22ead-129">-Force</span><span class="sxs-lookup"><span data-stu-id="22ead-129">-Force</span></span>
<span data-ttu-id="22ead-130">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22ead-130">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="22ead-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22ead-131">-ResourceGroupName</span></span>
<span data-ttu-id="22ead-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22ead-132">The resource group name.</span></span>

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

### <span data-ttu-id="22ead-133">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="22ead-133">-Workspace</span></span>
<span data-ttu-id="22ead-134">데이터 원본을 포함 하는 작업 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="22ead-134">The workspace that will contain the data source.</span></span>

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

### <span data-ttu-id="22ead-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="22ead-135">-WorkspaceName</span></span>
<span data-ttu-id="22ead-136">데이터 원본을 포함 하는 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22ead-136">The name of the workspace that will contain the data source.</span></span>

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

### <span data-ttu-id="22ead-137">-확인</span><span class="sxs-lookup"><span data-stu-id="22ead-137">-Confirm</span></span>
<span data-ttu-id="22ead-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="22ead-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22ead-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22ead-139">-WhatIf</span></span>
<span data-ttu-id="22ead-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="22ead-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22ead-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22ead-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22ead-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ead-142">CommonParameters</span></span>
<span data-ttu-id="22ead-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22ead-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ead-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22ead-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ead-145">입력</span><span class="sxs-lookup"><span data-stu-id="22ead-145">INPUTS</span></span>

### <span data-ttu-id="22ead-146">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="22ead-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="22ead-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="22ead-147">System.String</span></span>

## <span data-ttu-id="22ead-148">출력</span><span class="sxs-lookup"><span data-stu-id="22ead-148">OUTPUTS</span></span>

### <span data-ttu-id="22ead-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="22ead-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="22ead-150">상속자</span><span class="sxs-lookup"><span data-stu-id="22ead-150">NOTES</span></span>

## <span data-ttu-id="22ead-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22ead-151">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: adbe725557ccf1535a83f5f411cfdc44fd69c6a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981691"
---
# <span data-ttu-id="85c0e-101">Get-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="85c0e-101">Get-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="85c0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="85c0e-103">Storage Insight에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="85c0e-103">Gets information about a Storage Insight.</span></span>

## <span data-ttu-id="85c0e-104">구문</span><span class="sxs-lookup"><span data-stu-id="85c0e-104">SYNTAX</span></span>

### <span data-ttu-id="85c0e-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="85c0e-105">ByWorkspaceName (Default)</span></span>
```
Get-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85c0e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="85c0e-106">ByWorkspaceObject</span></span>
```
Get-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85c0e-107">설명</span><span class="sxs-lookup"><span data-stu-id="85c0e-107">DESCRIPTION</span></span>
<span data-ttu-id="85c0e-108">**Get-AzOperationalInsightsStorageInsight** cmdlet은 기존 Storage Insight에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="85c0e-108">The **Get-AzOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="85c0e-109">Storage Insight 이름이 지정되어 있는 경우 이 cmdlet은 해당 Storage Insight에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="85c0e-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="85c0e-110">이름을 지정하지 않으면 이 cmdlet은 작업 영역의 모든 저장소 인사이트에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="85c0e-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="85c0e-111">예제</span><span class="sxs-lookup"><span data-stu-id="85c0e-111">EXAMPLES</span></span>

### <span data-ttu-id="85c0e-112">예제 1: 이름으로 Storage Insight를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85c0e-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="85c0e-113">이 명령은 ContosoWorkspace라는 작업 영역에서 MyStorageInsight라는 저장소 인사이트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="85c0e-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="85c0e-114">예제 2: 작업 영역 개체를 사용하여 Storage Insight를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85c0e-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="85c0e-115">첫 번째 명령은 **Get-AzOperationalInsightsWorkspace** cmdlet을 사용하여 Operational Insights 작업 $Workspace 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="85c0e-115">The first command uses the **Get-AzOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="85c0e-116">두 번째 명령은 작업 영역의 MyStorageInsight라는 저장소 정보를 $Workspace.</span><span class="sxs-lookup"><span data-stu-id="85c0e-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="85c0e-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="85c0e-117">PARAMETERS</span></span>

### <span data-ttu-id="85c0e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c0e-118">-DefaultProfile</span></span>
<span data-ttu-id="85c0e-119">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="85c0e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85c0e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="85c0e-120">-Name</span></span>
<span data-ttu-id="85c0e-121">Storage Insight 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="85c0e-121">Specifies the Storage Insight name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85c0e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85c0e-122">-ResourceGroupName</span></span>
<span data-ttu-id="85c0e-123">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="85c0e-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85c0e-124">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="85c0e-124">-Workspace</span></span>
<span data-ttu-id="85c0e-125">Storage Insights를 포함하는 작업 공간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="85c0e-125">Specifies the workspace that contains the Storage Insights.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85c0e-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="85c0e-126">-WorkspaceName</span></span>
<span data-ttu-id="85c0e-127">Storage Insights를 포함하는 작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="85c0e-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85c0e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c0e-128">CommonParameters</span></span>
<span data-ttu-id="85c0e-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="85c0e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c0e-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="85c0e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c0e-131">입력</span><span class="sxs-lookup"><span data-stu-id="85c0e-131">INPUTS</span></span>

### <span data-ttu-id="85c0e-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="85c0e-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="85c0e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="85c0e-133">System.String</span></span>

## <span data-ttu-id="85c0e-134">출력</span><span class="sxs-lookup"><span data-stu-id="85c0e-134">OUTPUTS</span></span>

### <span data-ttu-id="85c0e-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="85c0e-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="85c0e-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="85c0e-136">NOTES</span></span>

## <span data-ttu-id="85c0e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85c0e-137">RELATED LINKS</span></span>

[<span data-ttu-id="85c0e-138">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="85c0e-138">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)



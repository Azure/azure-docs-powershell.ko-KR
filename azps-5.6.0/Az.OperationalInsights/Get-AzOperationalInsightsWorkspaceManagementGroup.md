---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: 505156f1c6303b8a3fa699b5528ed3ca2ff690de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990887"
---
# <span data-ttu-id="576ea-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span><span class="sxs-lookup"><span data-stu-id="576ea-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span></span>

## <span data-ttu-id="576ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="576ea-102">SYNOPSIS</span></span>
<span data-ttu-id="576ea-103">작업 영역과 연결된 관리 그룹의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="576ea-103">Gets details of management groups connected to a workspace.</span></span>

## <span data-ttu-id="576ea-104">구문</span><span class="sxs-lookup"><span data-stu-id="576ea-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="576ea-105">설명</span><span class="sxs-lookup"><span data-stu-id="576ea-105">DESCRIPTION</span></span>
<span data-ttu-id="576ea-106">**Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet에는 작업 영역과 연결된 관리 그룹이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="576ea-106">The **Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="576ea-107">예제</span><span class="sxs-lookup"><span data-stu-id="576ea-107">EXAMPLES</span></span>

### <span data-ttu-id="576ea-108">예제 1: 작업 영역 이름으로 관리 그룹 사용</span><span class="sxs-lookup"><span data-stu-id="576ea-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="576ea-109">이 명령은 ContosoResourceGroup이라는 리소스 그룹에서 MyWorkspace라는 작업 영역의 관리 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="576ea-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="576ea-110">예제 2: 파이프라인을 사용하여 관리 그룹 보기</span><span class="sxs-lookup"><span data-stu-id="576ea-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

<span data-ttu-id="576ea-111">이 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용하여 MyWorkspace라는 작업 영역이 있는 다음 작업 영역이 현재 cmdlet으로 전달되어 해당 작업 영역의 관리 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="576ea-111">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="576ea-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="576ea-112">PARAMETERS</span></span>

### <span data-ttu-id="576ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="576ea-113">-DefaultProfile</span></span>
<span data-ttu-id="576ea-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="576ea-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="576ea-115">-Name</span><span class="sxs-lookup"><span data-stu-id="576ea-115">-Name</span></span>
<span data-ttu-id="576ea-116">작업 영역 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="576ea-116">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="576ea-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="576ea-117">-ResourceGroupName</span></span>
<span data-ttu-id="576ea-118">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="576ea-118">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="576ea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="576ea-119">CommonParameters</span></span>
<span data-ttu-id="576ea-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="576ea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="576ea-121">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="576ea-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="576ea-122">입력</span><span class="sxs-lookup"><span data-stu-id="576ea-122">INPUTS</span></span>

### <span data-ttu-id="576ea-123">System.String</span><span class="sxs-lookup"><span data-stu-id="576ea-123">System.String</span></span>

## <span data-ttu-id="576ea-124">출력</span><span class="sxs-lookup"><span data-stu-id="576ea-124">OUTPUTS</span></span>

### <span data-ttu-id="576ea-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="576ea-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="576ea-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="576ea-126">NOTES</span></span>

## <span data-ttu-id="576ea-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="576ea-127">RELATED LINKS</span></span>

[<span data-ttu-id="576ea-128">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="576ea-128">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="576ea-129">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="576ea-129">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)



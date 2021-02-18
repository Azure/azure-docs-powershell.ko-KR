---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: 1579308aed29a4d42cddfeec6f01c71c72c06c6f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206365"
---
# <span data-ttu-id="0daa7-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0daa7-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span></span>

## <span data-ttu-id="0daa7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0daa7-102">SYNOPSIS</span></span>
<span data-ttu-id="0daa7-103">작업 영역과 연결된 관리 그룹의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0daa7-103">Gets details of management groups connected to a workspace.</span></span>

## <span data-ttu-id="0daa7-104">구문</span><span class="sxs-lookup"><span data-stu-id="0daa7-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0daa7-105">설명</span><span class="sxs-lookup"><span data-stu-id="0daa7-105">DESCRIPTION</span></span>
<span data-ttu-id="0daa7-106">**Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet에는 작업 영역과 연결된 관리 그룹이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="0daa7-106">The **Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="0daa7-107">예제</span><span class="sxs-lookup"><span data-stu-id="0daa7-107">EXAMPLES</span></span>

### <span data-ttu-id="0daa7-108">예제 1: 작업 영역 이름으로 관리 그룹 얻기</span><span class="sxs-lookup"><span data-stu-id="0daa7-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="0daa7-109">이 명령은 ContosoResourceGroup이라는 리소스 그룹의 MyWorkspace라는 작업 영역의 관리 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0daa7-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="0daa7-110">예제 2: 파이프라인을 사용하여 관리 그룹 얻기</span><span class="sxs-lookup"><span data-stu-id="0daa7-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

<span data-ttu-id="0daa7-111">이 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용하여 MyWorkspace라는 작업 영역이 있는 다음 작업 영역이 현재 cmdlet에 전달되어 해당 작업 영역의 관리 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0daa7-111">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="0daa7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0daa7-112">PARAMETERS</span></span>

### <span data-ttu-id="0daa7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0daa7-113">-DefaultProfile</span></span>
<span data-ttu-id="0daa7-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0daa7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0daa7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0daa7-115">-Name</span></span>
<span data-ttu-id="0daa7-116">작업 영역 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0daa7-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="0daa7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0daa7-117">-ResourceGroupName</span></span>
<span data-ttu-id="0daa7-118">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0daa7-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="0daa7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0daa7-119">CommonParameters</span></span>
<span data-ttu-id="0daa7-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0daa7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0daa7-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0daa7-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0daa7-122">입력</span><span class="sxs-lookup"><span data-stu-id="0daa7-122">INPUTS</span></span>

### <span data-ttu-id="0daa7-123">System.String</span><span class="sxs-lookup"><span data-stu-id="0daa7-123">System.String</span></span>

## <span data-ttu-id="0daa7-124">출력</span><span class="sxs-lookup"><span data-stu-id="0daa7-124">OUTPUTS</span></span>

### <span data-ttu-id="0daa7-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0daa7-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="0daa7-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0daa7-126">NOTES</span></span>

## <span data-ttu-id="0daa7-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0daa7-127">RELATED LINKS</span></span>

[<span data-ttu-id="0daa7-128">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0daa7-128">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="0daa7-129">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0daa7-129">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)



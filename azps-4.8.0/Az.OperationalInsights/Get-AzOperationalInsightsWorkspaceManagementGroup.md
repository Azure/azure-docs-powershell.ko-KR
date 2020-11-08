---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: 1579308aed29a4d42cddfeec6f01c71c72c06c6f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203845"
---
# <span data-ttu-id="12009-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span><span class="sxs-lookup"><span data-stu-id="12009-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span></span>

## <span data-ttu-id="12009-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12009-102">SYNOPSIS</span></span>
<span data-ttu-id="12009-103">작업 영역에 연결 된 관리 그룹의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="12009-103">Gets details of management groups connected to a workspace.</span></span>

## <span data-ttu-id="12009-104">구문과</span><span class="sxs-lookup"><span data-stu-id="12009-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12009-105">설명은</span><span class="sxs-lookup"><span data-stu-id="12009-105">DESCRIPTION</span></span>
<span data-ttu-id="12009-106">**AzOperationalInsightsWorkspaceManagementGroup** cmdlet은 작업 영역에 연결 된 관리 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="12009-106">The **Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="12009-107">예제의</span><span class="sxs-lookup"><span data-stu-id="12009-107">EXAMPLES</span></span>

### <span data-ttu-id="12009-108">예제 1: 작업 영역 이름별로 관리 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="12009-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="12009-109">이 명령은 ContosoResourceGroup 이라는 리소스 그룹에서 MyWorkspace 라는 작업 영역의 관리 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="12009-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="12009-110">예제 2: 파이프라인을 사용 하 여 관리 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="12009-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

<span data-ttu-id="12009-111">이 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용 하 여 MyWorkspace 라는 작업 영역을 가져온 다음 해당 작업 영역의 관리 그룹을 가져오는 현재 cmdlet에 작업 영역을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="12009-111">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="12009-112">변수</span><span class="sxs-lookup"><span data-stu-id="12009-112">PARAMETERS</span></span>

### <span data-ttu-id="12009-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12009-113">-DefaultProfile</span></span>
<span data-ttu-id="12009-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="12009-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12009-115">-이름</span><span class="sxs-lookup"><span data-stu-id="12009-115">-Name</span></span>
<span data-ttu-id="12009-116">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12009-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="12009-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12009-117">-ResourceGroupName</span></span>
<span data-ttu-id="12009-118">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12009-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="12009-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12009-119">CommonParameters</span></span>
<span data-ttu-id="12009-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="12009-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12009-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12009-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12009-122">입력</span><span class="sxs-lookup"><span data-stu-id="12009-122">INPUTS</span></span>

### <span data-ttu-id="12009-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="12009-123">System.String</span></span>

## <span data-ttu-id="12009-124">출력</span><span class="sxs-lookup"><span data-stu-id="12009-124">OUTPUTS</span></span>

### <span data-ttu-id="12009-125">OperationalInsights. PSManagementGroup/.</span><span class="sxs-lookup"><span data-stu-id="12009-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="12009-126">상속자</span><span class="sxs-lookup"><span data-stu-id="12009-126">NOTES</span></span>

## <span data-ttu-id="12009-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12009-127">RELATED LINKS</span></span>

[<span data-ttu-id="12009-128">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="12009-128">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="12009-129">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="12009-129">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)



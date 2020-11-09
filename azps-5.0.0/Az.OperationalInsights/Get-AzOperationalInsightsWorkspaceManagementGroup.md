---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: 1579308aed29a4d42cddfeec6f01c71c72c06c6f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308060"
---
# <span data-ttu-id="6bae9-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6bae9-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span></span>

## <span data-ttu-id="6bae9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bae9-102">SYNOPSIS</span></span>
<span data-ttu-id="6bae9-103">작업 영역에 연결 된 관리 그룹의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6bae9-103">Gets details of management groups connected to a workspace.</span></span>

## <span data-ttu-id="6bae9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6bae9-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bae9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6bae9-105">DESCRIPTION</span></span>
<span data-ttu-id="6bae9-106">**AzOperationalInsightsWorkspaceManagementGroup** cmdlet은 작업 영역에 연결 된 관리 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bae9-106">The **Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="6bae9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6bae9-107">EXAMPLES</span></span>

### <span data-ttu-id="6bae9-108">예제 1: 작업 영역 이름별로 관리 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="6bae9-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="6bae9-109">이 명령은 ContosoResourceGroup 이라는 리소스 그룹에서 MyWorkspace 라는 작업 영역의 관리 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6bae9-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="6bae9-110">예제 2: 파이프라인을 사용 하 여 관리 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="6bae9-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

<span data-ttu-id="6bae9-111">이 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용 하 여 MyWorkspace 라는 작업 영역을 가져온 다음 해당 작업 영역의 관리 그룹을 가져오는 현재 cmdlet에 작업 영역을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bae9-111">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="6bae9-112">변수</span><span class="sxs-lookup"><span data-stu-id="6bae9-112">PARAMETERS</span></span>

### <span data-ttu-id="6bae9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bae9-113">-DefaultProfile</span></span>
<span data-ttu-id="6bae9-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6bae9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6bae9-115">-이름</span><span class="sxs-lookup"><span data-stu-id="6bae9-115">-Name</span></span>
<span data-ttu-id="6bae9-116">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bae9-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="6bae9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bae9-117">-ResourceGroupName</span></span>
<span data-ttu-id="6bae9-118">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bae9-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="6bae9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bae9-119">CommonParameters</span></span>
<span data-ttu-id="6bae9-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bae9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bae9-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bae9-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bae9-122">입력</span><span class="sxs-lookup"><span data-stu-id="6bae9-122">INPUTS</span></span>

### <span data-ttu-id="6bae9-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6bae9-123">System.String</span></span>

## <span data-ttu-id="6bae9-124">출력</span><span class="sxs-lookup"><span data-stu-id="6bae9-124">OUTPUTS</span></span>

### <span data-ttu-id="6bae9-125">OperationalInsights. PSManagementGroup/.</span><span class="sxs-lookup"><span data-stu-id="6bae9-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="6bae9-126">상속자</span><span class="sxs-lookup"><span data-stu-id="6bae9-126">NOTES</span></span>

## <span data-ttu-id="6bae9-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6bae9-127">RELATED LINKS</span></span>

[<span data-ttu-id="6bae9-128">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6bae9-128">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="6bae9-129">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="6bae9-129">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)



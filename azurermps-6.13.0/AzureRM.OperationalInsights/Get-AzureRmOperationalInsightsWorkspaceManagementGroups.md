---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspacemanagementgroups
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
ms.openlocfilehash: 215e3007de3b3760d974512cdffdd669f32447ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527807"
---
# <span data-ttu-id="e5549-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span><span class="sxs-lookup"><span data-stu-id="e5549-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span></span>

## <span data-ttu-id="e5549-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5549-102">SYNOPSIS</span></span>
<span data-ttu-id="e5549-103">작업 영역에 연결 된 관리 그룹의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e5549-103">Gets details of management groups connected to a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5549-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e5549-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceManagementGroups [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5549-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e5549-105">DESCRIPTION</span></span>
<span data-ttu-id="e5549-106">**AzureRmOperationalInsightsWorkspaceManagementGroups** cmdlet은 작업 영역에 연결 된 관리 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5549-106">The **Get-AzureRmOperationalInsightsWorkspaceManagementGroups** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="e5549-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e5549-107">EXAMPLES</span></span>

### <span data-ttu-id="e5549-108">예제 1: 작업 영역 이름별로 관리 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="e5549-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceManagementGroups -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="e5549-109">이 명령은 ContosoResourceGroup 이라는 리소스 그룹에서 MyWorkspace 라는 작업 영역의 관리 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e5549-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="e5549-110">예제 2: 파이프라인을 사용 하 여 관리 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="e5549-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceManagementGroups
```

<span data-ttu-id="e5549-111">이 명령은 Get-AzureRmOperationalInsightsWorkspace cmdlet을 사용 하 여 MyWorkspace 라는 작업 영역을 가져온 다음 해당 작업 영역의 관리 그룹을 가져오는 현재 cmdlet에 작업 영역을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5549-111">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="e5549-112">변수</span><span class="sxs-lookup"><span data-stu-id="e5549-112">PARAMETERS</span></span>

### <span data-ttu-id="e5549-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5549-113">-DefaultProfile</span></span>
<span data-ttu-id="e5549-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e5549-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5549-115">-이름</span><span class="sxs-lookup"><span data-stu-id="e5549-115">-Name</span></span>
<span data-ttu-id="e5549-116">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5549-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="e5549-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5549-117">-ResourceGroupName</span></span>
<span data-ttu-id="e5549-118">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5549-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="e5549-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5549-119">CommonParameters</span></span>
<span data-ttu-id="e5549-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5549-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5549-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5549-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5549-122">입력</span><span class="sxs-lookup"><span data-stu-id="e5549-122">INPUTS</span></span>

### <span data-ttu-id="e5549-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e5549-123">System.String</span></span>

## <span data-ttu-id="e5549-124">출력</span><span class="sxs-lookup"><span data-stu-id="e5549-124">OUTPUTS</span></span>

### <span data-ttu-id="e5549-125">OperationalInsights. PSManagementGroup/.</span><span class="sxs-lookup"><span data-stu-id="e5549-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="e5549-126">상속자</span><span class="sxs-lookup"><span data-stu-id="e5549-126">NOTES</span></span>

## <span data-ttu-id="e5549-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5549-127">RELATED LINKS</span></span>

[<span data-ttu-id="e5549-128">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5549-128">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="e5549-129">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="e5549-129">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)



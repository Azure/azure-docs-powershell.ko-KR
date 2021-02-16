---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 1a0d36c2e871bd0495216bce18d84dff60e1044d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179225"
---
# <span data-ttu-id="742b5-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="742b5-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="742b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="742b5-102">SYNOPSIS</span></span>
<span data-ttu-id="742b5-103">작업 영역 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="742b5-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="742b5-104">구문</span><span class="sxs-lookup"><span data-stu-id="742b5-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="742b5-105">설명</span><span class="sxs-lookup"><span data-stu-id="742b5-105">DESCRIPTION</span></span>
<span data-ttu-id="742b5-106">**Get-AzOperationalInsightsWorkspace** cmdlet은 기존 작업 영역의 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="742b5-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="742b5-107">작업 영역 이름을 지정하는 경우 이 cmdlet은 해당 작업 영역 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="742b5-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="742b5-108">이름을 지정하지 않으면 이 cmdlet은 리소스 그룹의 모든 작업 영역 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="742b5-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="742b5-109">이름 및 리소스 그룹을 지정하지 않으면 이 cmdlet은 구독의 모든 작업 영역 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="742b5-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="742b5-110">예제</span><span class="sxs-lookup"><span data-stu-id="742b5-110">EXAMPLES</span></span>

### <span data-ttu-id="742b5-111">예제 1: 이름으로 작업 영역 얻기</span><span class="sxs-lookup"><span data-stu-id="742b5-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="742b5-112">이 명령은 ContosoResourceGroup이라는 리소스 그룹에 MyWorkspace라는 작업 영역이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="742b5-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="742b5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="742b5-113">PARAMETERS</span></span>

### <span data-ttu-id="742b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="742b5-114">-DefaultProfile</span></span>
<span data-ttu-id="742b5-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="742b5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="742b5-116">-Name</span><span class="sxs-lookup"><span data-stu-id="742b5-116">-Name</span></span>
<span data-ttu-id="742b5-117">작업 영역 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="742b5-117">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="742b5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="742b5-118">-ResourceGroupName</span></span>
<span data-ttu-id="742b5-119">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="742b5-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="742b5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="742b5-120">CommonParameters</span></span>
<span data-ttu-id="742b5-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="742b5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="742b5-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="742b5-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="742b5-123">입력</span><span class="sxs-lookup"><span data-stu-id="742b5-123">INPUTS</span></span>

### <span data-ttu-id="742b5-124">System.String</span><span class="sxs-lookup"><span data-stu-id="742b5-124">System.String</span></span>

## <span data-ttu-id="742b5-125">출력</span><span class="sxs-lookup"><span data-stu-id="742b5-125">OUTPUTS</span></span>

### <span data-ttu-id="742b5-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="742b5-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="742b5-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="742b5-127">NOTES</span></span>

## <span data-ttu-id="742b5-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="742b5-128">RELATED LINKS</span></span>

[<span data-ttu-id="742b5-129">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="742b5-129">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)



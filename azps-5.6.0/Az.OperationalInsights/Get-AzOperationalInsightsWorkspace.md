---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 4082e7fc36228953ea33f8f3252bab642ca50e2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001008"
---
# <span data-ttu-id="c1456-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="c1456-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="c1456-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1456-102">SYNOPSIS</span></span>
<span data-ttu-id="c1456-103">작업 영역에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c1456-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="c1456-104">구문</span><span class="sxs-lookup"><span data-stu-id="c1456-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1456-105">설명</span><span class="sxs-lookup"><span data-stu-id="c1456-105">DESCRIPTION</span></span>
<span data-ttu-id="c1456-106">**Get-AzOperationalInsightsWorkspace** cmdlet은 기존 작업 영역 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c1456-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="c1456-107">작업 영역 이름을 지정하는 경우 이 cmdlet은 해당 작업 영역에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c1456-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="c1456-108">이름을 지정하지 않으면 이 cmdlet은 리소스 그룹의 모든 작업 영역 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c1456-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="c1456-109">이름 및 리소스 그룹을 지정하지 않으면 이 cmdlet은 구독의 모든 작업 영역에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c1456-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="c1456-110">예제</span><span class="sxs-lookup"><span data-stu-id="c1456-110">EXAMPLES</span></span>

### <span data-ttu-id="c1456-111">예제 1: 이름에 따라 작업 영역 얻기</span><span class="sxs-lookup"><span data-stu-id="c1456-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="c1456-112">이 명령은 ContosoResourceGroup이라는 리소스 그룹에 MyWorkspace라는 작업 영역이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1456-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="c1456-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c1456-113">PARAMETERS</span></span>

### <span data-ttu-id="c1456-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1456-114">-DefaultProfile</span></span>
<span data-ttu-id="c1456-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c1456-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1456-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c1456-116">-Name</span></span>
<span data-ttu-id="c1456-117">작업 영역 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1456-117">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="c1456-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1456-118">-ResourceGroupName</span></span>
<span data-ttu-id="c1456-119">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1456-119">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="c1456-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1456-120">CommonParameters</span></span>
<span data-ttu-id="c1456-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c1456-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1456-122">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c1456-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1456-123">입력</span><span class="sxs-lookup"><span data-stu-id="c1456-123">INPUTS</span></span>

### <span data-ttu-id="c1456-124">System.String</span><span class="sxs-lookup"><span data-stu-id="c1456-124">System.String</span></span>

## <span data-ttu-id="c1456-125">출력</span><span class="sxs-lookup"><span data-stu-id="c1456-125">OUTPUTS</span></span>

### <span data-ttu-id="c1456-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c1456-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="c1456-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c1456-127">NOTES</span></span>

## <span data-ttu-id="c1456-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1456-128">RELATED LINKS</span></span>

[<span data-ttu-id="c1456-129">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1456-129">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)



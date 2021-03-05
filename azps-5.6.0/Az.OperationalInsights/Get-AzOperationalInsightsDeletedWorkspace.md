---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: a4ac55c3c00ba35fa53f6e9a338712d02e507ce1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976512"
---
# <span data-ttu-id="ecde3-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="ecde3-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="ecde3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecde3-102">SYNOPSIS</span></span>
<span data-ttu-id="ecde3-103">삭제된 작업 영역 목록을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ecde3-103">List deleted workspaces.</span></span>

## <span data-ttu-id="ecde3-104">구문</span><span class="sxs-lookup"><span data-stu-id="ecde3-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecde3-105">설명</span><span class="sxs-lookup"><span data-stu-id="ecde3-105">DESCRIPTION</span></span>
<span data-ttu-id="ecde3-106">삭제된 작업 영역 목록을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ecde3-106">List deleted workspaces.</span></span>

## <span data-ttu-id="ecde3-107">예제</span><span class="sxs-lookup"><span data-stu-id="ecde3-107">EXAMPLES</span></span>

### <span data-ttu-id="ecde3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ecde3-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="ecde3-109">삭제된 작업 영역 목록을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ecde3-109">List deleted workspaces.</span></span>

## <span data-ttu-id="ecde3-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ecde3-110">PARAMETERS</span></span>

### <span data-ttu-id="ecde3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecde3-111">-DefaultProfile</span></span>
<span data-ttu-id="ecde3-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ecde3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecde3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecde3-113">-ResourceGroupName</span></span>
<span data-ttu-id="ecde3-114">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ecde3-114">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecde3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecde3-115">CommonParameters</span></span>
<span data-ttu-id="ecde3-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ecde3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecde3-117">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecde3-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecde3-118">입력</span><span class="sxs-lookup"><span data-stu-id="ecde3-118">INPUTS</span></span>

### <span data-ttu-id="ecde3-119">System.String</span><span class="sxs-lookup"><span data-stu-id="ecde3-119">System.String</span></span>

## <span data-ttu-id="ecde3-120">출력</span><span class="sxs-lookup"><span data-stu-id="ecde3-120">OUTPUTS</span></span>

### <span data-ttu-id="ecde3-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ecde3-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="ecde3-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ecde3-122">NOTES</span></span>

## <span data-ttu-id="ecde3-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecde3-123">RELATED LINKS</span></span>

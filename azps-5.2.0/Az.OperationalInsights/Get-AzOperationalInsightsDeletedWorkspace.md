---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338594"
---
# <span data-ttu-id="aab40-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="aab40-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="aab40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aab40-102">SYNOPSIS</span></span>
<span data-ttu-id="aab40-103">삭제된 작업 영역 나열</span><span class="sxs-lookup"><span data-stu-id="aab40-103">List deleted workspaces.</span></span>

## <span data-ttu-id="aab40-104">구문</span><span class="sxs-lookup"><span data-stu-id="aab40-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aab40-105">설명</span><span class="sxs-lookup"><span data-stu-id="aab40-105">DESCRIPTION</span></span>
<span data-ttu-id="aab40-106">삭제된 작업 영역 나열</span><span class="sxs-lookup"><span data-stu-id="aab40-106">List deleted workspaces.</span></span>

## <span data-ttu-id="aab40-107">예제</span><span class="sxs-lookup"><span data-stu-id="aab40-107">EXAMPLES</span></span>

### <span data-ttu-id="aab40-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="aab40-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="aab40-109">삭제된 작업 영역 나열</span><span class="sxs-lookup"><span data-stu-id="aab40-109">List deleted workspaces.</span></span>

## <span data-ttu-id="aab40-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aab40-110">PARAMETERS</span></span>

### <span data-ttu-id="aab40-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab40-111">-DefaultProfile</span></span>
<span data-ttu-id="aab40-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aab40-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aab40-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aab40-113">-ResourceGroupName</span></span>
<span data-ttu-id="aab40-114">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aab40-114">The resource group name.</span></span>

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

### <span data-ttu-id="aab40-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab40-115">CommonParameters</span></span>
<span data-ttu-id="aab40-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aab40-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aab40-117">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aab40-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab40-118">입력</span><span class="sxs-lookup"><span data-stu-id="aab40-118">INPUTS</span></span>

### <span data-ttu-id="aab40-119">System.String</span><span class="sxs-lookup"><span data-stu-id="aab40-119">System.String</span></span>

## <span data-ttu-id="aab40-120">출력</span><span class="sxs-lookup"><span data-stu-id="aab40-120">OUTPUTS</span></span>

### <span data-ttu-id="aab40-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="aab40-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="aab40-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aab40-122">NOTES</span></span>

## <span data-ttu-id="aab40-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aab40-123">RELATED LINKS</span></span>

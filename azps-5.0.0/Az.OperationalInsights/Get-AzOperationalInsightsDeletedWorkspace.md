---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218500"
---
# <span data-ttu-id="d5780-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="d5780-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="d5780-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5780-102">SYNOPSIS</span></span>
<span data-ttu-id="d5780-103">삭제 된 작업 영역을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5780-103">List deleted workspaces.</span></span>

## <span data-ttu-id="d5780-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5780-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5780-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d5780-105">DESCRIPTION</span></span>
<span data-ttu-id="d5780-106">삭제 된 작업 영역을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5780-106">List deleted workspaces.</span></span>

## <span data-ttu-id="d5780-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d5780-107">EXAMPLES</span></span>

### <span data-ttu-id="d5780-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d5780-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="d5780-109">삭제 된 작업 영역을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5780-109">List deleted workspaces.</span></span>

## <span data-ttu-id="d5780-110">변수</span><span class="sxs-lookup"><span data-stu-id="d5780-110">PARAMETERS</span></span>

### <span data-ttu-id="d5780-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5780-111">-DefaultProfile</span></span>
<span data-ttu-id="d5780-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5780-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5780-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5780-113">-ResourceGroupName</span></span>
<span data-ttu-id="d5780-114">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5780-114">The resource group name.</span></span>

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

### <span data-ttu-id="d5780-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5780-115">CommonParameters</span></span>
<span data-ttu-id="d5780-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5780-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5780-117">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d5780-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5780-118">입력</span><span class="sxs-lookup"><span data-stu-id="d5780-118">INPUTS</span></span>

### <span data-ttu-id="d5780-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d5780-119">System.String</span></span>

## <span data-ttu-id="d5780-120">출력</span><span class="sxs-lookup"><span data-stu-id="d5780-120">OUTPUTS</span></span>

### <span data-ttu-id="d5780-121">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="d5780-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="d5780-122">상속자</span><span class="sxs-lookup"><span data-stu-id="d5780-122">NOTES</span></span>

## <span data-ttu-id="d5780-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5780-123">RELATED LINKS</span></span>

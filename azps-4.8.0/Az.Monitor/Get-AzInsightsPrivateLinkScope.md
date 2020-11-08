---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: d5986694ad0064265bbd4bad6e1efc378683ce97
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214439"
---
# <span data-ttu-id="c0718-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="c0718-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="c0718-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0718-102">SYNOPSIS</span></span>
<span data-ttu-id="c0718-103">개인 링크 범위 가져오기</span><span class="sxs-lookup"><span data-stu-id="c0718-103">Get private link scope</span></span>

## <span data-ttu-id="c0718-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c0718-104">SYNTAX</span></span>

### <span data-ttu-id="c0718-105">ByResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c0718-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0718-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0718-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0718-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0718-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0718-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c0718-108">DESCRIPTION</span></span>
<span data-ttu-id="c0718-109">개인 링크 범위 나열 또는 가져오기</span><span class="sxs-lookup"><span data-stu-id="c0718-109">List or get private link scope</span></span> 

## <span data-ttu-id="c0718-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c0718-110">EXAMPLES</span></span>

### <span data-ttu-id="c0718-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c0718-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="c0718-112">리소스 그룹 "rg_name" 아래에 개인 링크 범위 나열</span><span class="sxs-lookup"><span data-stu-id="c0718-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="c0718-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="c0718-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="c0718-114">"Rg_name" 리소스 그룹의 이름이 "scope_name" 인 개인 링크 범위 가져오기</span><span class="sxs-lookup"><span data-stu-id="c0718-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="c0718-115">변수</span><span class="sxs-lookup"><span data-stu-id="c0718-115">PARAMETERS</span></span>

### <span data-ttu-id="c0718-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0718-116">-DefaultProfile</span></span>
<span data-ttu-id="c0718-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0718-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0718-118">-이름</span><span class="sxs-lookup"><span data-stu-id="c0718-118">-Name</span></span>
<span data-ttu-id="c0718-119">개인 링크 범위 이름</span><span class="sxs-lookup"><span data-stu-id="c0718-119">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0718-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0718-120">-ResourceGroupName</span></span>
<span data-ttu-id="c0718-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c0718-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0718-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0718-122">-ResourceId</span></span>
<span data-ttu-id="c0718-123">리소스 Id</span><span class="sxs-lookup"><span data-stu-id="c0718-123">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0718-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0718-124">CommonParameters</span></span>
<span data-ttu-id="c0718-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0718-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0718-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c0718-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0718-127">입력</span><span class="sxs-lookup"><span data-stu-id="c0718-127">INPUTS</span></span>

### <span data-ttu-id="c0718-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c0718-128">System.String</span></span>

## <span data-ttu-id="c0718-129">출력</span><span class="sxs-lookup"><span data-stu-id="c0718-129">OUTPUTS</span></span>

### <span data-ttu-id="c0718-130">PSMonitorPrivateLinkScope를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0718-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="c0718-131">상속자</span><span class="sxs-lookup"><span data-stu-id="c0718-131">NOTES</span></span>

## <span data-ttu-id="c0718-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0718-132">RELATED LINKS</span></span>

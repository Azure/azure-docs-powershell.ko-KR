---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 198d52678bceccfd1045522881dc3a62fdebf752
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180129"
---
# <span data-ttu-id="5944b-101">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="5944b-101">New-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="5944b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5944b-102">SYNOPSIS</span></span>
<span data-ttu-id="5944b-103">개인 링크 범위 만들기</span><span class="sxs-lookup"><span data-stu-id="5944b-103">create private link scope</span></span>

## <span data-ttu-id="5944b-104">구문</span><span class="sxs-lookup"><span data-stu-id="5944b-104">SYNTAX</span></span>

```
New-AzInsightsPrivateLinkScope -Location <String> -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5944b-105">설명</span><span class="sxs-lookup"><span data-stu-id="5944b-105">DESCRIPTION</span></span>
<span data-ttu-id="5944b-106">개인 링크 범위 만들기</span><span class="sxs-lookup"><span data-stu-id="5944b-106">create private link scope</span></span>

## <span data-ttu-id="5944b-107">예제</span><span class="sxs-lookup"><span data-stu-id="5944b-107">EXAMPLES</span></span>

### <span data-ttu-id="5944b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5944b-108">Example 1</span></span>
```powershell
New-AzInsightsPrivateLinkScope -Location "eastus" -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="5944b-109">"eastus" 위치의 리소스 그룹 "scope_name"에서 "rg_name"라는 이름의 개인 링크 범위를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5944b-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span></span>

## <span data-ttu-id="5944b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5944b-110">PARAMETERS</span></span>

### <span data-ttu-id="5944b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5944b-111">-DefaultProfile</span></span>
<span data-ttu-id="5944b-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5944b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5944b-113">-Location</span><span class="sxs-lookup"><span data-stu-id="5944b-113">-Location</span></span>
<span data-ttu-id="5944b-114">위치</span><span class="sxs-lookup"><span data-stu-id="5944b-114">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5944b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5944b-115">-Name</span></span>
<span data-ttu-id="5944b-116">개인 링크 범위 이름</span><span class="sxs-lookup"><span data-stu-id="5944b-116">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5944b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5944b-117">-ResourceGroupName</span></span>
<span data-ttu-id="5944b-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="5944b-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5944b-119">-Tags</span><span class="sxs-lookup"><span data-stu-id="5944b-119">-Tags</span></span>
<span data-ttu-id="5944b-120">태그</span><span class="sxs-lookup"><span data-stu-id="5944b-120">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5944b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5944b-121">-Confirm</span></span>
<span data-ttu-id="5944b-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5944b-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5944b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5944b-123">-WhatIf</span></span>
<span data-ttu-id="5944b-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5944b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5944b-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5944b-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5944b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5944b-126">CommonParameters</span></span>
<span data-ttu-id="5944b-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5944b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5944b-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5944b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5944b-129">입력</span><span class="sxs-lookup"><span data-stu-id="5944b-129">INPUTS</span></span>

### <span data-ttu-id="5944b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5944b-130">System.String</span></span>

## <span data-ttu-id="5944b-131">출력</span><span class="sxs-lookup"><span data-stu-id="5944b-131">OUTPUTS</span></span>

### <span data-ttu-id="5944b-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="5944b-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="5944b-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5944b-133">NOTES</span></span>

## <span data-ttu-id="5944b-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5944b-134">RELATED LINKS</span></span>

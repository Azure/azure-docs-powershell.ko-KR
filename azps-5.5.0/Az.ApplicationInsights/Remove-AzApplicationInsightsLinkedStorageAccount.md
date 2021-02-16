---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 6bb6a422af88c0d7cd911e575e9d49bcdafcd3d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195273"
---
# <span data-ttu-id="68b08-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="68b08-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="68b08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68b08-102">SYNOPSIS</span></span>
<span data-ttu-id="68b08-103">Application Insights 연결된 저장소 계정 삭제</span><span class="sxs-lookup"><span data-stu-id="68b08-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="68b08-104">구문</span><span class="sxs-lookup"><span data-stu-id="68b08-104">SYNTAX</span></span>

### <span data-ttu-id="68b08-105">ByResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="68b08-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68b08-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68b08-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68b08-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68b08-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68b08-108">설명</span><span class="sxs-lookup"><span data-stu-id="68b08-108">DESCRIPTION</span></span>
<span data-ttu-id="68b08-109">Application Insights 연결된 저장소 계정 삭제</span><span class="sxs-lookup"><span data-stu-id="68b08-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="68b08-110">예제</span><span class="sxs-lookup"><span data-stu-id="68b08-110">EXAMPLES</span></span>

### <span data-ttu-id="68b08-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="68b08-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="68b08-112">Application Insights 구성 요소 "componentName"에 연결된 저장소 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="68b08-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="68b08-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68b08-113">PARAMETERS</span></span>

### <span data-ttu-id="68b08-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="68b08-114">-ComponentName</span></span>
<span data-ttu-id="68b08-115">구성 요소 이름</span><span class="sxs-lookup"><span data-stu-id="68b08-115">Component Name</span></span>

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

### <span data-ttu-id="68b08-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68b08-116">-DefaultProfile</span></span>
<span data-ttu-id="68b08-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68b08-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68b08-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68b08-118">-InputObject</span></span>
<span data-ttu-id="68b08-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="68b08-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68b08-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68b08-120">-ResourceGroupName</span></span>
<span data-ttu-id="68b08-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="68b08-121">Resource Group Name</span></span>

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

### <span data-ttu-id="68b08-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68b08-122">-ResourceId</span></span>
<span data-ttu-id="68b08-123">구성 요소 ResourceId</span><span class="sxs-lookup"><span data-stu-id="68b08-123">Component ResourceId</span></span>

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

### <span data-ttu-id="68b08-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68b08-124">-Confirm</span></span>
<span data-ttu-id="68b08-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="68b08-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68b08-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68b08-126">-WhatIf</span></span>
<span data-ttu-id="68b08-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="68b08-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68b08-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68b08-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68b08-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68b08-129">CommonParameters</span></span>
<span data-ttu-id="68b08-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="68b08-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68b08-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="68b08-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68b08-132">입력</span><span class="sxs-lookup"><span data-stu-id="68b08-132">INPUTS</span></span>

### <span data-ttu-id="68b08-133">System.String</span><span class="sxs-lookup"><span data-stu-id="68b08-133">System.String</span></span>

### <span data-ttu-id="68b08-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="68b08-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="68b08-135">출력</span><span class="sxs-lookup"><span data-stu-id="68b08-135">OUTPUTS</span></span>

### <span data-ttu-id="68b08-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="68b08-136">System.Boolean</span></span>

## <span data-ttu-id="68b08-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="68b08-137">NOTES</span></span>

## <span data-ttu-id="68b08-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68b08-138">RELATED LINKS</span></span>

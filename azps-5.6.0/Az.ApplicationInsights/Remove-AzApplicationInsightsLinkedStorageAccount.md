---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 377a2b967058de9c0cdae1d4c07ceffc73b1bfec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001888"
---
# <span data-ttu-id="5379c-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5379c-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="5379c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5379c-102">SYNOPSIS</span></span>
<span data-ttu-id="5379c-103">애플리케이션 인사이트 연결된 저장소 계정 삭제</span><span class="sxs-lookup"><span data-stu-id="5379c-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="5379c-104">구문</span><span class="sxs-lookup"><span data-stu-id="5379c-104">SYNTAX</span></span>

### <span data-ttu-id="5379c-105">ByResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5379c-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5379c-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5379c-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5379c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5379c-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5379c-108">설명</span><span class="sxs-lookup"><span data-stu-id="5379c-108">DESCRIPTION</span></span>
<span data-ttu-id="5379c-109">애플리케이션 인사이트 연결된 저장소 계정 삭제</span><span class="sxs-lookup"><span data-stu-id="5379c-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="5379c-110">예제</span><span class="sxs-lookup"><span data-stu-id="5379c-110">EXAMPLES</span></span>

### <span data-ttu-id="5379c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5379c-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="5379c-112">애플리케이션 인사이트 구성 요소 "componentName"와 연결된 저장소 계정 삭제</span><span class="sxs-lookup"><span data-stu-id="5379c-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="5379c-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5379c-113">PARAMETERS</span></span>

### <span data-ttu-id="5379c-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="5379c-114">-ComponentName</span></span>
<span data-ttu-id="5379c-115">구성 요소 이름</span><span class="sxs-lookup"><span data-stu-id="5379c-115">Component Name</span></span>

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

### <span data-ttu-id="5379c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5379c-116">-DefaultProfile</span></span>
<span data-ttu-id="5379c-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5379c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5379c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5379c-118">-InputObject</span></span>
<span data-ttu-id="5379c-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="5379c-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="5379c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5379c-120">-ResourceGroupName</span></span>
<span data-ttu-id="5379c-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="5379c-121">Resource Group Name</span></span>

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

### <span data-ttu-id="5379c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5379c-122">-ResourceId</span></span>
<span data-ttu-id="5379c-123">구성 요소 ResourceId</span><span class="sxs-lookup"><span data-stu-id="5379c-123">Component ResourceId</span></span>

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

### <span data-ttu-id="5379c-124">-확인</span><span class="sxs-lookup"><span data-stu-id="5379c-124">-Confirm</span></span>
<span data-ttu-id="5379c-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5379c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5379c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5379c-126">-WhatIf</span></span>
<span data-ttu-id="5379c-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5379c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5379c-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5379c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5379c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5379c-129">CommonParameters</span></span>
<span data-ttu-id="5379c-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5379c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5379c-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5379c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5379c-132">입력</span><span class="sxs-lookup"><span data-stu-id="5379c-132">INPUTS</span></span>

### <span data-ttu-id="5379c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5379c-133">System.String</span></span>

### <span data-ttu-id="5379c-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="5379c-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="5379c-135">출력</span><span class="sxs-lookup"><span data-stu-id="5379c-135">OUTPUTS</span></span>

### <span data-ttu-id="5379c-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5379c-136">System.Boolean</span></span>

## <span data-ttu-id="5379c-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5379c-137">NOTES</span></span>

## <span data-ttu-id="5379c-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5379c-138">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ef27923fbffc92a0190419cc5949c0b841b95dc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381242"
---
# <span data-ttu-id="98a03-101">Update-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="98a03-101">Update-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="98a03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98a03-102">SYNOPSIS</span></span>
<span data-ttu-id="98a03-103">Application Insights 연결된 저장소 계정 업데이트</span><span class="sxs-lookup"><span data-stu-id="98a03-103">Update application insights linked storage account</span></span>

## <span data-ttu-id="98a03-104">구문</span><span class="sxs-lookup"><span data-stu-id="98a03-104">SYNTAX</span></span>

### <span data-ttu-id="98a03-105">ByResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="98a03-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98a03-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98a03-106">ByInputObjectParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98a03-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98a03-107">ByResourceIdParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98a03-108">설명</span><span class="sxs-lookup"><span data-stu-id="98a03-108">DESCRIPTION</span></span>
<span data-ttu-id="98a03-109">Application Insights 연결된 저장소 계정 업데이트</span><span class="sxs-lookup"><span data-stu-id="98a03-109">Update application insights linked storage account</span></span>

## <span data-ttu-id="98a03-110">예제</span><span class="sxs-lookup"><span data-stu-id="98a03-110">EXAMPLES</span></span>

### <span data-ttu-id="98a03-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="98a03-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Update-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="98a03-112">구성 요소 "componentName"에서 연결된 저장소 계정을 업데이트하여 $account</span><span class="sxs-lookup"><span data-stu-id="98a03-112">Update linked storage account under component "componentName" to associate with $account</span></span>

## <span data-ttu-id="98a03-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98a03-113">PARAMETERS</span></span>

### <span data-ttu-id="98a03-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="98a03-114">-ComponentName</span></span>
<span data-ttu-id="98a03-115">구성 요소 이름</span><span class="sxs-lookup"><span data-stu-id="98a03-115">Component Name</span></span>

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

### <span data-ttu-id="98a03-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98a03-116">-DefaultProfile</span></span>
<span data-ttu-id="98a03-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="98a03-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98a03-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98a03-118">-InputObject</span></span>
<span data-ttu-id="98a03-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="98a03-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="98a03-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="98a03-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="98a03-121">Storage 계정 ResourceId</span><span class="sxs-lookup"><span data-stu-id="98a03-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="98a03-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98a03-122">-ResourceGroupName</span></span>
<span data-ttu-id="98a03-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="98a03-123">Resource Group Name</span></span>

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

### <span data-ttu-id="98a03-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98a03-124">-ResourceId</span></span>
<span data-ttu-id="98a03-125">구성 요소 ResourceId</span><span class="sxs-lookup"><span data-stu-id="98a03-125">Component ResourceId</span></span>

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

### <span data-ttu-id="98a03-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98a03-126">-Confirm</span></span>
<span data-ttu-id="98a03-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="98a03-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98a03-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98a03-128">-WhatIf</span></span>
<span data-ttu-id="98a03-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="98a03-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98a03-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="98a03-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98a03-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a03-131">CommonParameters</span></span>
<span data-ttu-id="98a03-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="98a03-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98a03-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="98a03-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a03-134">입력</span><span class="sxs-lookup"><span data-stu-id="98a03-134">INPUTS</span></span>

### <span data-ttu-id="98a03-135">System.String</span><span class="sxs-lookup"><span data-stu-id="98a03-135">System.String</span></span>

### <span data-ttu-id="98a03-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="98a03-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="98a03-137">출력</span><span class="sxs-lookup"><span data-stu-id="98a03-137">OUTPUTS</span></span>

### <span data-ttu-id="98a03-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="98a03-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="98a03-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="98a03-139">NOTES</span></span>

## <span data-ttu-id="98a03-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98a03-140">RELATED LINKS</span></span>

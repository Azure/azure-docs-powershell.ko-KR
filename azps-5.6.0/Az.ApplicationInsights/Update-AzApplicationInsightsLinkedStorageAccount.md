---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/update-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 50391bcd4356f24db6107a64ee5bdec9827407f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972240"
---
# <span data-ttu-id="5a7a3-101">Update-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5a7a3-101">Update-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="5a7a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a7a3-102">SYNOPSIS</span></span>
<span data-ttu-id="5a7a3-103">애플리케이션 인사이트 연결된 저장소 계정 업데이트</span><span class="sxs-lookup"><span data-stu-id="5a7a3-103">Update application insights linked storage account</span></span>

## <span data-ttu-id="5a7a3-104">구문</span><span class="sxs-lookup"><span data-stu-id="5a7a3-104">SYNTAX</span></span>

### <span data-ttu-id="5a7a3-105">ByResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5a7a3-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a7a3-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a7a3-106">ByInputObjectParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a7a3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a7a3-107">ByResourceIdParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a7a3-108">설명</span><span class="sxs-lookup"><span data-stu-id="5a7a3-108">DESCRIPTION</span></span>
<span data-ttu-id="5a7a3-109">애플리케이션 인사이트 연결된 저장소 계정 업데이트</span><span class="sxs-lookup"><span data-stu-id="5a7a3-109">Update application insights linked storage account</span></span>

## <span data-ttu-id="5a7a3-110">예제</span><span class="sxs-lookup"><span data-stu-id="5a7a3-110">EXAMPLES</span></span>

### <span data-ttu-id="5a7a3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5a7a3-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Update-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="5a7a3-112">구성 요소 "componentName"에서 연결된 저장소 계정을 업데이트하여 $account</span><span class="sxs-lookup"><span data-stu-id="5a7a3-112">Update linked storage account under component "componentName" to associate with $account</span></span>

## <span data-ttu-id="5a7a3-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5a7a3-113">PARAMETERS</span></span>

### <span data-ttu-id="5a7a3-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="5a7a3-114">-ComponentName</span></span>
<span data-ttu-id="5a7a3-115">구성 요소 이름</span><span class="sxs-lookup"><span data-stu-id="5a7a3-115">Component Name</span></span>

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

### <span data-ttu-id="5a7a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a7a3-116">-DefaultProfile</span></span>
<span data-ttu-id="5a7a3-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5a7a3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a7a3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a7a3-118">-InputObject</span></span>
<span data-ttu-id="5a7a3-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="5a7a3-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="5a7a3-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="5a7a3-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="5a7a3-121">Storage 계정 ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a7a3-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="5a7a3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a7a3-122">-ResourceGroupName</span></span>
<span data-ttu-id="5a7a3-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="5a7a3-123">Resource Group Name</span></span>

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

### <span data-ttu-id="5a7a3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a7a3-124">-ResourceId</span></span>
<span data-ttu-id="5a7a3-125">구성 요소 ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a7a3-125">Component ResourceId</span></span>

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

### <span data-ttu-id="5a7a3-126">-확인</span><span class="sxs-lookup"><span data-stu-id="5a7a3-126">-Confirm</span></span>
<span data-ttu-id="5a7a3-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a7a3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a7a3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a7a3-128">-WhatIf</span></span>
<span data-ttu-id="5a7a3-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5a7a3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a7a3-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5a7a3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a7a3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a7a3-131">CommonParameters</span></span>
<span data-ttu-id="5a7a3-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7a3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a7a3-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a7a3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a7a3-134">입력</span><span class="sxs-lookup"><span data-stu-id="5a7a3-134">INPUTS</span></span>

### <span data-ttu-id="5a7a3-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5a7a3-135">System.String</span></span>

### <span data-ttu-id="5a7a3-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="5a7a3-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="5a7a3-137">출력</span><span class="sxs-lookup"><span data-stu-id="5a7a3-137">OUTPUTS</span></span>

### <span data-ttu-id="5a7a3-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="5a7a3-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="5a7a3-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5a7a3-139">NOTES</span></span>

## <span data-ttu-id="5a7a3-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a7a3-140">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 652a5668bd641ae1b68093f431e0aa0963aca50b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381333"
---
# <span data-ttu-id="c8c8c-101">New-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8c8c-101">New-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="c8c8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8c8c-102">SYNOPSIS</span></span>
<span data-ttu-id="c8c8c-103">Application Insights 연결된 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="c8c8c-103">Create an application insights linked storage account</span></span>

## <span data-ttu-id="c8c8c-104">구문</span><span class="sxs-lookup"><span data-stu-id="c8c8c-104">SYNTAX</span></span>

### <span data-ttu-id="c8c8c-105">ByResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c8c8c-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8c8c-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8c8c-106">ByInputObjectParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8c8c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8c8c-107">ByResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8c8c-108">설명</span><span class="sxs-lookup"><span data-stu-id="c8c8c-108">DESCRIPTION</span></span>
<span data-ttu-id="c8c8c-109">Application Insights 연결된 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="c8c8c-109">Create an application insights linked storage account</span></span>

## <span data-ttu-id="c8c8c-110">예제</span><span class="sxs-lookup"><span data-stu-id="c8c8c-110">EXAMPLES</span></span>

### <span data-ttu-id="c8c8c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c8c8c-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | New-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="c8c8c-112">구성 요소 "componentName$account 아래에서 연결된 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="c8c8c-112">Create linked storage account $account under component "componentName"</span></span>

## <span data-ttu-id="c8c8c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8c8c-113">PARAMETERS</span></span>

### <span data-ttu-id="c8c8c-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="c8c8c-114">-ComponentName</span></span>
<span data-ttu-id="c8c8c-115">구성 요소 이름</span><span class="sxs-lookup"><span data-stu-id="c8c8c-115">Component Name</span></span>

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

### <span data-ttu-id="c8c8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8c8c-116">-DefaultProfile</span></span>
<span data-ttu-id="c8c8c-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c8c8c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8c8c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8c8c-118">-InputObject</span></span>
<span data-ttu-id="c8c8c-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c8c8c-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="c8c8c-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c8c8c-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="c8c8c-121">Storage 계정 ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8c8c-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="c8c8c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8c8c-122">-ResourceGroupName</span></span>
<span data-ttu-id="c8c8c-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c8c8c-123">Resource Group Name</span></span>

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

### <span data-ttu-id="c8c8c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8c8c-124">-ResourceId</span></span>
<span data-ttu-id="c8c8c-125">구성 요소 ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8c8c-125">Component ResourceId</span></span>

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

### <span data-ttu-id="c8c8c-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8c8c-126">-Confirm</span></span>
<span data-ttu-id="c8c8c-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8c8c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8c8c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8c8c-128">-WhatIf</span></span>
<span data-ttu-id="c8c8c-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c8c8c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8c8c-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8c8c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8c8c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8c8c-131">CommonParameters</span></span>
<span data-ttu-id="c8c8c-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c8c8c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8c8c-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c8c8c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8c8c-134">입력</span><span class="sxs-lookup"><span data-stu-id="c8c8c-134">INPUTS</span></span>

### <span data-ttu-id="c8c8c-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c8c8c-135">System.String</span></span>

### <span data-ttu-id="c8c8c-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c8c8c-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="c8c8c-137">출력</span><span class="sxs-lookup"><span data-stu-id="c8c8c-137">OUTPUTS</span></span>

### <span data-ttu-id="c8c8c-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="c8c8c-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="c8c8c-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c8c8c-139">NOTES</span></span>

## <span data-ttu-id="c8c8c-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c8c8c-140">RELATED LINKS</span></span>

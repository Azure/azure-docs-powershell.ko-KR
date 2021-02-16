---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195436"
---
# <span data-ttu-id="d70ab-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="d70ab-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="d70ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d70ab-102">SYNOPSIS</span></span>
<span data-ttu-id="d70ab-103">Azure PowerShell cmdlet을 사용하여 사용자 환경을 개선하기 위해 Azure PowerShell에서 데이터를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d70ab-103">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="d70ab-104">이 cmdlet을 실행하면 현재 컴퓨터의 현재 사용자에 대한 데이터 수집을 옵트인합니다.</span><span class="sxs-lookup"><span data-stu-id="d70ab-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="d70ab-105">명시적으로 옵트아웃하지 않는 한 기본적으로 데이터가 수집됩니다.</span><span class="sxs-lookup"><span data-stu-id="d70ab-105">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="d70ab-106">구문</span><span class="sxs-lookup"><span data-stu-id="d70ab-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d70ab-107">설명</span><span class="sxs-lookup"><span data-stu-id="d70ab-107">DESCRIPTION</span></span>

<span data-ttu-id="d70ab-108">`Enable-AzDataCollection`cmdlet은 데이터 수집에 옵트인하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d70ab-108">The `Enable-AzDataCollection` cmdlet is used to opt in to data collection.</span></span> <span data-ttu-id="d70ab-109">Azure PowerShell은 기본적으로 원격 분석 데이터를 자동으로 수집합니다.</span><span class="sxs-lookup"><span data-stu-id="d70ab-109">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="d70ab-110">Microsoft는 수집된 데이터를 집계하여 사용 패턴을 식별하고, 일반적인 문제를 식별하고, Azure PowerShell의 환경을 개선합니다.</span><span class="sxs-lookup"><span data-stu-id="d70ab-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="d70ab-111">Microsoft Azure PowerShell은 개인 또는 개인 데이터를 수집하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d70ab-111">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="d70ab-112">데이터 수집을 사용하지 않도록 설정하려면 다음을 실행하여 명시적으로 옵트아웃해야 `Disable-AzDataCollection` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d70ab-112">To disable data collection, you must explicitly opt out by executing `Disable-AzDataCollection`.</span></span>

## <span data-ttu-id="d70ab-113">예제</span><span class="sxs-lookup"><span data-stu-id="d70ab-113">EXAMPLES</span></span>

### <span data-ttu-id="d70ab-114">예제 1: 현재 사용자에 대해 데이터 수집 사용</span><span class="sxs-lookup"><span data-stu-id="d70ab-114">Example 1: Enabling data collection for the current user</span></span>

<span data-ttu-id="d70ab-115">다음 예제에서는 현재 사용자에 대해 데이터 수집을 사용하도록 설정하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d70ab-115">The following example shows how to enable data collection for the current user.</span></span>

```powershell
Enable-AzDataCollection
```

## <span data-ttu-id="d70ab-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d70ab-116">PARAMETERS</span></span>

### <span data-ttu-id="d70ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d70ab-117">-DefaultProfile</span></span>

<span data-ttu-id="d70ab-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d70ab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d70ab-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d70ab-119">-Confirm</span></span>

<span data-ttu-id="d70ab-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d70ab-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d70ab-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d70ab-121">-WhatIf</span></span>

<span data-ttu-id="d70ab-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d70ab-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d70ab-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d70ab-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d70ab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d70ab-124">CommonParameters</span></span>

<span data-ttu-id="d70ab-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d70ab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d70ab-126">자세한 내용은 [다음](/powershell/module/microsoft.powershell.core/about/about_commonparameters)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d70ab-126">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="d70ab-127">입력</span><span class="sxs-lookup"><span data-stu-id="d70ab-127">INPUTS</span></span>

### <span data-ttu-id="d70ab-128">없음</span><span class="sxs-lookup"><span data-stu-id="d70ab-128">None</span></span>

## <span data-ttu-id="d70ab-129">출력</span><span class="sxs-lookup"><span data-stu-id="d70ab-129">OUTPUTS</span></span>

### <span data-ttu-id="d70ab-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="d70ab-130">System.Void</span></span>

## <span data-ttu-id="d70ab-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d70ab-131">NOTES</span></span>

## <span data-ttu-id="d70ab-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d70ab-132">RELATED LINKS</span></span>

[<span data-ttu-id="d70ab-133">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="d70ab-133">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)

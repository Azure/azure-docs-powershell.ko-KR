---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195457"
---
# <span data-ttu-id="26cad-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="26cad-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="26cad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26cad-102">SYNOPSIS</span></span>
<span data-ttu-id="26cad-103">Azure PowerShell cmdlet을 개선하기 위해 데이터 수집을 옵트아웃합니다.</span><span class="sxs-lookup"><span data-stu-id="26cad-103">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="26cad-104">명시적으로 옵트아웃하지 않는 한 기본적으로 데이터가 수집됩니다.</span><span class="sxs-lookup"><span data-stu-id="26cad-104">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="26cad-105">구문</span><span class="sxs-lookup"><span data-stu-id="26cad-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26cad-106">설명</span><span class="sxs-lookup"><span data-stu-id="26cad-106">DESCRIPTION</span></span>

<span data-ttu-id="26cad-107">`Disable-AzDataCollection`cmdlet은 데이터 수집을 옵트아웃하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="26cad-107">The `Disable-AzDataCollection` cmdlet is used to opt out of data collection.</span></span> <span data-ttu-id="26cad-108">Azure PowerShell은 기본적으로 원격 분석 데이터를 자동으로 수집합니다.</span><span class="sxs-lookup"><span data-stu-id="26cad-108">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="26cad-109">데이터 수집을 사용하지 않도록 설정하려면 명시적으로 옵트아웃해야 합니다. Microsoft는 수집된 데이터를 집계하여 사용 패턴을 식별하고, 일반적인 문제를 식별하고, Azure PowerShell의 환경을 개선합니다.</span><span class="sxs-lookup"><span data-stu-id="26cad-109">To disable data collection, you must explicitly opt-out. Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="26cad-110">Microsoft Azure PowerShell은 개인 또는 개인 데이터를 수집하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26cad-110">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="26cad-111">이전에 옵트아웃한 경우 cmdlet을 실행하여 현재 머신에서 현재 사용자에 대한 데이터 수집을 `Enable-AzDataCollection` 다시 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="26cad-111">If you've previously opted out, run the `Enable-AzDataCollection` cmdlet to re-enable data collection for the current user on the current machine.</span></span>

## <span data-ttu-id="26cad-112">예제</span><span class="sxs-lookup"><span data-stu-id="26cad-112">EXAMPLES</span></span>

### <span data-ttu-id="26cad-113">예제 1: 현재 사용자에 대한 데이터 수집 사용 안 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="26cad-113">Example 1: Disabling data collection for the current user</span></span>

<span data-ttu-id="26cad-114">다음 예제에서는 현재 사용자에 대해 데이터 수집을 사용하지 않도록 설정하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="26cad-114">The following example shows how to disable data collection for the current user.</span></span>

```powershell
Disable-AzDataCollection
```

## <span data-ttu-id="26cad-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26cad-115">PARAMETERS</span></span>

### <span data-ttu-id="26cad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26cad-116">-DefaultProfile</span></span>

<span data-ttu-id="26cad-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26cad-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26cad-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26cad-118">-Confirm</span></span>

<span data-ttu-id="26cad-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="26cad-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26cad-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26cad-120">-WhatIf</span></span>

<span data-ttu-id="26cad-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="26cad-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26cad-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26cad-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26cad-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26cad-123">CommonParameters</span></span>

<span data-ttu-id="26cad-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="26cad-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26cad-125">자세한 내용은 [다음](/powershell/module/microsoft.powershell.core/about/about_commonparameters)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="26cad-125">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="26cad-126">입력</span><span class="sxs-lookup"><span data-stu-id="26cad-126">INPUTS</span></span>

### <span data-ttu-id="26cad-127">없음</span><span class="sxs-lookup"><span data-stu-id="26cad-127">None</span></span>

## <span data-ttu-id="26cad-128">출력</span><span class="sxs-lookup"><span data-stu-id="26cad-128">OUTPUTS</span></span>

### <span data-ttu-id="26cad-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="26cad-129">System.Void</span></span>

## <span data-ttu-id="26cad-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="26cad-130">NOTES</span></span>

## <span data-ttu-id="26cad-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26cad-131">RELATED LINKS</span></span>

[<span data-ttu-id="26cad-132">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="26cad-132">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)

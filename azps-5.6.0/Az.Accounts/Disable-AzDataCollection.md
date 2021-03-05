---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 54af80b230c3cb031e8927a82ec3536cc1a81ec0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999082"
---
# <span data-ttu-id="c081b-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="c081b-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="c081b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c081b-102">SYNOPSIS</span></span>
<span data-ttu-id="c081b-103">Azure PowerShell cmdlet을 개선하기 위해 데이터 수집을 옵트아웃합니다.</span><span class="sxs-lookup"><span data-stu-id="c081b-103">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="c081b-104">명시적으로 옵트아웃하지 않는 한 데이터는 기본적으로 수집됩니다.</span><span class="sxs-lookup"><span data-stu-id="c081b-104">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="c081b-105">구문</span><span class="sxs-lookup"><span data-stu-id="c081b-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c081b-106">설명</span><span class="sxs-lookup"><span data-stu-id="c081b-106">DESCRIPTION</span></span>

<span data-ttu-id="c081b-107">`Disable-AzDataCollection`cmdlet은 데이터 수집을 옵트아웃하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c081b-107">The `Disable-AzDataCollection` cmdlet is used to opt out of data collection.</span></span> <span data-ttu-id="c081b-108">Azure PowerShell은 기본적으로 원격 분석 데이터를 자동으로 수집합니다.</span><span class="sxs-lookup"><span data-stu-id="c081b-108">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="c081b-109">데이터 수집을 사용하지 않도록 설정하려면 명시적으로 옵트아웃해야 합니다. Microsoft는 수집된 데이터를 집계하여 사용 패턴을 식별하고, 일반적인 문제를 식별하고, Azure PowerShell의 환경을 개선합니다.</span><span class="sxs-lookup"><span data-stu-id="c081b-109">To disable data collection, you must explicitly opt-out. Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="c081b-110">Microsoft Azure PowerShell은 개인 또는 개인 데이터를 수집하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c081b-110">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="c081b-111">이전에 옵트아웃한 경우 cmdlet을 실행하여 현재 컴퓨터의 현재 사용자에 대한 데이터 수집을 `Enable-AzDataCollection` 다시 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c081b-111">If you've previously opted out, run the `Enable-AzDataCollection` cmdlet to re-enable data collection for the current user on the current machine.</span></span>

## <span data-ttu-id="c081b-112">예제</span><span class="sxs-lookup"><span data-stu-id="c081b-112">EXAMPLES</span></span>

### <span data-ttu-id="c081b-113">예제 1: 현재 사용자의 데이터 수집 사용 안 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="c081b-113">Example 1: Disabling data collection for the current user</span></span>

<span data-ttu-id="c081b-114">다음 예제에서는 현재 사용자의 데이터 수집을 사용하지 않도록 설정하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c081b-114">The following example shows how to disable data collection for the current user.</span></span>

```powershell
Disable-AzDataCollection
```

## <span data-ttu-id="c081b-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c081b-115">PARAMETERS</span></span>

### <span data-ttu-id="c081b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c081b-116">-DefaultProfile</span></span>

<span data-ttu-id="c081b-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c081b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c081b-118">-확인</span><span class="sxs-lookup"><span data-stu-id="c081b-118">-Confirm</span></span>

<span data-ttu-id="c081b-119">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c081b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c081b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c081b-120">-WhatIf</span></span>

<span data-ttu-id="c081b-121">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c081b-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c081b-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c081b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c081b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c081b-123">CommonParameters</span></span>
<span data-ttu-id="c081b-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c081b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c081b-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c081b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c081b-126">입력</span><span class="sxs-lookup"><span data-stu-id="c081b-126">INPUTS</span></span>

### <span data-ttu-id="c081b-127">없음</span><span class="sxs-lookup"><span data-stu-id="c081b-127">None</span></span>

## <span data-ttu-id="c081b-128">출력</span><span class="sxs-lookup"><span data-stu-id="c081b-128">OUTPUTS</span></span>

### <span data-ttu-id="c081b-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="c081b-129">System.Void</span></span>

## <span data-ttu-id="c081b-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c081b-130">NOTES</span></span>

## <span data-ttu-id="c081b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c081b-131">RELATED LINKS</span></span>

[<span data-ttu-id="c081b-132">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="c081b-132">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)

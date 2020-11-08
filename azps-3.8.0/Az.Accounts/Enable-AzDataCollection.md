---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/30/2020
ms.locfileid: "94045079"
---
# <span data-ttu-id="c9590-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="c9590-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="c9590-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9590-102">SYNOPSIS</span></span>
<span data-ttu-id="c9590-103">Azure powershell에서 데이터를 수집 하 여 Azure PowerShell cmdlet을 사용 하 여 사용자 환경을 향상 시킬 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9590-103">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="c9590-104">현재 컴퓨터의 현재 사용자에 대 한 데이터 수집에 opts cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9590-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="c9590-105">명시적으로 옵트아웃 하지 않는 한 기본적으로 데이터는 수집 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9590-105">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="c9590-106">구문과</span><span class="sxs-lookup"><span data-stu-id="c9590-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9590-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c9590-107">DESCRIPTION</span></span>

<span data-ttu-id="c9590-108">`Enable-AzDataCollection`Cmdlet을 사용 하 여 데이터 수집을 옵트아웃 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9590-108">The `Enable-AzDataCollection` cmdlet is used to opt in to data collection.</span></span> <span data-ttu-id="c9590-109">Azure PowerShell은 기본적으로 원격 분석 데이터를 자동으로 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9590-109">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="c9590-110">Microsoft는 수집 된 데이터를 집계 하 여 사용 패턴을 식별 하 고, 일반적인 문제를 식별 하 고, Azure PowerShell의 환경을 개선 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9590-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="c9590-111">Microsoft Azure PowerShell은 개인 또는 개인 데이터를 수집 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9590-111">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="c9590-112">데이터 수집을 사용 하지 않도록 설정 하려면를 실행 하 여 명시적으로 옵트아웃 해야 합니다 `Disable-AzDataCollection` .</span><span class="sxs-lookup"><span data-stu-id="c9590-112">To disable data collection, you must explicitly opt out by executing `Disable-AzDataCollection`.</span></span>

## <span data-ttu-id="c9590-113">예제의</span><span class="sxs-lookup"><span data-stu-id="c9590-113">EXAMPLES</span></span>

### <span data-ttu-id="c9590-114">예제 1: 현재 사용자의 데이터 수집 사용</span><span class="sxs-lookup"><span data-stu-id="c9590-114">Example 1: Enabling data collection for the current user</span></span>

<span data-ttu-id="c9590-115">다음 예제에서는 현재 사용자의 데이터 수집을 사용 하도록 설정 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c9590-115">The following example shows how to enable data collection for the current user.</span></span>

```powershell
Enable-AzDataCollection
```

## <span data-ttu-id="c9590-116">변수</span><span class="sxs-lookup"><span data-stu-id="c9590-116">PARAMETERS</span></span>

### <span data-ttu-id="c9590-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9590-117">-DefaultProfile</span></span>

<span data-ttu-id="c9590-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9590-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9590-119">-확인</span><span class="sxs-lookup"><span data-stu-id="c9590-119">-Confirm</span></span>

<span data-ttu-id="c9590-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9590-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9590-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9590-121">-WhatIf</span></span>

<span data-ttu-id="c9590-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c9590-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9590-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9590-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9590-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9590-124">CommonParameters</span></span>

<span data-ttu-id="c9590-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9590-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9590-126">자세한 내용은 [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c9590-126">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="c9590-127">입력</span><span class="sxs-lookup"><span data-stu-id="c9590-127">INPUTS</span></span>

### <span data-ttu-id="c9590-128">않아야</span><span class="sxs-lookup"><span data-stu-id="c9590-128">None</span></span>

## <span data-ttu-id="c9590-129">출력</span><span class="sxs-lookup"><span data-stu-id="c9590-129">OUTPUTS</span></span>

### <span data-ttu-id="c9590-130">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="c9590-130">System.Void</span></span>

## <span data-ttu-id="c9590-131">상속자</span><span class="sxs-lookup"><span data-stu-id="c9590-131">NOTES</span></span>

## <span data-ttu-id="c9590-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9590-132">RELATED LINKS</span></span>

[<span data-ttu-id="c9590-133">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="c9590-133">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)

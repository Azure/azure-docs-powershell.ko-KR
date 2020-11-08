---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/30/2020
ms.locfileid: "94045080"
---
# <span data-ttu-id="78db1-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="78db1-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="78db1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78db1-102">SYNOPSIS</span></span>
<span data-ttu-id="78db1-103">Azure PowerShell cmdlet을 개선 하기 위해 데이터를 수집 하는 Opts.</span><span class="sxs-lookup"><span data-stu-id="78db1-103">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="78db1-104">명시적으로 옵트아웃 하지 않는 한 기본적으로 데이터는 수집 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78db1-104">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="78db1-105">구문과</span><span class="sxs-lookup"><span data-stu-id="78db1-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78db1-106">설명은</span><span class="sxs-lookup"><span data-stu-id="78db1-106">DESCRIPTION</span></span>

<span data-ttu-id="78db1-107">`Disable-AzDataCollection`Cmdlet은 데이터 수집을 옵트아웃 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78db1-107">The `Disable-AzDataCollection` cmdlet is used to opt out of data collection.</span></span> <span data-ttu-id="78db1-108">Azure PowerShell은 기본적으로 원격 분석 데이터를 자동으로 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="78db1-108">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="78db1-109">데이터 수집을 사용 하지 않도록 설정 하려면 명시적으로 옵트아웃 해야 합니다. Microsoft는 수집 된 데이터를 집계 하 여 사용 패턴을 식별 하 고, 일반적인 문제를 식별 하 고, Azure PowerShell의 환경을 개선 합니다.</span><span class="sxs-lookup"><span data-stu-id="78db1-109">To disable data collection, you must explicitly opt-out. Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="78db1-110">Microsoft Azure PowerShell은 개인 또는 개인 데이터를 수집 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78db1-110">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="78db1-111">이전에 옵트아웃 한 경우 cmdlet을 실행 `Enable-AzDataCollection` 하 여 현재 컴퓨터의 현재 사용자에 대 한 데이터 수집을 다시 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78db1-111">If you've previously opted out, run the `Enable-AzDataCollection` cmdlet to re-enable data collection for the current user on the current machine.</span></span>

## <span data-ttu-id="78db1-112">예제의</span><span class="sxs-lookup"><span data-stu-id="78db1-112">EXAMPLES</span></span>

### <span data-ttu-id="78db1-113">예제 1: 현재 사용자에 대해 데이터 수집을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="78db1-113">Example 1: Disabling data collection for the current user</span></span>

<span data-ttu-id="78db1-114">다음 예제에서는 현재 사용자의 데이터 수집을 사용 하지 않도록 설정 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="78db1-114">The following example shows how to disable data collection for the current user.</span></span>

```powershell
Disable-AzDataCollection
```

## <span data-ttu-id="78db1-115">변수</span><span class="sxs-lookup"><span data-stu-id="78db1-115">PARAMETERS</span></span>

### <span data-ttu-id="78db1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78db1-116">-DefaultProfile</span></span>

<span data-ttu-id="78db1-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78db1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78db1-118">-확인</span><span class="sxs-lookup"><span data-stu-id="78db1-118">-Confirm</span></span>

<span data-ttu-id="78db1-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="78db1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78db1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78db1-120">-WhatIf</span></span>

<span data-ttu-id="78db1-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="78db1-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78db1-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78db1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78db1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78db1-123">CommonParameters</span></span>

<span data-ttu-id="78db1-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78db1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78db1-125">자세한 내용은 [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="78db1-125">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="78db1-126">입력</span><span class="sxs-lookup"><span data-stu-id="78db1-126">INPUTS</span></span>

### <span data-ttu-id="78db1-127">않아야</span><span class="sxs-lookup"><span data-stu-id="78db1-127">None</span></span>

## <span data-ttu-id="78db1-128">출력</span><span class="sxs-lookup"><span data-stu-id="78db1-128">OUTPUTS</span></span>

### <span data-ttu-id="78db1-129">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="78db1-129">System.Void</span></span>

## <span data-ttu-id="78db1-130">상속자</span><span class="sxs-lookup"><span data-stu-id="78db1-130">NOTES</span></span>

## <span data-ttu-id="78db1-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78db1-131">RELATED LINKS</span></span>

[<span data-ttu-id="78db1-132">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="78db1-132">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)

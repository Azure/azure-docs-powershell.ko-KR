---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: c9cfd91ecc094ad5df98d3c8478d197fbfa98a15
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875304"
---
# <span data-ttu-id="d2c31-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="d2c31-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="d2c31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2c31-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c31-103">Azure PowerShell에서 데이터를 수집 하 여 AzurePowerShell cmdlet을 사용 하 여 사용자 환경을 향상 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2c31-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="d2c31-104">현재 컴퓨터의 현재 사용자에 대 한 데이터 수집에 opts cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2c31-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="d2c31-105">명시적으로 옵트인 하지 않는 한 데이터는 수집 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2c31-105">No data is collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="d2c31-106">구문과</span><span class="sxs-lookup"><span data-stu-id="d2c31-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2c31-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d2c31-107">DESCRIPTION</span></span>
<span data-ttu-id="d2c31-108">데이터 수집을 통해 Microsoft 클라우드 및 Azure PowerShell을 사용 하는 환경을 개선할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2c31-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="d2c31-109">Azure PowerShell이 동의 하지 않고 데이터를 수집 하지 않음-AzDataCollection를 실행 하 여 명시적으로 옵트인 하거나 cmdlet을 처음 실행할 때 Azure PowerShell에 데이터 수집에 대 한 메시지가 표시 되 면 예를 사용 하 여 사용자에 게 응답 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2c31-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="d2c31-110">Microsoft는 일반적인 문제를 식별 하 고 Azure PowerShell을 사용 하는 환경을 개선 하기 위해 사용 패턴을 식별 하기 위해 수집 된 데이터를 집계 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2c31-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="d2c31-111">Microsoft Azure PowerShell은 개인 데이터 또는 개인 식별이 가능한 정보를 수집 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2c31-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>
<span data-ttu-id="d2c31-112">현재 컴퓨터에서 현재 사용자의 데이터 수집을 사용 하도록 설정 하려면 Enable-AzDataCollection cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2c31-112">Run the Enable-AzDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="d2c31-113">이렇게 하면 첫 번째 cmdlet이 실행 될 때 현재 사용자에 게 데이터 수집에 대 한 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2c31-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>
<span data-ttu-id="d2c31-114">현재 사용자에 대 한 데이터 수집을 사용 하지 않도록 설정 하려면 Disable-AzDataCollection cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2c31-114">To disable data collection for the current user, run the Disable-AzDataCollection cmdlet.</span></span>

## <span data-ttu-id="d2c31-115">예제의</span><span class="sxs-lookup"><span data-stu-id="d2c31-115">EXAMPLES</span></span>

### <span data-ttu-id="d2c31-116">예제 1: 현재 사용자의 데이터 수집 사용</span><span class="sxs-lookup"><span data-stu-id="d2c31-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzDataCollection
```

<span data-ttu-id="d2c31-117">이 예제에서는 현재 사용자의 데이터 수집을 사용 하도록 설정 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d2c31-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="d2c31-118">변수</span><span class="sxs-lookup"><span data-stu-id="d2c31-118">PARAMETERS</span></span>

### <span data-ttu-id="d2c31-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c31-119">-DefaultProfile</span></span>
<span data-ttu-id="d2c31-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2c31-120">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2c31-121">-확인</span><span class="sxs-lookup"><span data-stu-id="d2c31-121">-Confirm</span></span>
<span data-ttu-id="d2c31-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2c31-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2c31-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2c31-123">-WhatIf</span></span>
<span data-ttu-id="d2c31-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d2c31-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2c31-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2c31-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2c31-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c31-126">CommonParameters</span></span>
<span data-ttu-id="d2c31-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2c31-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c31-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d2c31-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c31-129">입력</span><span class="sxs-lookup"><span data-stu-id="d2c31-129">INPUTS</span></span>

### <span data-ttu-id="d2c31-130">않아야</span><span class="sxs-lookup"><span data-stu-id="d2c31-130">None</span></span>

## <span data-ttu-id="d2c31-131">출력</span><span class="sxs-lookup"><span data-stu-id="d2c31-131">OUTPUTS</span></span>

### <span data-ttu-id="d2c31-132">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="d2c31-132">System.Void</span></span>

## <span data-ttu-id="d2c31-133">상속자</span><span class="sxs-lookup"><span data-stu-id="d2c31-133">NOTES</span></span>

## <span data-ttu-id="d2c31-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2c31-134">RELATED LINKS</span></span>

[<span data-ttu-id="d2c31-135">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="d2c31-135">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)


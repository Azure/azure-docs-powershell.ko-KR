---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 9507271fe283277c212e4ed8d4117483a2797857
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969659"
---
# <span data-ttu-id="d5166-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="d5166-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="d5166-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5166-102">SYNOPSIS</span></span>
<span data-ttu-id="d5166-103">리소스 이름을 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5166-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="d5166-104">구문</span><span class="sxs-lookup"><span data-stu-id="d5166-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d5166-105">설명</span><span class="sxs-lookup"><span data-stu-id="d5166-105">DESCRIPTION</span></span>
<span data-ttu-id="d5166-106">리소스 이름을 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5166-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="d5166-107">예제</span><span class="sxs-lookup"><span data-stu-id="d5166-107">EXAMPLES</span></span>

### <span data-ttu-id="d5166-108">예제 1: 리소스 이름을 사용할 수 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="d5166-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="d5166-109">명령은 리소스 이름을 사용할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="d5166-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="d5166-110">예제 2: 리소스 이름을 사용할 수 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="d5166-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="d5166-111">명령은 리소스 이름을 사용할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="d5166-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="d5166-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d5166-112">PARAMETERS</span></span>

### <span data-ttu-id="d5166-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5166-113">-DefaultProfile</span></span>
<span data-ttu-id="d5166-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5166-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5166-115">-Location</span><span class="sxs-lookup"><span data-stu-id="d5166-115">-Location</span></span>
<span data-ttu-id="d5166-116">위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5166-116">Location Name.</span></span>

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

### <span data-ttu-id="d5166-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d5166-117">-Name</span></span>
<span data-ttu-id="d5166-118">확인할 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d5166-118">Gets or sets the name to check.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5166-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5166-119">-SubscriptionId</span></span>
<span data-ttu-id="d5166-120">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d5166-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d5166-121">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="d5166-121">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5166-122">-Type</span><span class="sxs-lookup"><span data-stu-id="d5166-122">-Type</span></span>
<span data-ttu-id="d5166-123">확인할 리소스 유형을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d5166-123">Gets or sets the type of the resource to check.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5166-124">-확인</span><span class="sxs-lookup"><span data-stu-id="d5166-124">-Confirm</span></span>
<span data-ttu-id="d5166-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5166-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5166-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5166-126">-WhatIf</span></span>
<span data-ttu-id="d5166-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d5166-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5166-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5166-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5166-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5166-129">CommonParameters</span></span>
<span data-ttu-id="d5166-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d5166-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5166-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5166-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5166-132">입력</span><span class="sxs-lookup"><span data-stu-id="d5166-132">INPUTS</span></span>

## <span data-ttu-id="d5166-133">출력</span><span class="sxs-lookup"><span data-stu-id="d5166-133">OUTPUTS</span></span>

### <span data-ttu-id="d5166-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span><span class="sxs-lookup"><span data-stu-id="d5166-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="d5166-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d5166-135">NOTES</span></span>

<span data-ttu-id="d5166-136">별칭</span><span class="sxs-lookup"><span data-stu-id="d5166-136">ALIASES</span></span>

## <span data-ttu-id="d5166-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5166-137">RELATED LINKS</span></span>


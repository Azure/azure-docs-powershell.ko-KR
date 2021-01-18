---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 42bd50dd96d235db823ec12498388f78d5ec641c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496208"
---
# <span data-ttu-id="d166c-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="d166c-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="d166c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d166c-102">SYNOPSIS</span></span>
<span data-ttu-id="d166c-103">리소스 이름을 사용할 수 있는지 여부를 확인</span><span class="sxs-lookup"><span data-stu-id="d166c-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="d166c-104">구문</span><span class="sxs-lookup"><span data-stu-id="d166c-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d166c-105">설명</span><span class="sxs-lookup"><span data-stu-id="d166c-105">DESCRIPTION</span></span>
<span data-ttu-id="d166c-106">리소스 이름을 사용할 수 있는지 여부를 확인</span><span class="sxs-lookup"><span data-stu-id="d166c-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="d166c-107">예제</span><span class="sxs-lookup"><span data-stu-id="d166c-107">EXAMPLES</span></span>

### <span data-ttu-id="d166c-108">예제 1: 리소스 이름을 사용할 수 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="d166c-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="d166c-109">이 명령은 리소스 이름을 사용할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="d166c-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="d166c-110">예제 2: 리소스 이름을 사용할 수 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="d166c-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="d166c-111">이 명령은 리소스 이름을 사용할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="d166c-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="d166c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d166c-112">PARAMETERS</span></span>

### <span data-ttu-id="d166c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d166c-113">-DefaultProfile</span></span>
<span data-ttu-id="d166c-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d166c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d166c-115">-Location</span><span class="sxs-lookup"><span data-stu-id="d166c-115">-Location</span></span>
<span data-ttu-id="d166c-116">위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d166c-116">Location Name.</span></span>

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

### <span data-ttu-id="d166c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d166c-117">-Name</span></span>
<span data-ttu-id="d166c-118">확인할 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d166c-118">Gets or sets the name to check.</span></span>

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

### <span data-ttu-id="d166c-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d166c-119">-SubscriptionId</span></span>
<span data-ttu-id="d166c-120">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d166c-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d166c-121">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="d166c-121">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d166c-122">-Type</span><span class="sxs-lookup"><span data-stu-id="d166c-122">-Type</span></span>
<span data-ttu-id="d166c-123">확인할 리소스의 유형을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d166c-123">Gets or sets the type of the resource to check.</span></span>

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

### <span data-ttu-id="d166c-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d166c-124">-Confirm</span></span>
<span data-ttu-id="d166c-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d166c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d166c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d166c-126">-WhatIf</span></span>
<span data-ttu-id="d166c-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d166c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d166c-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d166c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d166c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d166c-129">CommonParameters</span></span>
<span data-ttu-id="d166c-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d166c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d166c-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d166c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d166c-132">입력</span><span class="sxs-lookup"><span data-stu-id="d166c-132">INPUTS</span></span>

## <span data-ttu-id="d166c-133">출력</span><span class="sxs-lookup"><span data-stu-id="d166c-133">OUTPUTS</span></span>

### <span data-ttu-id="d166c-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span><span class="sxs-lookup"><span data-stu-id="d166c-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="d166c-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d166c-135">NOTES</span></span>

<span data-ttu-id="d166c-136">별칭</span><span class="sxs-lookup"><span data-stu-id="d166c-136">ALIASES</span></span>

## <span data-ttu-id="d166c-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d166c-137">RELATED LINKS</span></span>


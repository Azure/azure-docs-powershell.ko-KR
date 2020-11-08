---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 42bd50dd96d235db823ec12498388f78d5ec641c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218418"
---
# <span data-ttu-id="ea374-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ea374-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="ea374-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea374-102">SYNOPSIS</span></span>
<span data-ttu-id="ea374-103">리소스 이름을 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea374-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="ea374-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea374-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ea374-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ea374-105">DESCRIPTION</span></span>
<span data-ttu-id="ea374-106">리소스 이름을 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea374-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="ea374-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ea374-107">EXAMPLES</span></span>

### <span data-ttu-id="ea374-108">예제 1: 리소스 이름을 사용할 수 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="ea374-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="ea374-109">이 명령은 리소스 이름을 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea374-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="ea374-110">예제 2: 리소스 이름을 사용할 수 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="ea374-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="ea374-111">이 명령은 리소스 이름을 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea374-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="ea374-112">변수</span><span class="sxs-lookup"><span data-stu-id="ea374-112">PARAMETERS</span></span>

### <span data-ttu-id="ea374-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea374-113">-DefaultProfile</span></span>
<span data-ttu-id="ea374-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea374-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea374-115">-위치</span><span class="sxs-lookup"><span data-stu-id="ea374-115">-Location</span></span>
<span data-ttu-id="ea374-116">위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea374-116">Location Name.</span></span>

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

### <span data-ttu-id="ea374-117">-이름</span><span class="sxs-lookup"><span data-stu-id="ea374-117">-Name</span></span>
<span data-ttu-id="ea374-118">확인할 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea374-118">Gets or sets the name to check.</span></span>

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

### <span data-ttu-id="ea374-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea374-119">-SubscriptionId</span></span>
<span data-ttu-id="ea374-120">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea374-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ea374-121">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="ea374-121">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ea374-122">-Type</span><span class="sxs-lookup"><span data-stu-id="ea374-122">-Type</span></span>
<span data-ttu-id="ea374-123">확인할 리소스의 형식을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea374-123">Gets or sets the type of the resource to check.</span></span>

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

### <span data-ttu-id="ea374-124">-확인</span><span class="sxs-lookup"><span data-stu-id="ea374-124">-Confirm</span></span>
<span data-ttu-id="ea374-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea374-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea374-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea374-126">-WhatIf</span></span>
<span data-ttu-id="ea374-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ea374-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea374-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea374-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea374-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea374-129">CommonParameters</span></span>
<span data-ttu-id="ea374-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea374-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea374-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea374-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea374-132">입력</span><span class="sxs-lookup"><span data-stu-id="ea374-132">INPUTS</span></span>

## <span data-ttu-id="ea374-133">출력</span><span class="sxs-lookup"><span data-stu-id="ea374-133">OUTPUTS</span></span>

### <span data-ttu-id="ea374-134">Api20180601Preview를 사용 하는 경우의. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ea374-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="ea374-135">상속자</span><span class="sxs-lookup"><span data-stu-id="ea374-135">NOTES</span></span>

<span data-ttu-id="ea374-136">별칭과</span><span class="sxs-lookup"><span data-stu-id="ea374-136">ALIASES</span></span>

## <span data-ttu-id="ea374-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea374-137">RELATED LINKS</span></span>


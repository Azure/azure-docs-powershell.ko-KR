---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: a76c993abb254b1e24200267bf0195cb613d8207
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217978"
---
# <span data-ttu-id="79d98-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="79d98-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="79d98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79d98-102">SYNOPSIS</span></span>
<span data-ttu-id="79d98-103">구독 별칭 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79d98-103">Gets subscription alias details</span></span>

## <span data-ttu-id="79d98-104">구문과</span><span class="sxs-lookup"><span data-stu-id="79d98-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79d98-105">설명은</span><span class="sxs-lookup"><span data-stu-id="79d98-105">DESCRIPTION</span></span>
<span data-ttu-id="79d98-106">**Get-AzSubscriptionAlias** cmdlet은 구독 별칭 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79d98-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="79d98-107">예제의</span><span class="sxs-lookup"><span data-stu-id="79d98-107">EXAMPLES</span></span>

### <span data-ttu-id="79d98-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="79d98-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="79d98-109">구독 별칭 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79d98-109">Gets subscription alias details</span></span>

## <span data-ttu-id="79d98-110">변수</span><span class="sxs-lookup"><span data-stu-id="79d98-110">PARAMETERS</span></span>

### <span data-ttu-id="79d98-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="79d98-111">-AliasName</span></span>
<span data-ttu-id="79d98-112">구독에 대 한 별칭</span><span class="sxs-lookup"><span data-stu-id="79d98-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="79d98-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79d98-113">-AsJob</span></span>
<span data-ttu-id="79d98-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="79d98-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d98-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79d98-115">-DefaultProfile</span></span>
<span data-ttu-id="79d98-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79d98-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79d98-117">-확인</span><span class="sxs-lookup"><span data-stu-id="79d98-117">-Confirm</span></span>
<span data-ttu-id="79d98-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d98-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79d98-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79d98-119">-WhatIf</span></span>
<span data-ttu-id="79d98-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="79d98-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79d98-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79d98-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79d98-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79d98-122">CommonParameters</span></span>
<span data-ttu-id="79d98-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d98-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79d98-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="79d98-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79d98-125">입력</span><span class="sxs-lookup"><span data-stu-id="79d98-125">INPUTS</span></span>

### <span data-ttu-id="79d98-126">않아야</span><span class="sxs-lookup"><span data-stu-id="79d98-126">None</span></span>

## <span data-ttu-id="79d98-127">출력</span><span class="sxs-lookup"><span data-stu-id="79d98-127">OUTPUTS</span></span>

### <span data-ttu-id="79d98-128">PSAzureSubscription에 대 한.</span><span class="sxs-lookup"><span data-stu-id="79d98-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="79d98-129">상속자</span><span class="sxs-lookup"><span data-stu-id="79d98-129">NOTES</span></span>

## <span data-ttu-id="79d98-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79d98-130">RELATED LINKS</span></span>

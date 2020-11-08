---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/start-azsreclaimstoragecapacity
schema: 2.0.0
ms.openlocfilehash: bb2eecb93a7a18559dc6fbe58cd5f07c737e16b5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045155"
---
# <span data-ttu-id="ecb65-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="ecb65-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="ecb65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecb65-102">SYNOPSIS</span></span>


## <span data-ttu-id="ecb65-103">구문과</span><span class="sxs-lookup"><span data-stu-id="ecb65-103">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ecb65-104">설명은</span><span class="sxs-lookup"><span data-stu-id="ecb65-104">DESCRIPTION</span></span>


## <span data-ttu-id="ecb65-105">예제의</span><span class="sxs-lookup"><span data-stu-id="ecb65-105">EXAMPLES</span></span>

### <span data-ttu-id="ecb65-106">예제 1:</span><span class="sxs-lookup"><span data-stu-id="ecb65-106">Example 1:</span></span>
```powershell
PS C:\> Start-AzsReclaimStorageCapacity
```

<span data-ttu-id="ecb65-107">가비지 수집을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb65-107">Start garbage collection.</span></span>

## <span data-ttu-id="ecb65-108">변수</span><span class="sxs-lookup"><span data-stu-id="ecb65-108">PARAMETERS</span></span>

### <span data-ttu-id="ecb65-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecb65-109">-AsJob</span></span>


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

### <span data-ttu-id="ecb65-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb65-110">-DefaultProfile</span></span>


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

### <span data-ttu-id="ecb65-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ecb65-111">-Force</span></span>


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

### <span data-ttu-id="ecb65-112">-위치</span><span class="sxs-lookup"><span data-stu-id="ecb65-112">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ecb65-113">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ecb65-113">-NoWait</span></span>


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

### <span data-ttu-id="ecb65-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecb65-114">-PassThru</span></span>


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

### <span data-ttu-id="ecb65-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ecb65-115">-SubscriptionId</span></span>


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

### <span data-ttu-id="ecb65-116">-확인</span><span class="sxs-lookup"><span data-stu-id="ecb65-116">-Confirm</span></span>
<span data-ttu-id="ecb65-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb65-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecb65-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecb65-118">-WhatIf</span></span>
<span data-ttu-id="ecb65-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ecb65-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecb65-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecb65-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecb65-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb65-121">CommonParameters</span></span>
<span data-ttu-id="ecb65-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb65-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb65-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ecb65-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb65-124">입력</span><span class="sxs-lookup"><span data-stu-id="ecb65-124">INPUTS</span></span>

## <span data-ttu-id="ecb65-125">출력</span><span class="sxs-lookup"><span data-stu-id="ecb65-125">OUTPUTS</span></span>

### <span data-ttu-id="ecb65-126">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ecb65-126">System.Boolean</span></span>



## <span data-ttu-id="ecb65-127">상속자</span><span class="sxs-lookup"><span data-stu-id="ecb65-127">NOTES</span></span>

## <span data-ttu-id="ecb65-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecb65-128">RELATED LINKS</span></span>


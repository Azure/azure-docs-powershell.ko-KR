---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/restore-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 81b6a6dc960e9364d6d3e54f6e6394e17559b7f8
ms.sourcegitcommit: 5523170e571fbd1dc93bd0fa4223aba3b324d3b0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/25/2020
ms.locfileid: "94045387"
---
# <span data-ttu-id="1dc60-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1dc60-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="1dc60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dc60-102">SYNOPSIS</span></span>


## <span data-ttu-id="1dc60-103">구문과</span><span class="sxs-lookup"><span data-stu-id="1dc60-103">SYNTAX</span></span>

```
Restore-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-NewAccountName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1dc60-104">설명은</span><span class="sxs-lookup"><span data-stu-id="1dc60-104">DESCRIPTION</span></span>


## <span data-ttu-id="1dc60-105">예제의</span><span class="sxs-lookup"><span data-stu-id="1dc60-105">EXAMPLES</span></span>

### <span data-ttu-id="1dc60-106">예제 1:</span><span class="sxs-lookup"><span data-stu-id="1dc60-106">Example 1:</span></span>
```powershell
PS C:\> Restore-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 
```

<span data-ttu-id="1dc60-107">삭제 된 저장소 계정의 삭제를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc60-107">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="1dc60-108">변수</span><span class="sxs-lookup"><span data-stu-id="1dc60-108">PARAMETERS</span></span>

### <span data-ttu-id="1dc60-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1dc60-109">-AsJob</span></span>


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

### <span data-ttu-id="1dc60-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc60-110">-DefaultProfile</span></span>


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

### <span data-ttu-id="1dc60-111">-Force</span><span class="sxs-lookup"><span data-stu-id="1dc60-111">-Force</span></span>


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

### <span data-ttu-id="1dc60-112">-위치</span><span class="sxs-lookup"><span data-stu-id="1dc60-112">-Location</span></span>


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

### <span data-ttu-id="1dc60-113">-이름</span><span class="sxs-lookup"><span data-stu-id="1dc60-113">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1dc60-114">-NewAccountName</span><span class="sxs-lookup"><span data-stu-id="1dc60-114">-NewAccountName</span></span>


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

### <span data-ttu-id="1dc60-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1dc60-115">-NoWait</span></span>


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

### <span data-ttu-id="1dc60-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1dc60-116">-PassThru</span></span>


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

### <span data-ttu-id="1dc60-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1dc60-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="1dc60-118">-확인</span><span class="sxs-lookup"><span data-stu-id="1dc60-118">-Confirm</span></span>
<span data-ttu-id="1dc60-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc60-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dc60-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dc60-120">-WhatIf</span></span>
<span data-ttu-id="1dc60-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1dc60-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dc60-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dc60-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dc60-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc60-123">CommonParameters</span></span>
<span data-ttu-id="1dc60-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc60-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc60-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1dc60-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc60-126">입력</span><span class="sxs-lookup"><span data-stu-id="1dc60-126">INPUTS</span></span>

## <span data-ttu-id="1dc60-127">출력</span><span class="sxs-lookup"><span data-stu-id="1dc60-127">OUTPUTS</span></span>

### <span data-ttu-id="1dc60-128">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1dc60-128">System.Boolean</span></span>



## <span data-ttu-id="1dc60-129">상속자</span><span class="sxs-lookup"><span data-stu-id="1dc60-129">NOTES</span></span>

## <span data-ttu-id="1dc60-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1dc60-130">RELATED LINKS</span></span>


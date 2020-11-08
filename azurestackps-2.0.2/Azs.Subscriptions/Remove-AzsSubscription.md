---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/remove-azssubscription
schema: 2.0.0
ms.openlocfilehash: b6fddf677cd619dad577b7bca8286671b85d0791
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047021"
---
# <span data-ttu-id="71140-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="71140-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="71140-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71140-102">SYNOPSIS</span></span>


## <span data-ttu-id="71140-103">구문과</span><span class="sxs-lookup"><span data-stu-id="71140-103">SYNTAX</span></span>

### <span data-ttu-id="71140-104">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="71140-104">Delete (Default)</span></span>
```
Remove-AzsSubscription -SubscriptionId <String> [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="71140-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="71140-105">DeleteViaIdentity</span></span>
```
Remove-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [-Force] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="71140-106">설명은</span><span class="sxs-lookup"><span data-stu-id="71140-106">DESCRIPTION</span></span>


## <span data-ttu-id="71140-107">예제의</span><span class="sxs-lookup"><span data-stu-id="71140-107">EXAMPLES</span></span>

### <span data-ttu-id="71140-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="71140-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9

```

<span data-ttu-id="71140-109">지정한 구독을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="71140-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="71140-110">변수</span><span class="sxs-lookup"><span data-stu-id="71140-110">PARAMETERS</span></span>

### <span data-ttu-id="71140-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71140-111">-DefaultProfile</span></span>


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

### <span data-ttu-id="71140-112">-Force</span><span class="sxs-lookup"><span data-stu-id="71140-112">-Force</span></span>


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

### <span data-ttu-id="71140-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71140-113">-InputObject</span></span>
<span data-ttu-id="71140-114">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71140-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="71140-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71140-115">-PassThru</span></span>


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

### <span data-ttu-id="71140-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71140-116">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="71140-117">-확인</span><span class="sxs-lookup"><span data-stu-id="71140-117">-Confirm</span></span>
<span data-ttu-id="71140-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="71140-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71140-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71140-119">-WhatIf</span></span>
<span data-ttu-id="71140-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="71140-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71140-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71140-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71140-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71140-122">CommonParameters</span></span>
<span data-ttu-id="71140-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="71140-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71140-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="71140-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71140-125">입력</span><span class="sxs-lookup"><span data-stu-id="71140-125">INPUTS</span></span>

### <span data-ttu-id="71140-126">Microsoft. i d. PowerShell. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="71140-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="71140-127">출력</span><span class="sxs-lookup"><span data-stu-id="71140-127">OUTPUTS</span></span>

### <span data-ttu-id="71140-128">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="71140-128">System.Boolean</span></span>



## <span data-ttu-id="71140-129">상속자</span><span class="sxs-lookup"><span data-stu-id="71140-129">NOTES</span></span>

<span data-ttu-id="71140-130">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="71140-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="71140-131">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="71140-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="71140-132">INPUTOBJECT <ISubscriptionIdentity> :</span><span class="sxs-lookup"><span data-stu-id="71140-132">INPUTOBJECT <ISubscriptionIdentity>:</span></span> 
  - <span data-ttu-id="71140-133">`[DelegatedProviderId <String>]`: 위임 된 공급자의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="71140-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="71140-134">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="71140-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="71140-135">`[OfferName <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71140-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="71140-136">`[SubscriptionId <String>]`: 구독의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="71140-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="71140-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71140-137">RELATED LINKS</span></span>


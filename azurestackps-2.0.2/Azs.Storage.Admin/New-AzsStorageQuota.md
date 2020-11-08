---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/new-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: bd97eff2a0ed37c309ad0b50927f8231a2da27a6
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046597"
---
# <span data-ttu-id="b3610-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="b3610-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="b3610-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3610-102">SYNOPSIS</span></span>


## <span data-ttu-id="b3610-103">구문과</span><span class="sxs-lookup"><span data-stu-id="b3610-103">SYNTAX</span></span>

### <span data-ttu-id="b3610-104">CreateExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="b3610-104">CreateExpanded (Default)</span></span>
```
New-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b3610-105">만드는</span><span class="sxs-lookup"><span data-stu-id="b3610-105">Create</span></span>
```
New-AzsStorageQuota -Name <String> -QuotaObject <IStorageQuota> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b3610-106">설명은</span><span class="sxs-lookup"><span data-stu-id="b3610-106">DESCRIPTION</span></span>


## <span data-ttu-id="b3610-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b3610-107">EXAMPLES</span></span>

### <span data-ttu-id="b3610-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="b3610-108">Example 1:</span></span>
```powershell
PS C:\> New-AzsStorageQuota -Name TestQuota -CapacityInGb 123 -NumberOfStorageAccounts 456
```

<span data-ttu-id="b3610-109">지정 된 값을 사용 하 여 새 저장소 할당량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b3610-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="b3610-110">변수</span><span class="sxs-lookup"><span data-stu-id="b3610-110">PARAMETERS</span></span>

### <span data-ttu-id="b3610-111">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="b3610-111">-CapacityInGb</span></span>


```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b3610-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3610-112">-DefaultProfile</span></span>


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

### <span data-ttu-id="b3610-113">-위치</span><span class="sxs-lookup"><span data-stu-id="b3610-113">-Location</span></span>


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

### <span data-ttu-id="b3610-114">-이름</span><span class="sxs-lookup"><span data-stu-id="b3610-114">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b3610-115">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="b3610-115">-NumberOfStorageAccounts</span></span>


```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b3610-116">-QuotaObject</span><span class="sxs-lookup"><span data-stu-id="b3610-116">-QuotaObject</span></span>
<span data-ttu-id="b3610-117">생성 하려면 QUOTAOBJECT 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b3610-117">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b3610-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3610-118">-SubscriptionId</span></span>


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

### <span data-ttu-id="b3610-119">-확인</span><span class="sxs-lookup"><span data-stu-id="b3610-119">-Confirm</span></span>
<span data-ttu-id="b3610-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3610-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3610-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3610-121">-WhatIf</span></span>
<span data-ttu-id="b3610-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b3610-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3610-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3610-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3610-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3610-124">CommonParameters</span></span>
<span data-ttu-id="b3610-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3610-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3610-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b3610-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3610-127">입력</span><span class="sxs-lookup"><span data-stu-id="b3610-127">INPUTS</span></span>

### <span data-ttu-id="b3610-128">Api201908Preview. IStorageQuota에 대 한 관리자.</span><span class="sxs-lookup"><span data-stu-id="b3610-128">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="b3610-129">출력</span><span class="sxs-lookup"><span data-stu-id="b3610-129">OUTPUTS</span></span>

### <span data-ttu-id="b3610-130">Api201908Preview. IStorageQuota에 대 한 관리자.</span><span class="sxs-lookup"><span data-stu-id="b3610-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="b3610-131">상속자</span><span class="sxs-lookup"><span data-stu-id="b3610-131">NOTES</span></span>

<span data-ttu-id="b3610-132">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3610-132">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b3610-133">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="b3610-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b3610-134">QUOTAOBJECT <IStorageQuota> :</span><span class="sxs-lookup"><span data-stu-id="b3610-134">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="b3610-135">`[CapacityInGb <Int32?>]`: 최대 용량 (GB).</span><span class="sxs-lookup"><span data-stu-id="b3610-135">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="b3610-136">`[NumberOfStorageAccounts <Int32?>]`: 총 저장소 계정 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b3610-136">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="b3610-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3610-137">RELATED LINKS</span></span>


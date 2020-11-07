---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: b89bef906cf54378719c7c6b83dcaff484ced282
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876013"
---
# <span data-ttu-id="8587e-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="8587e-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="8587e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8587e-102">SYNOPSIS</span></span>


## <span data-ttu-id="8587e-103">구문과</span><span class="sxs-lookup"><span data-stu-id="8587e-103">SYNTAX</span></span>

### <span data-ttu-id="8587e-104">Name (기본값)</span><span class="sxs-lookup"><span data-stu-id="8587e-104">Name (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8587e-105">QuotaObject</span><span class="sxs-lookup"><span data-stu-id="8587e-105">QuotaObject</span></span>
```
Set-AzsStorageQuota -QuotaObject <IStorageQuota> [-Location <String>] [-SubscriptionId <String>]
 [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8587e-106">설명은</span><span class="sxs-lookup"><span data-stu-id="8587e-106">DESCRIPTION</span></span>


## <span data-ttu-id="8587e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8587e-107">EXAMPLES</span></span>

### <span data-ttu-id="8587e-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="8587e-108">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -NumberOfStorageAccounts 11 -CapacityInGb 22
```

<span data-ttu-id="8587e-109">이름으로 기존 저장소 할당량을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8587e-109">Update an existing storage quota by name.</span></span>

### <span data-ttu-id="8587e-110">예제 2:</span><span class="sxs-lookup"><span data-stu-id="8587e-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestUpdateStorageQuota' | Set-AzsStorageQuota -NumberOfStorageAccounts 22 -CapacityInGb 33
```

<span data-ttu-id="8587e-111">파이프를 기준으로 기존 저장소 할당량을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8587e-111">Update an existing storage quota by piping.</span></span>

## <span data-ttu-id="8587e-112">변수</span><span class="sxs-lookup"><span data-stu-id="8587e-112">PARAMETERS</span></span>

### <span data-ttu-id="8587e-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="8587e-113">-CapacityInGb</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8587e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8587e-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="8587e-115">-위치</span><span class="sxs-lookup"><span data-stu-id="8587e-115">-Location</span></span>


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

### <span data-ttu-id="8587e-116">-이름</span><span class="sxs-lookup"><span data-stu-id="8587e-116">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Name
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8587e-117">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="8587e-117">-NumberOfStorageAccounts</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8587e-118">-QuotaObject</span><span class="sxs-lookup"><span data-stu-id="8587e-118">-QuotaObject</span></span>
<span data-ttu-id="8587e-119">생성 하려면 QUOTAOBJECT 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8587e-119">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota
Parameter Sets: QuotaObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8587e-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8587e-120">-SubscriptionId</span></span>


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

### <span data-ttu-id="8587e-121">-확인</span><span class="sxs-lookup"><span data-stu-id="8587e-121">-Confirm</span></span>
<span data-ttu-id="8587e-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8587e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8587e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8587e-123">-WhatIf</span></span>
<span data-ttu-id="8587e-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8587e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8587e-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8587e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8587e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8587e-126">CommonParameters</span></span>
<span data-ttu-id="8587e-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8587e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8587e-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8587e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8587e-129">입력</span><span class="sxs-lookup"><span data-stu-id="8587e-129">INPUTS</span></span>

### <span data-ttu-id="8587e-130">Api201908Preview. IStorageQuota에 대 한 관리자.</span><span class="sxs-lookup"><span data-stu-id="8587e-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="8587e-131">출력</span><span class="sxs-lookup"><span data-stu-id="8587e-131">OUTPUTS</span></span>

### <span data-ttu-id="8587e-132">Api201908Preview. IStorageQuota에 대 한 관리자.</span><span class="sxs-lookup"><span data-stu-id="8587e-132">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="8587e-133">상속자</span><span class="sxs-lookup"><span data-stu-id="8587e-133">NOTES</span></span>

<span data-ttu-id="8587e-134">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8587e-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8587e-135">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="8587e-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8587e-136">QUOTAOBJECT <IStorageQuota> :</span><span class="sxs-lookup"><span data-stu-id="8587e-136">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="8587e-137">`[CapacityInGb <Int32?>]`: 최대 용량 (GB).</span><span class="sxs-lookup"><span data-stu-id="8587e-137">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="8587e-138">`[NumberOfStorageAccounts <Int32?>]`: 총 저장소 계정 수입니다.</span><span class="sxs-lookup"><span data-stu-id="8587e-138">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="8587e-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8587e-139">RELATED LINKS</span></span>


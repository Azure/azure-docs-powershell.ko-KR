---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
ms.openlocfilehash: 9cb677ff172c986f18c7c11c00e0f8d7e0bbf5bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225981"
---
# <span data-ttu-id="22ca7-101">Test-AzVMWareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="22ca7-101">Test-AzVMWareLocationQuotaAvailability</span></span>

## <span data-ttu-id="22ca7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22ca7-102">SYNOPSIS</span></span>
<span data-ttu-id="22ca7-103">지역별 구독에 대 한 할당량 반환</span><span class="sxs-lookup"><span data-stu-id="22ca7-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="22ca7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22ca7-104">SYNTAX</span></span>

### <span data-ttu-id="22ca7-105">선택 (기본값)</span><span class="sxs-lookup"><span data-stu-id="22ca7-105">Check (Default)</span></span>
```
Test-AzVMWareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="22ca7-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="22ca7-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationQuotaAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="22ca7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="22ca7-107">DESCRIPTION</span></span>
<span data-ttu-id="22ca7-108">지역별 구독에 대 한 할당량 반환</span><span class="sxs-lookup"><span data-stu-id="22ca7-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="22ca7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="22ca7-109">EXAMPLES</span></span>

### <span data-ttu-id="22ca7-110">예제 1: 할당량 사용 가능 여부 확인</span><span class="sxs-lookup"><span data-stu-id="22ca7-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="22ca7-111">할당량 사용 가능 여부 확인</span><span class="sxs-lookup"><span data-stu-id="22ca7-111">Check quota availability</span></span>

## <span data-ttu-id="22ca7-112">변수</span><span class="sxs-lookup"><span data-stu-id="22ca7-112">PARAMETERS</span></span>

### <span data-ttu-id="22ca7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ca7-113">-DefaultProfile</span></span>
<span data-ttu-id="22ca7-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="22ca7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22ca7-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22ca7-115">-InputObject</span></span>
<span data-ttu-id="22ca7-116">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22ca7-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22ca7-117">-위치</span><span class="sxs-lookup"><span data-stu-id="22ca7-117">-Location</span></span>
<span data-ttu-id="22ca7-118">Azure 지역</span><span class="sxs-lookup"><span data-stu-id="22ca7-118">Azure region</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ca7-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="22ca7-119">-SubscriptionId</span></span>
<span data-ttu-id="22ca7-120">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="22ca7-120">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ca7-121">-확인</span><span class="sxs-lookup"><span data-stu-id="22ca7-121">-Confirm</span></span>
<span data-ttu-id="22ca7-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="22ca7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22ca7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22ca7-123">-WhatIf</span></span>
<span data-ttu-id="22ca7-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="22ca7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22ca7-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22ca7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22ca7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ca7-126">CommonParameters</span></span>
<span data-ttu-id="22ca7-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22ca7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ca7-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="22ca7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ca7-129">입력</span><span class="sxs-lookup"><span data-stu-id="22ca7-129">INPUTS</span></span>

### <span data-ttu-id="22ca7-130">IVMWareIdentity (Microsoft. v.</span><span class="sxs-lookup"><span data-stu-id="22ca7-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="22ca7-131">출력</span><span class="sxs-lookup"><span data-stu-id="22ca7-131">OUTPUTS</span></span>

### <span data-ttu-id="22ca7-132">Api20200320 (Microsoft. v r a. i r a r.</span><span class="sxs-lookup"><span data-stu-id="22ca7-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="22ca7-133">상속자</span><span class="sxs-lookup"><span data-stu-id="22ca7-133">NOTES</span></span>

<span data-ttu-id="22ca7-134">별칭과</span><span class="sxs-lookup"><span data-stu-id="22ca7-134">ALIASES</span></span>

<span data-ttu-id="22ca7-135">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="22ca7-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="22ca7-136">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="22ca7-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="22ca7-137">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="22ca7-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="22ca7-138">INPUTOBJECT <IVMWareIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="22ca7-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="22ca7-139">`[AuthorizationName <String>]`: 사설 클라우드의 Express 경로 권한 부여 이름</span><span class="sxs-lookup"><span data-stu-id="22ca7-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="22ca7-140">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="22ca7-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="22ca7-141">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise 사이트의 이름</span><span class="sxs-lookup"><span data-stu-id="22ca7-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="22ca7-142">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="22ca7-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="22ca7-143">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="22ca7-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="22ca7-144">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="22ca7-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="22ca7-145">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22ca7-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="22ca7-146">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="22ca7-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="22ca7-147">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="22ca7-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="22ca7-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22ca7-148">RELATED LINKS</span></span>


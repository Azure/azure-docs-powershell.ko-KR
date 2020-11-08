---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: e9fbcb04841c08fe396cc56d92acd0abdaf94089
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045213"
---
# <span data-ttu-id="549d2-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="549d2-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="549d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="549d2-102">SYNOPSIS</span></span>
<span data-ttu-id="549d2-103">이름으로 할당량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="549d2-103">Get a quota by name.</span></span>

## <span data-ttu-id="549d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="549d2-104">SYNTAX</span></span>

### <span data-ttu-id="549d2-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="549d2-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="549d2-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="549d2-106">Get</span></span>
```
Get-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="549d2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="549d2-107">GetViaIdentity</span></span>
```
Get-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="549d2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="549d2-108">DESCRIPTION</span></span>
<span data-ttu-id="549d2-109">모든 할당량을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="549d2-109">List all quotas.</span></span>
<span data-ttu-id="549d2-110">이름 또는 필터를 전달 하 여 목록을 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="549d2-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="549d2-111">예제의</span><span class="sxs-lookup"><span data-stu-id="549d2-111">EXAMPLES</span></span>

### <span data-ttu-id="549d2-112">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="549d2-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="549d2-113">모든 네트워크 할당량을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="549d2-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="549d2-114">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="549d2-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="549d2-115">지정 된 네트워크 할당량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="549d2-115">Gets the specified network quota.</span></span>



## <span data-ttu-id="549d2-116">변수</span><span class="sxs-lookup"><span data-stu-id="549d2-116">PARAMETERS</span></span>

### <span data-ttu-id="549d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="549d2-117">-DefaultProfile</span></span>
<span data-ttu-id="549d2-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="549d2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="549d2-119">-필터</span><span class="sxs-lookup"><span data-stu-id="549d2-119">-Filter</span></span>
<span data-ttu-id="549d2-120">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="549d2-120">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="549d2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="549d2-121">-InputObject</span></span>
<span data-ttu-id="549d2-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="549d2-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="549d2-123">-위치</span><span class="sxs-lookup"><span data-stu-id="549d2-123">-Location</span></span>
<span data-ttu-id="549d2-124">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="549d2-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="549d2-125">-이름</span><span class="sxs-lookup"><span data-stu-id="549d2-125">-Name</span></span>
<span data-ttu-id="549d2-126">리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="549d2-126">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="549d2-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="549d2-127">-PassThru</span></span>
<span data-ttu-id="549d2-128">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="549d2-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="549d2-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="549d2-129">-SubscriptionId</span></span>
<span data-ttu-id="549d2-130">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="549d2-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="549d2-131">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="549d2-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="549d2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="549d2-132">CommonParameters</span></span>
<span data-ttu-id="549d2-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="549d2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="549d2-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="549d2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="549d2-135">입력</span><span class="sxs-lookup"><span data-stu-id="549d2-135">INPUTS</span></span>

### <span data-ttu-id="549d2-136">INetworkAdminIdentity (Microsoft. PowerShell. 관리자.</span><span class="sxs-lookup"><span data-stu-id="549d2-136">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="549d2-137">출력</span><span class="sxs-lookup"><span data-stu-id="549d2-137">OUTPUTS</span></span>

### <span data-ttu-id="549d2-138">Api20150615 (Microsoft. PowerShell. i N.exe 할당량</span><span class="sxs-lookup"><span data-stu-id="549d2-138">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="549d2-139">상속자</span><span class="sxs-lookup"><span data-stu-id="549d2-139">NOTES</span></span>

<span data-ttu-id="549d2-140">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="549d2-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="549d2-141">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="549d2-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="549d2-142">INPUTOBJECT <INetworkAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="549d2-142">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="549d2-143">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="549d2-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="549d2-144">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="549d2-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="549d2-145">`[ResourceName <String>]`: 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="549d2-145">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="549d2-146">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="549d2-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="549d2-147">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="549d2-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="549d2-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="549d2-148">RELATED LINKS</span></span>


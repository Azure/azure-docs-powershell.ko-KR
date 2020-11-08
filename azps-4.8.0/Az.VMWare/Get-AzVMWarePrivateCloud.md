---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
ms.openlocfilehash: 31400d3b9b6e57190a852ae579fffcaa9fc60401
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213439"
---
# <span data-ttu-id="8c266-101">Get-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="8c266-101">Get-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="8c266-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c266-102">SYNOPSIS</span></span>
<span data-ttu-id="8c266-103">사설 클라우드 받기</span><span class="sxs-lookup"><span data-stu-id="8c266-103">Get a private cloud</span></span>

## <span data-ttu-id="8c266-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8c266-104">SYNTAX</span></span>

### <span data-ttu-id="8c266-105">List1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8c266-105">List1 (Default)</span></span>
```
Get-AzVMWarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8c266-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="8c266-106">Get</span></span>
```
Get-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8c266-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8c266-107">GetViaIdentity</span></span>
```
Get-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8c266-108">목록</span><span class="sxs-lookup"><span data-stu-id="8c266-108">List</span></span>
```
Get-AzVMWarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c266-109">설명은</span><span class="sxs-lookup"><span data-stu-id="8c266-109">DESCRIPTION</span></span>
<span data-ttu-id="8c266-110">사설 클라우드 받기</span><span class="sxs-lookup"><span data-stu-id="8c266-110">Get a private cloud</span></span>

## <span data-ttu-id="8c266-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8c266-111">EXAMPLES</span></span>

### <span data-ttu-id="8c266-112">예제 1: 구독에 사설 클라우드 나열</span><span class="sxs-lookup"><span data-stu-id="8c266-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="8c266-113">구독에 사설 클라우드 나열</span><span class="sxs-lookup"><span data-stu-id="8c266-113">List private cloud under subscription</span></span>

### <span data-ttu-id="8c266-114">예제 2: 리소스 그룹 아래에 개인 클라우드 나열</span><span class="sxs-lookup"><span data-stu-id="8c266-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="8c266-115">리소스 그룹 아래에 개인 클라우드 나열</span><span class="sxs-lookup"><span data-stu-id="8c266-115">List private cloud under resource group</span></span>

### <span data-ttu-id="8c266-116">예제 3: 사설 클라우드 가져오기</span><span class="sxs-lookup"><span data-stu-id="8c266-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="8c266-117">사설 클라우드 가져오기</span><span class="sxs-lookup"><span data-stu-id="8c266-117">Get private cloud</span></span>

## <span data-ttu-id="8c266-118">변수</span><span class="sxs-lookup"><span data-stu-id="8c266-118">PARAMETERS</span></span>

### <span data-ttu-id="8c266-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c266-119">-DefaultProfile</span></span>
<span data-ttu-id="8c266-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8c266-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c266-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c266-121">-InputObject</span></span>
<span data-ttu-id="8c266-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8c266-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c266-123">-이름</span><span class="sxs-lookup"><span data-stu-id="8c266-123">-Name</span></span>
<span data-ttu-id="8c266-124">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="8c266-124">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c266-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c266-125">-ResourceGroupName</span></span>
<span data-ttu-id="8c266-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8c266-126">The name of the resource group.</span></span>
<span data-ttu-id="8c266-127">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c266-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c266-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c266-128">-SubscriptionId</span></span>
<span data-ttu-id="8c266-129">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8c266-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c266-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c266-130">CommonParameters</span></span>
<span data-ttu-id="8c266-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c266-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c266-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8c266-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c266-133">입력</span><span class="sxs-lookup"><span data-stu-id="8c266-133">INPUTS</span></span>

### <span data-ttu-id="8c266-134">IVMWareIdentity (Microsoft. v.</span><span class="sxs-lookup"><span data-stu-id="8c266-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="8c266-135">출력</span><span class="sxs-lookup"><span data-stu-id="8c266-135">OUTPUTS</span></span>

### <span data-ttu-id="8c266-136">Api20200320. IPrivateCloud에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8c266-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="8c266-137">상속자</span><span class="sxs-lookup"><span data-stu-id="8c266-137">NOTES</span></span>

<span data-ttu-id="8c266-138">별칭과</span><span class="sxs-lookup"><span data-stu-id="8c266-138">ALIASES</span></span>

<span data-ttu-id="8c266-139">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="8c266-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8c266-140">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c266-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8c266-141">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="8c266-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8c266-142">INPUTOBJECT <IVMWareIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8c266-142">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8c266-143">`[AuthorizationName <String>]`: 사설 클라우드의 Express 경로 권한 부여 이름</span><span class="sxs-lookup"><span data-stu-id="8c266-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="8c266-144">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="8c266-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="8c266-145">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise 사이트의 이름</span><span class="sxs-lookup"><span data-stu-id="8c266-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="8c266-146">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="8c266-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8c266-147">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="8c266-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="8c266-148">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="8c266-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="8c266-149">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8c266-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8c266-150">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c266-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="8c266-151">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8c266-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="8c266-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c266-152">RELATED LINKS</span></span>


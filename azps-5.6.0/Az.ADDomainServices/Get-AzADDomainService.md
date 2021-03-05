---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/get-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
ms.openlocfilehash: 19ae45bf50c9ae54075e46a8db8fc66cc08e488a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997038"
---
# <span data-ttu-id="67efa-101">Get-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="67efa-101">Get-AzADDomainService</span></span>

## <span data-ttu-id="67efa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67efa-102">SYNOPSIS</span></span>
<span data-ttu-id="67efa-103">도메인 서비스 Get 작업은 도메인 서비스의 json 표현을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="67efa-103">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="67efa-104">구문</span><span class="sxs-lookup"><span data-stu-id="67efa-104">SYNTAX</span></span>

### <span data-ttu-id="67efa-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="67efa-105">List (Default)</span></span>
```
Get-AzADDomainService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="67efa-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="67efa-106">Get</span></span>
```
Get-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="67efa-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="67efa-107">GetViaIdentity</span></span>
```
Get-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="67efa-108">List1</span><span class="sxs-lookup"><span data-stu-id="67efa-108">List1</span></span>
```
Get-AzADDomainService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="67efa-109">설명</span><span class="sxs-lookup"><span data-stu-id="67efa-109">DESCRIPTION</span></span>
<span data-ttu-id="67efa-110">도메인 서비스 Get 작업은 도메인 서비스의 json 표현을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="67efa-110">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="67efa-111">예제</span><span class="sxs-lookup"><span data-stu-id="67efa-111">EXAMPLES</span></span>

### <span data-ttu-id="67efa-112">예제 1: 기본적으로 모든 ADDomainService를 얻다</span><span class="sxs-lookup"><span data-stu-id="67efa-112">Example 1: Get All ADDomainService By default</span></span>
```powershell
PS C:\> Get-AzADDomainService

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="67efa-113">기본적으로 모든 ADDomainService를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="67efa-113">Get All ADDomainService By default</span></span>

### <span data-ttu-id="67efa-114">예제 2: ResourceGroup 및 이름에 따라 ADDomainService를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="67efa-114">Example 2: Get ADDomainService By ResourceGroup and name</span></span>
```powershell
PS C:\> Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="67efa-115">ResourceGroup 및 이름에 따라 ADDomainService를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="67efa-115">Get ADDomainService By ResourceGroup and name</span></span>

### <span data-ttu-id="67efa-116">예제 3: 모든 ADDomainService By ResourceGroup 사용</span><span class="sxs-lookup"><span data-stu-id="67efa-116">Example 3: Get all ADDomainService By ResourceGroup</span></span>
```powershell
PS C:\> Get-AzADDomainService -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="67efa-117">리소스 그룹으로 모든 ADDomainService를 얻다</span><span class="sxs-lookup"><span data-stu-id="67efa-117">Get all ADDomainService By ResourceGroup</span></span>

### <span data-ttu-id="67efa-118">예제 4: InputObject로 ADDomainService를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67efa-118">Example 4: Get ADDomainService By InputObject</span></span>
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
Get-AzADDomainService -InputObject $getAzAddomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="67efa-119">InputObject로 ADDomainService를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67efa-119">Get ADDomainService By InputObject</span></span>

## <span data-ttu-id="67efa-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="67efa-120">PARAMETERS</span></span>

### <span data-ttu-id="67efa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67efa-121">-DefaultProfile</span></span>
<span data-ttu-id="67efa-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67efa-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67efa-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67efa-123">-InputObject</span></span>
<span data-ttu-id="67efa-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="67efa-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67efa-125">-Name</span><span class="sxs-lookup"><span data-stu-id="67efa-125">-Name</span></span>
<span data-ttu-id="67efa-126">도메인 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67efa-126">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67efa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67efa-127">-ResourceGroupName</span></span>
<span data-ttu-id="67efa-128">사용자의 구독 내의 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67efa-128">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="67efa-129">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="67efa-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67efa-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67efa-130">-SubscriptionId</span></span>
<span data-ttu-id="67efa-131">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67efa-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="67efa-132">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="67efa-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="67efa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67efa-133">CommonParameters</span></span>
<span data-ttu-id="67efa-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="67efa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67efa-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67efa-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67efa-136">입력</span><span class="sxs-lookup"><span data-stu-id="67efa-136">INPUTS</span></span>

### <span data-ttu-id="67efa-137">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="67efa-137">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="67efa-138">출력</span><span class="sxs-lookup"><span data-stu-id="67efa-138">OUTPUTS</span></span>

### <span data-ttu-id="67efa-139">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="67efa-139">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="67efa-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="67efa-140">NOTES</span></span>

<span data-ttu-id="67efa-141">별칭</span><span class="sxs-lookup"><span data-stu-id="67efa-141">ALIASES</span></span>

<span data-ttu-id="67efa-142">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="67efa-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="67efa-143">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="67efa-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="67efa-144">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="67efa-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="67efa-145">INPUTOBJECT <IAdDomainServicesIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="67efa-145">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="67efa-146">`[DomainServiceName <String>]`: 도메인 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67efa-146">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="67efa-147">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="67efa-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="67efa-148">`[ResourceGroupName <String>]`: 사용자의 구독 내의 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67efa-148">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="67efa-149">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="67efa-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="67efa-150">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67efa-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="67efa-151">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="67efa-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="67efa-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67efa-152">RELATED LINKS</span></span>


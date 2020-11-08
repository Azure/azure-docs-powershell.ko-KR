---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
schema: 2.0.0
ms.openlocfilehash: 8559b8cdde324c3927ac835f49291441a4e58847
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045214"
---
# <span data-ttu-id="fb6fe-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="fb6fe-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="fb6fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb6fe-102">SYNOPSIS</span></span>
<span data-ttu-id="fb6fe-103">네트워크 리소스 공급자의 상태에 대 한 개요를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="fb6fe-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="fb6fe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fb6fe-104">SYNTAX</span></span>

### <span data-ttu-id="fb6fe-105">Get (기본값)</span><span class="sxs-lookup"><span data-stu-id="fb6fe-105">Get (Default)</span></span>
```
Get-AzsNetworkAdminOverview [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fb6fe-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fb6fe-106">GetViaIdentity</span></span>
```
Get-AzsNetworkAdminOverview -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb6fe-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fb6fe-107">DESCRIPTION</span></span>
<span data-ttu-id="fb6fe-108">네트워크 리소스 공급자의 상태에 대 한 개요를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="fb6fe-108">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="fb6fe-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fb6fe-109">EXAMPLES</span></span>

### <span data-ttu-id="fb6fe-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fb6fe-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsNetworkAdminOverview
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
```



## <span data-ttu-id="fb6fe-111">변수</span><span class="sxs-lookup"><span data-stu-id="fb6fe-111">PARAMETERS</span></span>

### <span data-ttu-id="fb6fe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb6fe-112">-DefaultProfile</span></span>
<span data-ttu-id="fb6fe-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6fe-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb6fe-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb6fe-114">-InputObject</span></span>
<span data-ttu-id="fb6fe-115">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb6fe-115">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fb6fe-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fb6fe-116">-SubscriptionId</span></span>
<span data-ttu-id="fb6fe-117">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6fe-117">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fb6fe-118">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6fe-118">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fb6fe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb6fe-119">CommonParameters</span></span>
<span data-ttu-id="fb6fe-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6fe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb6fe-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fb6fe-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb6fe-122">입력</span><span class="sxs-lookup"><span data-stu-id="fb6fe-122">INPUTS</span></span>

### <span data-ttu-id="fb6fe-123">INetworkAdminIdentity (Microsoft. PowerShell. 관리자.</span><span class="sxs-lookup"><span data-stu-id="fb6fe-123">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="fb6fe-124">출력</span><span class="sxs-lookup"><span data-stu-id="fb6fe-124">OUTPUTS</span></span>

### <span data-ttu-id="fb6fe-125">Api20150615. a PowerShell. i i m. 관리자. IAdminOverview</span><span class="sxs-lookup"><span data-stu-id="fb6fe-125">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IAdminOverview</span></span>



## <span data-ttu-id="fb6fe-126">상속자</span><span class="sxs-lookup"><span data-stu-id="fb6fe-126">NOTES</span></span>

<span data-ttu-id="fb6fe-127">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6fe-127">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fb6fe-128">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="fb6fe-128">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="fb6fe-129">INPUTOBJECT <INetworkAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="fb6fe-129">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fb6fe-130">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="fb6fe-130">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fb6fe-131">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6fe-131">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="fb6fe-132">`[ResourceName <String>]`: 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6fe-132">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="fb6fe-133">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6fe-133">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="fb6fe-134">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6fe-134">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="fb6fe-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb6fe-135">RELATED LINKS</span></span>


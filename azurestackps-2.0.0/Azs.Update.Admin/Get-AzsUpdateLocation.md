---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdatelocation
schema: 2.0.0
ms.openlocfilehash: 0aa8e2358a5af4a5f73339a1068b0668914eef6e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875239"
---
# <span data-ttu-id="5cab0-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="5cab0-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="5cab0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cab0-102">SYNOPSIS</span></span>
<span data-ttu-id="5cab0-103">이름에 따라 업데이트 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5cab0-103">Get an update location based on name.</span></span>

## <span data-ttu-id="5cab0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5cab0-104">SYNTAX</span></span>

### <span data-ttu-id="5cab0-105">Get (기본값)</span><span class="sxs-lookup"><span data-stu-id="5cab0-105">Get (Default)</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5cab0-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5cab0-106">GetViaIdentity</span></span>
```
Get-AzsUpdateLocation -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5cab0-107">목록</span><span class="sxs-lookup"><span data-stu-id="5cab0-107">List</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5cab0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5cab0-108">DESCRIPTION</span></span>
<span data-ttu-id="5cab0-109">이름에 따라 업데이트 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5cab0-109">Get an update location based on name.</span></span>

## <span data-ttu-id="5cab0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5cab0-110">EXAMPLES</span></span>

### <span data-ttu-id="5cab0-111">예제 1: 모든 업데이트 위치 가져오기</span><span class="sxs-lookup"><span data-stu-id="5cab0-111">Example 1: Get All Updates Locations</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="5cab0-112">매개 변수 없이이는 모든 업데이트 위치를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cab0-112">Without any parameters, this commandlet will retrieve all update locations</span></span>

### <span data-ttu-id="5cab0-113">예제 2: 이름으로 모든 업데이트 위치 가져오기</span><span class="sxs-lookup"><span data-stu-id="5cab0-113">Example 2: Get All Updates Locations by Name</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation -Name northwest

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="5cab0-114">지정 된 이름 매개 변수와 일치 하는 모든 업데이트 위치를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cab0-114">Will retrieve all update locations that matches the specified Name parameter</span></span>

## <span data-ttu-id="5cab0-115">변수</span><span class="sxs-lookup"><span data-stu-id="5cab0-115">PARAMETERS</span></span>

### <span data-ttu-id="5cab0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cab0-116">-DefaultProfile</span></span>
<span data-ttu-id="5cab0-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5cab0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cab0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cab0-118">-InputObject</span></span>
<span data-ttu-id="5cab0-119">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5cab0-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5cab0-120">-이름</span><span class="sxs-lookup"><span data-stu-id="5cab0-120">-Name</span></span>
<span data-ttu-id="5cab0-121">업데이트 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cab0-121">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5cab0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cab0-122">-ResourceGroupName</span></span>
<span data-ttu-id="5cab0-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cab0-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5cab0-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5cab0-124">-SubscriptionId</span></span>
<span data-ttu-id="5cab0-125">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="5cab0-125">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5cab0-126">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cab0-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5cab0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cab0-127">CommonParameters</span></span>
<span data-ttu-id="5cab0-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cab0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cab0-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5cab0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cab0-130">입력</span><span class="sxs-lookup"><span data-stu-id="5cab0-130">INPUTS</span></span>

### <span data-ttu-id="5cab0-131">Microsoft. i d. PowerShell. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="5cab0-131">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="5cab0-132">출력</span><span class="sxs-lookup"><span data-stu-id="5cab0-132">OUTPUTS</span></span>

### <span data-ttu-id="5cab0-133">Api20160501. PowerShell. i i m. i a 365 위치</span><span class="sxs-lookup"><span data-stu-id="5cab0-133">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateLocation</span></span>



## <span data-ttu-id="5cab0-134">상속자</span><span class="sxs-lookup"><span data-stu-id="5cab0-134">NOTES</span></span>

<span data-ttu-id="5cab0-135">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cab0-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5cab0-136">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="5cab0-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5cab0-137">INPUTOBJECT <IUpdateAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5cab0-137">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5cab0-138">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="5cab0-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5cab0-139">`[ResourceGroupName <String>]`: 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cab0-139">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="5cab0-140">`[RunName <String>]`: 업데이트 실행 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5cab0-140">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="5cab0-141">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="5cab0-141">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="5cab0-142">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cab0-142">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5cab0-143">`[UpdateLocation <String>]`: 업데이트 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cab0-143">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="5cab0-144">`[UpdateName <String>]`: 업데이트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cab0-144">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="5cab0-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5cab0-145">RELATED LINKS</span></span>


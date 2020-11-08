---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdate
schema: 2.0.0
ms.openlocfilehash: d4acc60a0f5b9acc15efd66187c09ec3acb6cb62
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046609"
---
# <span data-ttu-id="b6f73-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="b6f73-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="b6f73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6f73-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f73-103">업데이트 위치에서 특정 업데이트를 받으세요.</span><span class="sxs-lookup"><span data-stu-id="b6f73-103">Get a specific update at an update location.</span></span>

## <span data-ttu-id="b6f73-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b6f73-104">SYNTAX</span></span>

### <span data-ttu-id="b6f73-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b6f73-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b6f73-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="b6f73-106">Get</span></span>
```
Get-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b6f73-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b6f73-107">GetViaIdentity</span></span>
```
Get-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b6f73-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b6f73-108">DESCRIPTION</span></span>
<span data-ttu-id="b6f73-109">업데이트 위치에서 특정 업데이트를 받으세요.</span><span class="sxs-lookup"><span data-stu-id="b6f73-109">Get a specific update at an update location.</span></span>

## <span data-ttu-id="b6f73-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b6f73-110">EXAMPLES</span></span>

### <span data-ttu-id="b6f73-111">예제 1: 모든 업데이트 가져오기</span><span class="sxs-lookup"><span data-stu-id="b6f73-111">Example 1: Get All Updates</span></span>
```powershell
PS C:\> Get-AzsUpdate

Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
northwest       AzS Update - 1.1907.0.13       northwest/Microsoft1.1907.0.13           Installed            Microsoft
northwest       AzS Update - 1.1907.0.20       northwest/Microsoft1.1907.0.20           Installed            Microsoft
```

<span data-ttu-id="b6f73-112">매개 변수를 사용 하지 않으면 스탬프에서 검색할 수 있는 모든 업데이트가 나열 Get-AzsUpdate 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6f73-112">Without any parameters, Get-AzsUpdate will list all updates that the stamp can discover</span></span>

### <span data-ttu-id="b6f73-113">예제 2: 이름으로 업데이트 가져오기</span><span class="sxs-lookup"><span data-stu-id="b6f73-113">Example 2: Get Update by Name</span></span>
```powershell
PS C:\> Get-AzsUpdate -Name Microsoft1.1907.0.10
or
PS C:\> Get-AzsUpdate -Name northwest/Microsoft1.1907.0.10


Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
```

<span data-ttu-id="b6f73-114">지정 된 이름에 해당 하는 모든 업데이트를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f73-114">Will retrieve all updates that correspond to the specified Name</span></span>

### <span data-ttu-id="b6f73-115">예제 3: 위치에 따라 모든 업데이트 가져오기</span><span class="sxs-lookup"><span data-stu-id="b6f73-115">Example 3: Get All Updates by Location</span></span>
```powershell
PS C:\> Get-AzsUpdate -Location northwest

Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
northwest       AzS Update - 1.1907.0.13       northwest/Microsoft1.1907.0.13           Installed            Microsoft
northwest       AzS Update - 1.1907.0.20       northwest/Microsoft1.1907.0.20           Installed            Microsoft
```

<span data-ttu-id="b6f73-116">지정 된 위치 내의 모든 업데이트를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f73-116">Will retrieve all updates within a specified Location.</span></span>
<span data-ttu-id="b6f73-117">현재는 한 위치만 지원 되므로이는 같은 것입니다 Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="b6f73-117">Currently, only one location is supported so this is the equivalent as just Get-AzsUpdate</span></span>

## <span data-ttu-id="b6f73-118">변수</span><span class="sxs-lookup"><span data-stu-id="b6f73-118">PARAMETERS</span></span>

### <span data-ttu-id="b6f73-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f73-119">-DefaultProfile</span></span>
<span data-ttu-id="b6f73-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6f73-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6f73-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6f73-121">-InputObject</span></span>
<span data-ttu-id="b6f73-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6f73-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b6f73-123">-위치</span><span class="sxs-lookup"><span data-stu-id="b6f73-123">-Location</span></span>
<span data-ttu-id="b6f73-124">업데이트 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6f73-124">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b6f73-125">-이름</span><span class="sxs-lookup"><span data-stu-id="b6f73-125">-Name</span></span>
<span data-ttu-id="b6f73-126">업데이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6f73-126">Name of the update.</span></span>

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

### <span data-ttu-id="b6f73-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6f73-127">-ResourceGroupName</span></span>
<span data-ttu-id="b6f73-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6f73-128">Resource group name.</span></span>

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

### <span data-ttu-id="b6f73-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6f73-129">-SubscriptionId</span></span>
<span data-ttu-id="b6f73-130">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="b6f73-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b6f73-131">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f73-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b6f73-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f73-132">CommonParameters</span></span>
<span data-ttu-id="b6f73-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f73-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f73-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b6f73-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f73-135">입력</span><span class="sxs-lookup"><span data-stu-id="b6f73-135">INPUTS</span></span>

### <span data-ttu-id="b6f73-136">Microsoft. i d. PowerShell. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b6f73-136">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="b6f73-137">출력</span><span class="sxs-lookup"><span data-stu-id="b6f73-137">OUTPUTS</span></span>

### <span data-ttu-id="b6f73-138">Api20160501-IUpdate (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b6f73-138">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdate</span></span>



## <span data-ttu-id="b6f73-139">상속자</span><span class="sxs-lookup"><span data-stu-id="b6f73-139">NOTES</span></span>

<span data-ttu-id="b6f73-140">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f73-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b6f73-141">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="b6f73-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b6f73-142">INPUTOBJECT <IUpdateAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b6f73-142">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b6f73-143">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="b6f73-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b6f73-144">`[ResourceGroupName <String>]`: 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6f73-144">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="b6f73-145">`[RunName <String>]`: 업데이트 실행 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b6f73-145">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="b6f73-146">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="b6f73-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="b6f73-147">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f73-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b6f73-148">`[UpdateLocation <String>]`: 업데이트 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6f73-148">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="b6f73-149">`[UpdateName <String>]`: 업데이트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6f73-149">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="b6f73-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6f73-150">RELATED LINKS</span></span>


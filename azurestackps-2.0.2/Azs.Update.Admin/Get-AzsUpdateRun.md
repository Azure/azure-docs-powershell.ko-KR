---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: fb36cb0d1be46abb66a1c0cc97165f8eb9cc3913
ms.sourcegitcommit: f7edd4f5c4bebedc139cb01438081edc6ed560bd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/29/2020
ms.locfileid: "94047349"
---
# <span data-ttu-id="d17a4-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="d17a4-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="d17a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d17a4-102">SYNOPSIS</span></span>
<span data-ttu-id="d17a4-103">ID를 사용 하 여 업데이트 실행의 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-103">Get an instance of update run using the ID.</span></span>

## <span data-ttu-id="d17a4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d17a4-104">SYNTAX</span></span>

### <span data-ttu-id="d17a4-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d17a4-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d17a4-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="d17a4-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d17a4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d17a4-107">GetViaIdentity</span></span>
```
Get-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d17a4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d17a4-108">DESCRIPTION</span></span>
<span data-ttu-id="d17a4-109">ID를 사용 하 여 업데이트 실행의 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-109">Get an instance of update run using the ID.</span></span>

## <span data-ttu-id="d17a4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d17a4-110">EXAMPLES</span></span>

### <span data-ttu-id="d17a4-111">예제 1: Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="d17a4-111">Example 1: Get-AzsUpdateRun</span></span>
```powershell
PS C:\> Get-AzsUpdateRun

cmdlet Get-AzsUpdateRun at command pipeline position 1
Supply values for the following parameters:
UpdateName: Microsoft1.1907.0.10

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
northwest/Microsoft1.1907.0.10/51e878... Succeeded       7/11/2019 3:07:10 PM      7/12/2019 6:47:37 AM
```

<span data-ttu-id="d17a4-112">UpdateName 값이 지정 되지 않은 경우 Get-UpdateRun는 항상 입력을 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-112">If a UpdateName value is not specified, Get-UpdateRun will always ask for input.</span></span>
<span data-ttu-id="d17a4-113">제공 된 후에는 실패 하거나 성공한 모든 UpdateRun의 인스턴스를 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-113">Once provided, it will output all instances of UpdateRun that were Failed or Successful</span></span>

### <span data-ttu-id="d17a4-114">예제 2: UpdateName을 기준으로 Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="d17a4-114">Example 2: Get-AzsUpdateRun By UpdateName</span></span>
```powershell
PS C:\> Get-AzsUpdateRun -UpdateName Microsoft1.1907.0.10
or 
PS C:\> Get-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
northwest/Microsoft1.1907.0.10/51e878... Succeeded       7/11/2019 3:07:10 PM      7/12/2019 6:47:37 AM
```

<span data-ttu-id="d17a4-115">특정 업데이트와 관련 된 모든 UpdateRuns 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-115">Will retrieve all UpdateRuns associated with a specific Update</span></span>

### <span data-ttu-id="d17a4-116">예제 2: 이름으로 Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="d17a4-116">Example 2: Get-AzsUpdateRun By Name</span></span>
```powershell
PS C:\> Get-AzsUpdateRun -UpdateName Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4
or 
PS C:\> Get-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name northwest/Microsoft1.1907.0.10/45aaeb26-805b-495b-9c8c-d5da5542dbf4

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
```

<span data-ttu-id="d17a4-117">특정 업데이트 및 특정 이름과 관련 된 모든 UpdateRuns 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-117">Will retrieve all UpdateRuns associated with a specific Update and a specific Name</span></span>

## <span data-ttu-id="d17a4-118">변수</span><span class="sxs-lookup"><span data-stu-id="d17a4-118">PARAMETERS</span></span>

### <span data-ttu-id="d17a4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d17a4-119">-DefaultProfile</span></span>
<span data-ttu-id="d17a4-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d17a4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d17a4-121">-InputObject</span></span>
<span data-ttu-id="d17a4-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d17a4-123">-위치</span><span class="sxs-lookup"><span data-stu-id="d17a4-123">-Location</span></span>
<span data-ttu-id="d17a4-124">업데이트 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-124">The name of the update location.</span></span>

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

### <span data-ttu-id="d17a4-125">-이름</span><span class="sxs-lookup"><span data-stu-id="d17a4-125">-Name</span></span>
<span data-ttu-id="d17a4-126">업데이트 실행 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-126">Update run identifier.</span></span>

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

### <span data-ttu-id="d17a4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d17a4-127">-ResourceGroupName</span></span>
<span data-ttu-id="d17a4-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-128">Resource group name.</span></span>

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

### <span data-ttu-id="d17a4-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d17a4-129">-SubscriptionId</span></span>
<span data-ttu-id="d17a4-130">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d17a4-131">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d17a4-132">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="d17a4-132">-UpdateName</span></span>
<span data-ttu-id="d17a4-133">업데이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-133">Name of the update.</span></span>

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

### <span data-ttu-id="d17a4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d17a4-134">CommonParameters</span></span>
<span data-ttu-id="d17a4-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d17a4-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d17a4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d17a4-137">입력</span><span class="sxs-lookup"><span data-stu-id="d17a4-137">INPUTS</span></span>

### <span data-ttu-id="d17a4-138">Microsoft. i d. PowerShell. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d17a4-138">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="d17a4-139">출력</span><span class="sxs-lookup"><span data-stu-id="d17a4-139">OUTPUTS</span></span>

### <span data-ttu-id="d17a4-140">Api20160501. IUpdateRun에 대 한 관리자.</span><span class="sxs-lookup"><span data-stu-id="d17a4-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="d17a4-141">상속자</span><span class="sxs-lookup"><span data-stu-id="d17a4-141">NOTES</span></span>

<span data-ttu-id="d17a4-142">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-142">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d17a4-143">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="d17a4-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d17a4-144">INPUTOBJECT <IUpdateAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d17a4-144">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d17a4-145">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="d17a4-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d17a4-146">`[ResourceGroupName <String>]`: 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-146">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="d17a4-147">`[RunName <String>]`: 업데이트 실행 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-147">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="d17a4-148">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="d17a4-149">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d17a4-150">`[UpdateLocation <String>]`: 업데이트 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-150">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="d17a4-151">`[UpdateName <String>]`: 업데이트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d17a4-151">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="d17a4-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d17a4-152">RELATED LINKS</span></span>


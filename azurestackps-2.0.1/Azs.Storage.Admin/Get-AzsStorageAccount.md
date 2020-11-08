---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 0ddf99277834e69a55b009abcb4b683eebb7a4ec
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045327"
---
# <span data-ttu-id="f5ae4-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5ae4-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="f5ae4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ae4-103">요청 된 저장소 계정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="f5ae4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5ae4-104">SYNTAX</span></span>

### <span data-ttu-id="f5ae4-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f5ae4-105">List (Default)</span></span>
```
Get-AzsStorageAccount [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>] [-Summary]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f5ae4-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="f5ae4-106">Get</span></span>
```
Get-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f5ae4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f5ae4-107">GetViaIdentity</span></span>
```
Get-AzsStorageAccount -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f5ae4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f5ae4-108">DESCRIPTION</span></span>
<span data-ttu-id="f5ae4-109">요청 된 저장소 계정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="f5ae4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f5ae4-110">EXAMPLES</span></span>

### <span data-ttu-id="f5ae4-111">예제 1:</span><span class="sxs-lookup"><span data-stu-id="f5ae4-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Summary
```

<span data-ttu-id="f5ae4-112">저장소 계정 목록 가져오기 (요약)</span><span class="sxs-lookup"><span data-stu-id="f5ae4-112">Get a list of storage accounts (summary).</span></span>

### <span data-ttu-id="f5ae4-113">예제 2:</span><span class="sxs-lookup"><span data-stu-id="f5ae4-113">Example 2:</span></span>
```powershell
PS C:\> $storageAccount = Get-AzsStorageAccount
PS C:\> $storageAccount | Select Location,Name,AccountStatus,HealthState,Kind | ft
```

<span data-ttu-id="f5ae4-114">세부 정보를 포함 하 여 저장소 계정 목록을 가져오고 상태를 인쇄 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-114">Get a list of storage account with details and print the status.</span></span>

### <span data-ttu-id="f5ae4-115">예제 3:</span><span class="sxs-lookup"><span data-stu-id="f5ae4-115">Example 3:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 | fl *
```

<span data-ttu-id="f5ae4-116">지정 된 저장소 계정에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-116">Get details of the specified storage account.</span></span>

## <span data-ttu-id="f5ae4-117">변수</span><span class="sxs-lookup"><span data-stu-id="f5ae4-117">PARAMETERS</span></span>

### <span data-ttu-id="f5ae4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ae4-118">-DefaultProfile</span></span>
<span data-ttu-id="f5ae4-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5ae4-120">-필터</span><span class="sxs-lookup"><span data-stu-id="f5ae4-120">-Filter</span></span>
<span data-ttu-id="f5ae4-121">필터 문자열</span><span class="sxs-lookup"><span data-stu-id="f5ae4-121">Filter string</span></span>

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

### <span data-ttu-id="f5ae4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5ae4-122">-InputObject</span></span>
<span data-ttu-id="f5ae4-123">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="f5ae4-124">-위치</span><span class="sxs-lookup"><span data-stu-id="f5ae4-124">-Location</span></span>
<span data-ttu-id="f5ae4-125">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-125">Resource location.</span></span>

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

### <span data-ttu-id="f5ae4-126">-이름</span><span class="sxs-lookup"><span data-stu-id="f5ae4-126">-Name</span></span>
<span data-ttu-id="f5ae4-127">테 넌 트에 표시 되지 않는 내부 저장소 계정 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-127">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f5ae4-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5ae4-128">-SubscriptionId</span></span>
<span data-ttu-id="f5ae4-129">구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-129">Subscription Id.</span></span>

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

### <span data-ttu-id="f5ae4-130">-요약</span><span class="sxs-lookup"><span data-stu-id="f5ae4-130">-Summary</span></span>
<span data-ttu-id="f5ae4-131">요약 또는 상세 정보가 반환 되는지 여부를 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-131">Switch for whether summary or detailed information is returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: $false
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f5ae4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ae4-132">CommonParameters</span></span>
<span data-ttu-id="f5ae4-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ae4-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ae4-135">입력</span><span class="sxs-lookup"><span data-stu-id="f5ae4-135">INPUTS</span></span>

### <span data-ttu-id="f5ae4-136">Microsoft. PowerShell. i d a Orageadminidentity</span><span class="sxs-lookup"><span data-stu-id="f5ae4-136">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="f5ae4-137">출력</span><span class="sxs-lookup"><span data-stu-id="f5ae4-137">OUTPUTS</span></span>

### <span data-ttu-id="f5ae4-138">Api201908Preview. i i m. i a PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-138">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageAccount</span></span>



## <span data-ttu-id="f5ae4-139">상속자</span><span class="sxs-lookup"><span data-stu-id="f5ae4-139">NOTES</span></span>

<span data-ttu-id="f5ae4-140">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f5ae4-141">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f5ae4-142">INPUTOBJECT <IStorageAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f5ae4-142">INPUTOBJECT <IStorageAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f5ae4-143">`[AccountId <String>]`: 테 넌 트에 표시 되지 않는 내부 저장소 계정 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-143">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="f5ae4-144">`[AsyncOperationId <String>]`: 비동기 작업 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-144">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="f5ae4-145">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="f5ae4-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f5ae4-146">`[Location <String>]`: 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-146">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="f5ae4-147">`[QuotaName <String>]`: 저장소 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-147">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="f5ae4-148">`[ResourceGroup <String>]`: 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-148">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="f5ae4-149">`[ServiceName <String>]`: 저장소 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-149">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="f5ae4-150">`[SubscriptionId <String>]`: 구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae4-150">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="f5ae4-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5ae4-151">RELATED LINKS</span></span>


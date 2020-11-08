---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: ed5261a9b6d65918fce0fd90c8f2db0ff42baa3a
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94045085"
---
# <span data-ttu-id="03a21-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="03a21-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="03a21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03a21-102">SYNOPSIS</span></span>


## <span data-ttu-id="03a21-103">구문과</span><span class="sxs-lookup"><span data-stu-id="03a21-103">SYNTAX</span></span>

### <span data-ttu-id="03a21-104">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="03a21-104">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="03a21-105">가져오기</span><span class="sxs-lookup"><span data-stu-id="03a21-105">Get</span></span>
```
Get-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="03a21-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="03a21-106">GetViaIdentity</span></span>
```
Get-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="03a21-107">설명은</span><span class="sxs-lookup"><span data-stu-id="03a21-107">DESCRIPTION</span></span>


## <span data-ttu-id="03a21-108">예제의</span><span class="sxs-lookup"><span data-stu-id="03a21-108">EXAMPLES</span></span>

### <span data-ttu-id="03a21-109">예제 1:</span><span class="sxs-lookup"><span data-stu-id="03a21-109">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota
```

<span data-ttu-id="03a21-110">저장소 할당량 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="03a21-110">Get the list of storage quotas.</span></span>

### <span data-ttu-id="03a21-111">예제 2:</span><span class="sxs-lookup"><span data-stu-id="03a21-111">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'Default Quota'
```

<span data-ttu-id="03a21-112">이름으로 지정 된 저장소 할당량에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="03a21-112">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="03a21-113">변수</span><span class="sxs-lookup"><span data-stu-id="03a21-113">PARAMETERS</span></span>

### <span data-ttu-id="03a21-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03a21-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="03a21-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03a21-115">-InputObject</span></span>
<span data-ttu-id="03a21-116">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="03a21-116">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: System.String
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="03a21-117">-위치</span><span class="sxs-lookup"><span data-stu-id="03a21-117">-Location</span></span>


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

### <span data-ttu-id="03a21-118">-이름</span><span class="sxs-lookup"><span data-stu-id="03a21-118">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="03a21-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="03a21-119">-SubscriptionId</span></span>


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

### <span data-ttu-id="03a21-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03a21-120">CommonParameters</span></span>
<span data-ttu-id="03a21-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="03a21-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03a21-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="03a21-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03a21-123">입력</span><span class="sxs-lookup"><span data-stu-id="03a21-123">INPUTS</span></span>

### <span data-ttu-id="03a21-124">Microsoft. PowerShell. i d a Orageadminidentity</span><span class="sxs-lookup"><span data-stu-id="03a21-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="03a21-125">출력</span><span class="sxs-lookup"><span data-stu-id="03a21-125">OUTPUTS</span></span>

### <span data-ttu-id="03a21-126">Api201908Preview. IStorageQuota에 대 한 관리자.</span><span class="sxs-lookup"><span data-stu-id="03a21-126">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="03a21-127">상속자</span><span class="sxs-lookup"><span data-stu-id="03a21-127">NOTES</span></span>

<span data-ttu-id="03a21-128">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="03a21-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="03a21-129">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="03a21-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="03a21-130">INPUTOBJECT <IStorageAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="03a21-130">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="03a21-131">`[AccountId <String>]`: 테 넌 트에 표시 되지 않는 내부 저장소 계정 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="03a21-131">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="03a21-132">`[AsyncOperationId <String>]`: 비동기 작업 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="03a21-132">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="03a21-133">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="03a21-133">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="03a21-134">`[Location <String>]`: 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="03a21-134">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="03a21-135">`[QuotaName <String>]`: 저장소 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03a21-135">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="03a21-136">`[ResourceGroup <String>]`: 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03a21-136">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="03a21-137">`[ServiceName <String>]`: 저장소 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03a21-137">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="03a21-138">`[SubscriptionId <String>]`: 구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="03a21-138">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="03a21-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03a21-139">RELATED LINKS</span></span>


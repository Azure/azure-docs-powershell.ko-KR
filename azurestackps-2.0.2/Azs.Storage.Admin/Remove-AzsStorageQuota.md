---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/remove-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: 258c7057b8f78ea6de1db506d23c60f679e1ca39
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046750"
---
# <span data-ttu-id="8388e-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="8388e-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="8388e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8388e-102">SYNOPSIS</span></span>


## <span data-ttu-id="8388e-103">구문과</span><span class="sxs-lookup"><span data-stu-id="8388e-103">SYNTAX</span></span>

### <span data-ttu-id="8388e-104">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8388e-104">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8388e-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8388e-105">DeleteViaIdentity</span></span>
```
Remove-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8388e-106">설명은</span><span class="sxs-lookup"><span data-stu-id="8388e-106">DESCRIPTION</span></span>


## <span data-ttu-id="8388e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8388e-107">EXAMPLES</span></span>

### <span data-ttu-id="8388e-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="8388e-108">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsStorageQuota -Name 'TestQuota'
```

<span data-ttu-id="8388e-109">이름으로 저장소 할당량을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8388e-109">Remove a storage quota by name.</span></span>

### <span data-ttu-id="8388e-110">예제 2:</span><span class="sxs-lookup"><span data-stu-id="8388e-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestQuota' | Remove-AzsStorageQuota
```

<span data-ttu-id="8388e-111">파이프에 따라 저장소 할당량을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8388e-111">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="8388e-112">변수</span><span class="sxs-lookup"><span data-stu-id="8388e-112">PARAMETERS</span></span>

### <span data-ttu-id="8388e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8388e-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="8388e-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8388e-114">-InputObject</span></span>
<span data-ttu-id="8388e-115">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8388e-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8388e-116">-위치</span><span class="sxs-lookup"><span data-stu-id="8388e-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8388e-117">-이름</span><span class="sxs-lookup"><span data-stu-id="8388e-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8388e-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8388e-118">-PassThru</span></span>


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

### <span data-ttu-id="8388e-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8388e-119">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8388e-120">-확인</span><span class="sxs-lookup"><span data-stu-id="8388e-120">-Confirm</span></span>
<span data-ttu-id="8388e-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8388e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8388e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8388e-122">-WhatIf</span></span>
<span data-ttu-id="8388e-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8388e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8388e-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8388e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8388e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8388e-125">CommonParameters</span></span>
<span data-ttu-id="8388e-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8388e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8388e-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8388e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8388e-128">입력</span><span class="sxs-lookup"><span data-stu-id="8388e-128">INPUTS</span></span>

### <span data-ttu-id="8388e-129">Microsoft. PowerShell. i d a Orageadminidentity</span><span class="sxs-lookup"><span data-stu-id="8388e-129">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="8388e-130">출력</span><span class="sxs-lookup"><span data-stu-id="8388e-130">OUTPUTS</span></span>

### <span data-ttu-id="8388e-131">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8388e-131">System.Boolean</span></span>



## <span data-ttu-id="8388e-132">상속자</span><span class="sxs-lookup"><span data-stu-id="8388e-132">NOTES</span></span>

<span data-ttu-id="8388e-133">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8388e-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8388e-134">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="8388e-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8388e-135">INPUTOBJECT <IStorageAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="8388e-135">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="8388e-136">`[AccountId <String>]`: 테 넌 트에 표시 되지 않는 내부 저장소 계정 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8388e-136">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="8388e-137">`[AsyncOperationId <String>]`: 비동기 작업 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="8388e-137">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="8388e-138">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="8388e-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8388e-139">`[Location <String>]`: 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="8388e-139">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="8388e-140">`[QuotaName <String>]`: 저장소 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8388e-140">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="8388e-141">`[ResourceGroup <String>]`: 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8388e-141">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="8388e-142">`[ServiceName <String>]`: 저장소 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8388e-142">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="8388e-143">`[SubscriptionId <String>]`: 구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="8388e-143">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="8388e-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8388e-144">RELATED LINKS</span></span>


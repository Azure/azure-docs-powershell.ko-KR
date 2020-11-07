---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackup
schema: 2.0.0
ms.openlocfilehash: 2c2d517da3be62ff407ca17577edefcf7322ad55
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877214"
---
# <span data-ttu-id="2bf44-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="2bf44-101">Get-AzsBackup</span></span>

## <span data-ttu-id="2bf44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bf44-102">SYNOPSIS</span></span>
<span data-ttu-id="2bf44-103">이름에 따라 위치에서 백업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bf44-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="2bf44-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2bf44-104">SYNTAX</span></span>

### <span data-ttu-id="2bf44-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="2bf44-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2bf44-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="2bf44-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2bf44-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2bf44-107">GetViaIdentity</span></span>
```
Get-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2bf44-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2bf44-108">DESCRIPTION</span></span>
<span data-ttu-id="2bf44-109">이름에 따라 위치에서 백업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bf44-109">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="2bf44-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2bf44-110">EXAMPLES</span></span>

### <span data-ttu-id="2bf44-111">예제 1: 백업 목록</span><span class="sxs-lookup"><span data-stu-id="2bf44-111">Example 1: List Backups</span></span>
```powershell
PS C:\> Get-AzsBackup

```

<span data-ttu-id="2bf44-112">모든 Azure 스택 백업 sbout 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2bf44-112">Get information sbout all Azure Stack backups.</span></span>

### <span data-ttu-id="2bf44-113">예제 2: 특정 백업 가져오기</span><span class="sxs-lookup"><span data-stu-id="2bf44-113">Example 2: Get specific backup</span></span>
```powershell
PS C:\> Get-AzsBackup -Name 'backupName'

```

<span data-ttu-id="2bf44-114">지정 된 Azure 스택 백업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2bf44-114">Get information for the the specified Azure Stack backup.</span></span>

## <span data-ttu-id="2bf44-115">변수</span><span class="sxs-lookup"><span data-stu-id="2bf44-115">PARAMETERS</span></span>

### <span data-ttu-id="2bf44-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bf44-116">-DefaultProfile</span></span>
<span data-ttu-id="2bf44-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2bf44-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bf44-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2bf44-118">-InputObject</span></span>
<span data-ttu-id="2bf44-119">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2bf44-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="2bf44-120">-위치</span><span class="sxs-lookup"><span data-stu-id="2bf44-120">-Location</span></span>
<span data-ttu-id="2bf44-121">백업 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2bf44-121">Name of the backup location.</span></span>

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

### <span data-ttu-id="2bf44-122">-이름</span><span class="sxs-lookup"><span data-stu-id="2bf44-122">-Name</span></span>
<span data-ttu-id="2bf44-123">백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2bf44-123">Name of the backup.</span></span>

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

### <span data-ttu-id="2bf44-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bf44-124">-ResourceGroupName</span></span>
<span data-ttu-id="2bf44-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2bf44-125">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2bf44-126">-생략</span><span class="sxs-lookup"><span data-stu-id="2bf44-126">-Skip</span></span>
<span data-ttu-id="2bf44-127">OData skip 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="2bf44-127">OData skip parameter.</span></span>

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

### <span data-ttu-id="2bf44-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2bf44-128">-SubscriptionId</span></span>
<span data-ttu-id="2bf44-129">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="2bf44-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2bf44-130">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bf44-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2bf44-131">-위쪽</span><span class="sxs-lookup"><span data-stu-id="2bf44-131">-Top</span></span>
<span data-ttu-id="2bf44-132">OData top 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="2bf44-132">OData top parameter.</span></span>

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

### <span data-ttu-id="2bf44-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bf44-133">CommonParameters</span></span>
<span data-ttu-id="2bf44-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bf44-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bf44-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2bf44-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bf44-136">입력</span><span class="sxs-lookup"><span data-stu-id="2bf44-136">INPUTS</span></span>

### <span data-ttu-id="2bf44-137">Microsoft. PowerShell. i d. a i m. 관리자. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="2bf44-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="2bf44-138">출력</span><span class="sxs-lookup"><span data-stu-id="2bf44-138">OUTPUTS</span></span>

### <span data-ttu-id="2bf44-139">Api20180901/. i i a i. i m a 백업</span><span class="sxs-lookup"><span data-stu-id="2bf44-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="2bf44-140">상속자</span><span class="sxs-lookup"><span data-stu-id="2bf44-140">NOTES</span></span>

<span data-ttu-id="2bf44-141">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bf44-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2bf44-142">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="2bf44-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2bf44-143">INPUTOBJECT <IBackupAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2bf44-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2bf44-144">`[Backup <String>]`: 백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2bf44-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="2bf44-145">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="2bf44-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2bf44-146">`[Location <String>]`: 백업 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2bf44-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="2bf44-147">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2bf44-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="2bf44-148">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="2bf44-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2bf44-149">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bf44-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2bf44-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2bf44-150">RELATED LINKS</span></span>


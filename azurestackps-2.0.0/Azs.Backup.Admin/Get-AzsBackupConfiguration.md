---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 3a9fedc637f8400b952d823a98dfe0abaa1d40d3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877216"
---
# <span data-ttu-id="29e46-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="29e46-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="29e46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29e46-102">SYNOPSIS</span></span>
<span data-ttu-id="29e46-103">이름에 따라 특정 백업 위치를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="29e46-103">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="29e46-104">구문과</span><span class="sxs-lookup"><span data-stu-id="29e46-104">SYNTAX</span></span>

### <span data-ttu-id="29e46-105">Get (기본값)</span><span class="sxs-lookup"><span data-stu-id="29e46-105">Get (Default)</span></span>
```
Get-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="29e46-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="29e46-106">GetViaIdentity</span></span>
```
Get-AzsBackupConfiguration -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="29e46-107">목록</span><span class="sxs-lookup"><span data-stu-id="29e46-107">List</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="29e46-108">설명은</span><span class="sxs-lookup"><span data-stu-id="29e46-108">DESCRIPTION</span></span>
<span data-ttu-id="29e46-109">이름에 따라 특정 백업 위치를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="29e46-109">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="29e46-110">예제의</span><span class="sxs-lookup"><span data-stu-id="29e46-110">EXAMPLES</span></span>

### <span data-ttu-id="29e46-111">예제 1: Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="29e46-111">Example 1: Get-AzsBackupConfiguration</span></span>
```powershell
PS C:\> Get-AzsBackupConfiguration

```

<span data-ttu-id="29e46-112">Azure 스택 백업 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="29e46-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="29e46-113">변수</span><span class="sxs-lookup"><span data-stu-id="29e46-113">PARAMETERS</span></span>

### <span data-ttu-id="29e46-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29e46-114">-DefaultProfile</span></span>
<span data-ttu-id="29e46-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29e46-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29e46-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29e46-116">-InputObject</span></span>
<span data-ttu-id="29e46-117">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="29e46-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="29e46-118">-위치</span><span class="sxs-lookup"><span data-stu-id="29e46-118">-Location</span></span>
<span data-ttu-id="29e46-119">백업 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29e46-119">Name of the backup location.</span></span>

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

### <span data-ttu-id="29e46-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29e46-120">-ResourceGroupName</span></span>
<span data-ttu-id="29e46-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29e46-121">Name of the resource group.</span></span>

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

### <span data-ttu-id="29e46-122">-생략</span><span class="sxs-lookup"><span data-stu-id="29e46-122">-Skip</span></span>
<span data-ttu-id="29e46-123">OData skip 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="29e46-123">OData skip parameter.</span></span>

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

### <span data-ttu-id="29e46-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="29e46-124">-SubscriptionId</span></span>
<span data-ttu-id="29e46-125">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="29e46-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="29e46-126">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="29e46-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="29e46-127">-위쪽</span><span class="sxs-lookup"><span data-stu-id="29e46-127">-Top</span></span>
<span data-ttu-id="29e46-128">OData top 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="29e46-128">OData top parameter.</span></span>

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

### <span data-ttu-id="29e46-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29e46-129">CommonParameters</span></span>
<span data-ttu-id="29e46-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="29e46-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29e46-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="29e46-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29e46-132">입력</span><span class="sxs-lookup"><span data-stu-id="29e46-132">INPUTS</span></span>

### <span data-ttu-id="29e46-133">Microsoft. PowerShell. i d. a i m. 관리자. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="29e46-133">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="29e46-134">출력</span><span class="sxs-lookup"><span data-stu-id="29e46-134">OUTPUTS</span></span>

### <span data-ttu-id="29e46-135">Api20180901. IBackupLocation에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="29e46-135">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="29e46-136">상속자</span><span class="sxs-lookup"><span data-stu-id="29e46-136">NOTES</span></span>

<span data-ttu-id="29e46-137">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="29e46-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="29e46-138">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="29e46-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="29e46-139">INPUTOBJECT <IBackupAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="29e46-139">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="29e46-140">`[Backup <String>]`: 백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29e46-140">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="29e46-141">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="29e46-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="29e46-142">`[Location <String>]`: 백업 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29e46-142">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="29e46-143">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29e46-143">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="29e46-144">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="29e46-144">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="29e46-145">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="29e46-145">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="29e46-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29e46-146">RELATED LINKS</span></span>


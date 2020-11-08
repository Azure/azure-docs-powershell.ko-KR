---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/start-azsbackup
schema: 2.0.0
ms.openlocfilehash: 37fc3ddb1c878bc8b6b1e14d920a5747edce0cd3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047034"
---
# <span data-ttu-id="6009c-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="6009c-101">Start-AzsBackup</span></span>

## <span data-ttu-id="6009c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6009c-102">SYNOPSIS</span></span>
<span data-ttu-id="6009c-103">특정 위치를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="6009c-103">Back up a specific location.</span></span>

## <span data-ttu-id="6009c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6009c-104">SYNTAX</span></span>

### <span data-ttu-id="6009c-105">만들기 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6009c-105">Create (Default)</span></span>
```
Start-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6009c-106">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6009c-106">CreateViaIdentity</span></span>
```
Start-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6009c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6009c-107">DESCRIPTION</span></span>
<span data-ttu-id="6009c-108">특정 위치를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="6009c-108">Back up a specific location.</span></span>

## <span data-ttu-id="6009c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6009c-109">EXAMPLES</span></span>

### <span data-ttu-id="6009c-110">예제 1: azurestack 백업 시작</span><span class="sxs-lookup"><span data-stu-id="6009c-110">Example 1: Start azurestack backup</span></span>
```powershell
PS C:\>Start-AzsBackup

```

<span data-ttu-id="6009c-111">Azure 스택 백업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6009c-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="6009c-112">변수</span><span class="sxs-lookup"><span data-stu-id="6009c-112">PARAMETERS</span></span>

### <span data-ttu-id="6009c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6009c-113">-AsJob</span></span>
<span data-ttu-id="6009c-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="6009c-114">Run the command as a job</span></span>

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

### <span data-ttu-id="6009c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6009c-115">-DefaultProfile</span></span>
<span data-ttu-id="6009c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6009c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6009c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6009c-117">-InputObject</span></span>
<span data-ttu-id="6009c-118">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6009c-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6009c-119">-위치</span><span class="sxs-lookup"><span data-stu-id="6009c-119">-Location</span></span>
<span data-ttu-id="6009c-120">백업 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6009c-120">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6009c-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6009c-121">-NoWait</span></span>
<span data-ttu-id="6009c-122">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="6009c-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6009c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6009c-123">-ResourceGroupName</span></span>
<span data-ttu-id="6009c-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6009c-124">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6009c-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6009c-125">-SubscriptionId</span></span>
<span data-ttu-id="6009c-126">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="6009c-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6009c-127">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6009c-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6009c-128">-확인</span><span class="sxs-lookup"><span data-stu-id="6009c-128">-Confirm</span></span>
<span data-ttu-id="6009c-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6009c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6009c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6009c-130">-WhatIf</span></span>
<span data-ttu-id="6009c-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6009c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6009c-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6009c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6009c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6009c-133">CommonParameters</span></span>
<span data-ttu-id="6009c-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6009c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6009c-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6009c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6009c-136">입력</span><span class="sxs-lookup"><span data-stu-id="6009c-136">INPUTS</span></span>

### <span data-ttu-id="6009c-137">Microsoft. PowerShell. i d. a i m. 관리자. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="6009c-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="6009c-138">출력</span><span class="sxs-lookup"><span data-stu-id="6009c-138">OUTPUTS</span></span>

### <span data-ttu-id="6009c-139">Api20180901/. i i a i. i m a 백업</span><span class="sxs-lookup"><span data-stu-id="6009c-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="6009c-140">상속자</span><span class="sxs-lookup"><span data-stu-id="6009c-140">NOTES</span></span>

<span data-ttu-id="6009c-141">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6009c-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6009c-142">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="6009c-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6009c-143">INPUTOBJECT <IBackupAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6009c-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6009c-144">`[Backup <String>]`: 백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6009c-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="6009c-145">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="6009c-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6009c-146">`[Location <String>]`: 백업 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6009c-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="6009c-147">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6009c-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="6009c-148">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="6009c-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6009c-149">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6009c-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6009c-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6009c-150">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/restore-azsbackup
schema: 2.0.0
ms.openlocfilehash: d441c74817ccaf1b32b7caf6fe811f6a5a4789da
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877215"
---
# <span data-ttu-id="bb58a-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="bb58a-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="bb58a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb58a-102">SYNOPSIS</span></span>
<span data-ttu-id="bb58a-103">백업을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-103">Restore a backup.</span></span>

## <span data-ttu-id="bb58a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb58a-104">SYNTAX</span></span>

### <span data-ttu-id="bb58a-105">RestoreExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="bb58a-105">RestoreExpanded (Default)</span></span>
```
Restore-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DecryptionCertPassword <SecureString>] [-DecryptionCertPath <String>] [-RoleName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="bb58a-106">복원한</span><span class="sxs-lookup"><span data-stu-id="bb58a-106">Restore</span></span>
```
Restore-AzsBackup -Name <String> -RestoreOption <IRestoreOptions> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bb58a-107">RestoreViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bb58a-107">RestoreViaIdentity</span></span>
```
Restore-AzsBackup -InputObject <IBackupAdminIdentity> -RestoreOption <IRestoreOptions>
 [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="bb58a-108">RestoreViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bb58a-108">RestoreViaIdentityExpanded</span></span>
```
Restore-AzsBackup -InputObject <IBackupAdminIdentity> [-DecryptionCertPassword <SecureString>]
 [-DecryptionCertPath <String>] [-RoleName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bb58a-109">설명은</span><span class="sxs-lookup"><span data-stu-id="bb58a-109">DESCRIPTION</span></span>
<span data-ttu-id="bb58a-110">백업을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-110">Restore a backup.</span></span>

## <span data-ttu-id="bb58a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="bb58a-111">EXAMPLES</span></span>

### <span data-ttu-id="bb58a-112">예제 1: 백업 복원</span><span class="sxs-lookup"><span data-stu-id="bb58a-112">Example 1: Restore Backup</span></span>
```powershell
PS C:\> Restore-AzsBackup -Name $backupResourceName -DecryptionCertPath $decryptionCertPath -DecryptionCertPassword $decryptionCertPassword

```

<span data-ttu-id="bb58a-113">Azure 스택 백업에서 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-113">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="bb58a-114">변수</span><span class="sxs-lookup"><span data-stu-id="bb58a-114">PARAMETERS</span></span>

### <span data-ttu-id="bb58a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb58a-115">-AsJob</span></span>
<span data-ttu-id="bb58a-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="bb58a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bb58a-117">-DecryptionCertPassword</span><span class="sxs-lookup"><span data-stu-id="bb58a-117">-DecryptionCertPassword</span></span>
<span data-ttu-id="bb58a-118">암호 해독 인증서의 비밀 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-118">The password for the decryption certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bb58a-119">-DecryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="bb58a-119">-DecryptionCertPath</span></span>
<span data-ttu-id="bb58a-120">개인 키 (.pfx)를 사용 하 여 암호 해독 인증서 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-120">Path to the decryption cert file with private key (.pfx).</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bb58a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb58a-121">-DefaultProfile</span></span>
<span data-ttu-id="bb58a-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb58a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="bb58a-123">-Force</span></span>
<span data-ttu-id="bb58a-124">확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="bb58a-124">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="bb58a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb58a-125">-InputObject</span></span>
<span data-ttu-id="bb58a-126">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: RestoreViaIdentity, RestoreViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="bb58a-127">-위치</span><span class="sxs-lookup"><span data-stu-id="bb58a-127">-Location</span></span>
<span data-ttu-id="bb58a-128">백업 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-128">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bb58a-129">-이름</span><span class="sxs-lookup"><span data-stu-id="bb58a-129">-Name</span></span>
<span data-ttu-id="bb58a-130">백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-130">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bb58a-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bb58a-131">-NoWait</span></span>
<span data-ttu-id="bb58a-132">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="bb58a-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bb58a-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb58a-133">-PassThru</span></span>
<span data-ttu-id="bb58a-134">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-134">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bb58a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb58a-135">-ResourceGroupName</span></span>
<span data-ttu-id="bb58a-136">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-136">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bb58a-137">-RestoreOption</span><span class="sxs-lookup"><span data-stu-id="bb58a-137">-RestoreOption</span></span>
<span data-ttu-id="bb58a-138">복원 옵션에 대 한 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-138">Properties for restore options.</span></span>
<span data-ttu-id="bb58a-139">생성 하려면 RESTOREOPTION 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-139">To construct, see NOTES section for RESTOREOPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IRestoreOptions
Parameter Sets: Restore, RestoreViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bb58a-140">-RoleName</span><span class="sxs-lookup"><span data-stu-id="bb58a-140">-RoleName</span></span>
<span data-ttu-id="bb58a-141">복원에 대 한 Azure 스택 역할 이름으로, 모든 인프라 역할에 대해 empty로 설정</span><span class="sxs-lookup"><span data-stu-id="bb58a-141">The Azure Stack role name for restore, set it to empty for all infrastructure role</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bb58a-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb58a-142">-SubscriptionId</span></span>
<span data-ttu-id="bb58a-143">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-143">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bb58a-144">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bb58a-145">-확인</span><span class="sxs-lookup"><span data-stu-id="bb58a-145">-Confirm</span></span>
<span data-ttu-id="bb58a-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb58a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb58a-147">-WhatIf</span></span>
<span data-ttu-id="bb58a-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb58a-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb58a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb58a-150">CommonParameters</span></span>
<span data-ttu-id="bb58a-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb58a-152">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bb58a-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb58a-153">입력</span><span class="sxs-lookup"><span data-stu-id="bb58a-153">INPUTS</span></span>

### <span data-ttu-id="bb58a-154">Microsoft. PowerShell. i d. a i m. 관리자. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="bb58a-154">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="bb58a-155">출력</span><span class="sxs-lookup"><span data-stu-id="bb58a-155">OUTPUTS</span></span>

### <span data-ttu-id="bb58a-156">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="bb58a-156">System.Boolean</span></span>



## <span data-ttu-id="bb58a-157">상속자</span><span class="sxs-lookup"><span data-stu-id="bb58a-157">NOTES</span></span>

<span data-ttu-id="bb58a-158">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-158">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bb58a-159">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="bb58a-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="bb58a-160">INPUTOBJECT <IBackupAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="bb58a-160">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bb58a-161">`[Backup <String>]`: 백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-161">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="bb58a-162">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="bb58a-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bb58a-163">`[Location <String>]`: 백업 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-163">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="bb58a-164">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="bb58a-165">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-165">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bb58a-166">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-166">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="bb58a-167">RESTOREOPTION <IRestoreOptions> : 복원 옵션에 대 한 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-167">RESTOREOPTION <IRestoreOptions>: Properties for restore options.</span></span>
  - <span data-ttu-id="bb58a-168">`[DecryptionCertBase64 <String>]`: 인증서 파일에 Base64 문자열의 원시 데이터가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-168">`[DecryptionCertBase64 <String>]`: The certificate file raw data in Base64 string.</span></span> <span data-ttu-id="bb58a-169">개인 키를 사용 하 여 .pfx 파일 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-169">This should be the .pfx file with the private key.</span></span>
  - <span data-ttu-id="bb58a-170">`[DecryptionCertPassword <String>]`: 암호 해독 인증서의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="bb58a-170">`[DecryptionCertPassword <String>]`: The password for the decryption certificate.</span></span>
  - <span data-ttu-id="bb58a-171">`[RoleName <String>]`: 복원에 대 한 Azure 스택 역할 이름으로, 모든 인프라 역할에 대해 empty로 설정</span><span class="sxs-lookup"><span data-stu-id="bb58a-171">`[RoleName <String>]`: The Azure Stack role name for restore, set it to empty for all infrastructure role</span></span>

## <span data-ttu-id="bb58a-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb58a-172">RELATED LINKS</span></span>


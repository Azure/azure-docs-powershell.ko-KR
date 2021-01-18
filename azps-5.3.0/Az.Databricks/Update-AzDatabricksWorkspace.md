---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
ms.openlocfilehash: 0d213dd18ea2423c90dec6446e4551cbcd8d161a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494609"
---
# <span data-ttu-id="c4e86-101">Update-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="c4e86-101">Update-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="c4e86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4e86-102">SYNOPSIS</span></span>
<span data-ttu-id="c4e86-103">작업 영역 업데이트</span><span class="sxs-lookup"><span data-stu-id="c4e86-103">Updates a workspace.</span></span>

## <span data-ttu-id="c4e86-104">구문</span><span class="sxs-lookup"><span data-stu-id="c4e86-104">SYNTAX</span></span>

### <span data-ttu-id="c4e86-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="c4e86-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>]
 [-EncryptionKeyVersion <String>] [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c4e86-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c4e86-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-EncryptionKeyName <String>]
 [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>] [-EncryptionKeyVersion <String>]
 [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c4e86-107">설명</span><span class="sxs-lookup"><span data-stu-id="c4e86-107">DESCRIPTION</span></span>
<span data-ttu-id="c4e86-108">작업 영역 업데이트</span><span class="sxs-lookup"><span data-stu-id="c4e86-108">Updates a workspace.</span></span>

## <span data-ttu-id="c4e86-109">예제</span><span class="sxs-lookup"><span data-stu-id="c4e86-109">EXAMPLES</span></span>

### <span data-ttu-id="c4e86-110">예제 1: Databricks 작업 영역의 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="c4e86-110">Example 1: Updates the tags of a Databricks workspace</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceopsc46 -Tag @{'key'=1}
PS C:\> Update-AzDatabricksWorkspace -InputObject $dbr -Tag @{key="value"}

Name            Location Managed Resource Group ID
----            -------- -------------------------
workspaceopsc46 eastus   /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceopsc46-wfgp3ayhu6jkn
```

<span data-ttu-id="c4e86-111">이 명령은 Databricks 작업 영역의 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-111">This command updates the tags of a Databricks workspace.</span></span>

### <span data-ttu-id="c4e86-112">예제 2: Databricks 작업 영역에서 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="c4e86-112">Example 2: Enable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -PrepareEncryption
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Microsoft.KeyVault' -EncryptionKeyVaultUri https://keyvalult-j3kube.vault.azure.net/ -EncryptionKeyName key-p3bjsf -EncryptionKeyVersion 853999da89714fb4a1408681945135fd

Name            Location       Managed Resource Group ID
----            --------       -------------------------
workspaceypae6l East US 2 EUAP /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceypae6l-wzefrgv2b075t
```

<span data-ttu-id="c4e86-113">Databricks 작업 영역의 암호화를 사용하도록 설정하는 데는 다음 세 단계가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-113">Enabling encryption on a Databricks workspace takes three steps:</span></span>
1.
<span data-ttu-id="c4e86-114">작업 영역이 만들어지지 않은 경우 `-PrepareEncryption` 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-114">Update the workspace with `-PrepareEncryption` (if it was not created so).</span></span>
1.
<span data-ttu-id="c4e86-115">마지막 `StorageAccountIdentityPrincipalId` 단계의 출력에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-115">Find `StorageAccountIdentityPrincipalId` in the output of the last step.</span></span>
<span data-ttu-id="c4e86-116">보안 주체에 키 사용 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-116">Grant key permissions to the principal.</span></span>
1.
<span data-ttu-id="c4e86-117">암호화 키에 대한 정보를 입력하기 위해 작업 영역 다시 업데이트:</span><span class="sxs-lookup"><span data-stu-id="c4e86-117">Update the workspace again to fill in information about the encryption key:</span></span>
    - `-EncryptionKeySource`
    - `-EncryptionKeyVaultUri`
    - `-EncryptionKeyName`
    - `-EncryptionKeyVersion`

### <span data-ttu-id="c4e86-118">예제 3: Databricks 작업 영역의 암호화 사용 안</span><span class="sxs-lookup"><span data-stu-id="c4e86-118">Example 3: Disable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Default'
```

<span data-ttu-id="c4e86-119">암호화를 사용하지 않도록 설정하기 위해 .로 `-EncryptionKeySource` 설정하기만 `'Default'` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-119">To disable encryption, simply set `-EncryptionKeySource` to `'Default'`.</span></span>

## <span data-ttu-id="c4e86-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4e86-120">PARAMETERS</span></span>

### <span data-ttu-id="c4e86-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4e86-121">-AsJob</span></span>
<span data-ttu-id="c4e86-122">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="c4e86-122">Run the command as a job</span></span>

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

### <span data-ttu-id="c4e86-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4e86-123">-DefaultProfile</span></span>
<span data-ttu-id="c4e86-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4e86-125">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="c4e86-125">-EncryptionKeyName</span></span>
<span data-ttu-id="c4e86-126">Key Vault 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-126">The name of Key Vault key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e86-127">-EncryptionKeySource</span><span class="sxs-lookup"><span data-stu-id="c4e86-127">-EncryptionKeySource</span></span>
<span data-ttu-id="c4e86-128">암호화 keySource(공급자)</span><span class="sxs-lookup"><span data-stu-id="c4e86-128">The encryption keySource (provider).</span></span>
<span data-ttu-id="c4e86-129">가능한 값(대/소문자 무관): 기본값, Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="c4e86-129">Possible values (case-insensitive): Default, Microsoft.Keyvault</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Support.KeySource
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e86-130">-EncryptionKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="c4e86-130">-EncryptionKeyVaultUri</span></span>
<span data-ttu-id="c4e86-131">Key Vault의 URI(DNS 이름)입니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-131">The URI (DNS name) of the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e86-132">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="c4e86-132">-EncryptionKeyVersion</span></span>
<span data-ttu-id="c4e86-133">KeyVault 키의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-133">The version of KeyVault key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e86-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4e86-134">-InputObject</span></span>
<span data-ttu-id="c4e86-135">ID 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-135">Identity parameter.</span></span>
<span data-ttu-id="c4e86-136">생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="c4e86-136">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4e86-137">-Name</span><span class="sxs-lookup"><span data-stu-id="c4e86-137">-Name</span></span>
<span data-ttu-id="c4e86-138">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-138">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e86-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c4e86-139">-NoWait</span></span>
<span data-ttu-id="c4e86-140">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="c4e86-140">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c4e86-141">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="c4e86-141">-PrepareEncryption</span></span>
<span data-ttu-id="c4e86-142">암호화를 위해 작업 영역 준비</span><span class="sxs-lookup"><span data-stu-id="c4e86-142">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="c4e86-143">관리되는 저장소 계정에 대한 관리 ID를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-143">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="c4e86-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4e86-144">-ResourceGroupName</span></span>
<span data-ttu-id="c4e86-145">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-145">The name of the resource group.</span></span>
<span data-ttu-id="c4e86-146">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-146">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e86-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4e86-147">-SubscriptionId</span></span>
<span data-ttu-id="c4e86-148">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-148">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e86-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="c4e86-149">-Tag</span></span>
<span data-ttu-id="c4e86-150">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="c4e86-150">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e86-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4e86-151">-Confirm</span></span>
<span data-ttu-id="c4e86-152">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4e86-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4e86-153">-WhatIf</span></span>
<span data-ttu-id="c4e86-154">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c4e86-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4e86-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4e86-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4e86-156">CommonParameters</span></span>
<span data-ttu-id="c4e86-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4e86-158">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c4e86-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4e86-159">입력</span><span class="sxs-lookup"><span data-stu-id="c4e86-159">INPUTS</span></span>

### <span data-ttu-id="c4e86-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="c4e86-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="c4e86-161">출력</span><span class="sxs-lookup"><span data-stu-id="c4e86-161">OUTPUTS</span></span>

### <span data-ttu-id="c4e86-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="c4e86-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="c4e86-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c4e86-163">NOTES</span></span>

<span data-ttu-id="c4e86-164">별칭</span><span class="sxs-lookup"><span data-stu-id="c4e86-164">ALIASES</span></span>

<span data-ttu-id="c4e86-165">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="c4e86-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c4e86-166">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c4e86-167">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c4e86-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c4e86-168">INPUTOBJECT: <IDatabricksIdentity> ID 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-168">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="c4e86-169">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="c4e86-169">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c4e86-170">`[PeeringName <String>]`: 작업 영역 vNet 피어링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-170">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="c4e86-171">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-171">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c4e86-172">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-172">The name is case insensitive.</span></span>
  - <span data-ttu-id="c4e86-173">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c4e86-174">`[WorkspaceName <String>]`: 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4e86-174">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="c4e86-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4e86-175">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
ms.openlocfilehash: 0d213dd18ea2423c90dec6446e4551cbcd8d161a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212811"
---
# <span data-ttu-id="a5d51-101">Update-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="a5d51-101">Update-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="a5d51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5d51-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d51-103">작업 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-103">Updates a workspace.</span></span>

## <span data-ttu-id="a5d51-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5d51-104">SYNTAX</span></span>

### <span data-ttu-id="a5d51-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a5d51-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>]
 [-EncryptionKeyVersion <String>] [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a5d51-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a5d51-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-EncryptionKeyName <String>]
 [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>] [-EncryptionKeyVersion <String>]
 [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a5d51-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a5d51-107">DESCRIPTION</span></span>
<span data-ttu-id="a5d51-108">작업 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-108">Updates a workspace.</span></span>

## <span data-ttu-id="a5d51-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a5d51-109">EXAMPLES</span></span>

### <span data-ttu-id="a5d51-110">예제 1: Databricks 작업 영역의 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="a5d51-110">Example 1: Updates the tags of a Databricks workspace</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceopsc46 -Tag @{'key'=1}
PS C:\> Update-AzDatabricksWorkspace -InputObject $dbr -Tag @{key="value"}

Name            Location Managed Resource Group ID
----            -------- -------------------------
workspaceopsc46 eastus   /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceopsc46-wfgp3ayhu6jkn
```

<span data-ttu-id="a5d51-111">이 명령은 Databricks workspace의 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-111">This command updates the tags of a Databricks workspace.</span></span>

### <span data-ttu-id="a5d51-112">예제 2: Databricks 작업 영역에서 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="a5d51-112">Example 2: Enable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -PrepareEncryption
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Microsoft.KeyVault' -EncryptionKeyVaultUri https://keyvalult-j3kube.vault.azure.net/ -EncryptionKeyName key-p3bjsf -EncryptionKeyVersion 853999da89714fb4a1408681945135fd

Name            Location       Managed Resource Group ID
----            --------       -------------------------
workspaceypae6l East US 2 EUAP /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceypae6l-wzefrgv2b075t
```

<span data-ttu-id="a5d51-113">Databricks 작업 영역에서 암호화를 사용 하도록 설정 하는 단계는 다음과 같이 세 가지입니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-113">Enabling encryption on a Databricks workspace takes three steps:</span></span>
1.
<span data-ttu-id="a5d51-114">작업 영역을 `-PrepareEncryption` (만들지 않은 경우)으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-114">Update the workspace with `-PrepareEncryption` (if it was not created so).</span></span>
1.
<span data-ttu-id="a5d51-115">`StorageAccountIdentityPrincipalId`마지막 단계의 출력을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-115">Find `StorageAccountIdentityPrincipalId` in the output of the last step.</span></span>
<span data-ttu-id="a5d51-116">보안 주체에 키 사용 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-116">Grant key permissions to the principal.</span></span>
1.
<span data-ttu-id="a5d51-117">작업 영역을 다시 업데이트 하 여 암호화 키에 대 한 정보를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-117">Update the workspace again to fill in information about the encryption key:</span></span>
    - `-EncryptionKeySource`
    - `-EncryptionKeyVaultUri`
    - `-EncryptionKeyName`
    - `-EncryptionKeyVersion`

### <span data-ttu-id="a5d51-118">예제 3: Databricks 작업 영역에서 암호화 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="a5d51-118">Example 3: Disable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Default'
```

<span data-ttu-id="a5d51-119">암호화를 사용 하지 않으려면 `-EncryptionKeySource` 로 설정 `'Default'` 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-119">To disable encryption, simply set `-EncryptionKeySource` to `'Default'`.</span></span>

## <span data-ttu-id="a5d51-120">변수</span><span class="sxs-lookup"><span data-stu-id="a5d51-120">PARAMETERS</span></span>

### <span data-ttu-id="a5d51-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5d51-121">-AsJob</span></span>
<span data-ttu-id="a5d51-122">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="a5d51-122">Run the command as a job</span></span>

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

### <span data-ttu-id="a5d51-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d51-123">-DefaultProfile</span></span>
<span data-ttu-id="a5d51-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5d51-125">-A</span><span class="sxs-lookup"><span data-stu-id="a5d51-125">-EncryptionKeyName</span></span>
<span data-ttu-id="a5d51-126">키 자격 증명 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-126">The name of Key Vault key.</span></span>

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

### <span data-ttu-id="a5d51-127">-EncryptionKeySource</span><span class="sxs-lookup"><span data-stu-id="a5d51-127">-EncryptionKeySource</span></span>
<span data-ttu-id="a5d51-128">암호화 keySource (공급자)입니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-128">The encryption keySource (provider).</span></span>
<span data-ttu-id="a5d51-129">사용할 수 있는 값 (대/소문자 구분 안 함): 기본값, Microsoft. Keyvault</span><span class="sxs-lookup"><span data-stu-id="a5d51-129">Possible values (case-insensitive): Default, Microsoft.Keyvault</span></span>

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

### <span data-ttu-id="a5d51-130">-EncryptionKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="a5d51-130">-EncryptionKeyVaultUri</span></span>
<span data-ttu-id="a5d51-131">키 자격 증명 모음의 URI (DNS 이름)입니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-131">The URI (DNS name) of the Key Vault.</span></span>

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

### <span data-ttu-id="a5d51-132">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="a5d51-132">-EncryptionKeyVersion</span></span>
<span data-ttu-id="a5d51-133">KeyVault 키 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-133">The version of KeyVault key.</span></span>

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

### <span data-ttu-id="a5d51-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5d51-134">-InputObject</span></span>
<span data-ttu-id="a5d51-135">Id 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-135">Identity parameter.</span></span>
<span data-ttu-id="a5d51-136">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-136">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a5d51-137">-이름</span><span class="sxs-lookup"><span data-stu-id="a5d51-137">-Name</span></span>
<span data-ttu-id="a5d51-138">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-138">The name of the workspace.</span></span>

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

### <span data-ttu-id="a5d51-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a5d51-139">-NoWait</span></span>
<span data-ttu-id="a5d51-140">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="a5d51-140">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a5d51-141">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="a5d51-141">-PrepareEncryption</span></span>
<span data-ttu-id="a5d51-142">암호화를 위해 작업 영역을 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-142">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="a5d51-143">관리 되는 저장소 계정에 관리 되는 Id를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-143">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="a5d51-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d51-144">-ResourceGroupName</span></span>
<span data-ttu-id="a5d51-145">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-145">The name of the resource group.</span></span>
<span data-ttu-id="a5d51-146">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-146">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a5d51-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5d51-147">-SubscriptionId</span></span>
<span data-ttu-id="a5d51-148">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-148">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a5d51-149">태그</span><span class="sxs-lookup"><span data-stu-id="a5d51-149">-Tag</span></span>
<span data-ttu-id="a5d51-150">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="a5d51-150">Resource tags.</span></span>

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

### <span data-ttu-id="a5d51-151">-확인</span><span class="sxs-lookup"><span data-stu-id="a5d51-151">-Confirm</span></span>
<span data-ttu-id="a5d51-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5d51-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5d51-153">-WhatIf</span></span>
<span data-ttu-id="a5d51-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5d51-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5d51-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d51-156">CommonParameters</span></span>
<span data-ttu-id="a5d51-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d51-158">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5d51-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d51-159">입력</span><span class="sxs-lookup"><span data-stu-id="a5d51-159">INPUTS</span></span>

### <span data-ttu-id="a5d51-160">Databricks. IDatabricksIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="a5d51-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="a5d51-161">출력</span><span class="sxs-lookup"><span data-stu-id="a5d51-161">OUTPUTS</span></span>

### <span data-ttu-id="a5d51-162">Databricks. Api20180401에 대 한 작업 영역</span><span class="sxs-lookup"><span data-stu-id="a5d51-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="a5d51-163">상속자</span><span class="sxs-lookup"><span data-stu-id="a5d51-163">NOTES</span></span>

<span data-ttu-id="a5d51-164">별칭과</span><span class="sxs-lookup"><span data-stu-id="a5d51-164">ALIASES</span></span>

<span data-ttu-id="a5d51-165">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a5d51-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a5d51-166">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a5d51-167">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5d51-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a5d51-168">INPUTOBJECT <IDatabricksIdentity> : Identity 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-168">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="a5d51-169">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="a5d51-169">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a5d51-170">`[PeeringName <String>]`: 작업 영역 vNet 피어 링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-170">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="a5d51-171">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-171">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a5d51-172">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-172">The name is case insensitive.</span></span>
  - <span data-ttu-id="a5d51-173">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a5d51-174">`[WorkspaceName <String>]`: 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5d51-174">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="a5d51-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5d51-175">RELATED LINKS</span></span>


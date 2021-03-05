---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
ms.openlocfilehash: 631cb05e15231bb4e695ad3047a7736177a785e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976971"
---
# <span data-ttu-id="fcfd7-101">Update-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fcfd7-101">Update-AzKeyVaultKey</span></span>

## <span data-ttu-id="fcfd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcfd7-102">SYNOPSIS</span></span>
<span data-ttu-id="fcfd7-103">키 자격 증명 모음에서 키의 특성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="fcfd7-104">구문</span><span class="sxs-lookup"><span data-stu-id="fcfd7-104">SYNTAX</span></span>

### <span data-ttu-id="fcfd7-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="fcfd7-105">Default (Default)</span></span>
```
Update-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcfd7-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="fcfd7-106">HsmInteractive</span></span>
```
Update-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcfd7-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="fcfd7-107">InputObject</span></span>
```
Update-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcfd7-108">설명</span><span class="sxs-lookup"><span data-stu-id="fcfd7-108">DESCRIPTION</span></span>
<span data-ttu-id="fcfd7-109">**Update-AzKeyVaultKey** cmdlet은 키 자격 증명 모음에서 키의 편집 가능한 특성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-109">The **Update-AzKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="fcfd7-110">예제</span><span class="sxs-lookup"><span data-stu-id="fcfd7-110">EXAMPLES</span></span>

### <span data-ttu-id="fcfd7-111">예제 1: 키를 사용하도록 수정하고 만료 날짜 및 태그를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-111">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 7:59:02 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="fcfd7-112">첫 번째 명령은 **Get-Date** cmdlet을 사용하여 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-112">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="fcfd7-113">이 개체는 향후 2년의 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-113">That object specifies a time two years in the future.</span></span> <span data-ttu-id="fcfd7-114">명령은 이 날짜를 $Expires 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-114">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="fcfd7-115">자세한 내용은 `Get-Help Get-Date` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-115">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="fcfd7-116">두 번째 명령은 높은 심각도 및 회계의 태그 값을 저장하는 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-116">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="fcfd7-117">최종 명령은 ITSoftware라는 키를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-117">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="fcfd7-118">명령을 사용하면 키를 사용할 수 있으며, 만료 시간을 $Expires 시간으로 설정하고, 해당 키에 저장된 태그를 $Tags.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-118">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="fcfd7-119">예제 2: 모든 태그를 삭제하도록 키 수정</span><span class="sxs-lookup"><span data-stu-id="fcfd7-119">Example 2: Modify a key to delete all tags</span></span>
```powershell
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Version '394f9379a47a4e2086585468de6c7ae5' -Tag @{}

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 8:00:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="fcfd7-120">이 명령은 ITSoftware라는 키의 특정 버전에 대한 모든 태그를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-120">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="fcfd7-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fcfd7-121">PARAMETERS</span></span>

### <span data-ttu-id="fcfd7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcfd7-122">-DefaultProfile</span></span>
<span data-ttu-id="fcfd7-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcfd7-124">-사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="fcfd7-124">-Enable</span></span>
<span data-ttu-id="fcfd7-125">true 값을 사용하면 키와 false 값이 키를 사용하지 않도록 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-125">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="fcfd7-126">지정하지 않으면 기존 사용/사용 안 함 상태는 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-126">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcfd7-127">-만료</span><span class="sxs-lookup"><span data-stu-id="fcfd7-127">-Expires</span></span>
<span data-ttu-id="fcfd7-128">UTC 시간의 키의 만료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-128">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="fcfd7-129">지정하지 않으면 키의 기존 만료 시간은 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-129">If not specified, the existing expiration time of the key remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcfd7-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="fcfd7-130">-HsmName</span></span>
<span data-ttu-id="fcfd7-131">HSM 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-131">HSM name.</span></span> <span data-ttu-id="fcfd7-132">Cmdlet은 이름 및 현재 선택한 환경에 따라 관리되는 HSM의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractive
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcfd7-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcfd7-133">-InputObject</span></span>
<span data-ttu-id="fcfd7-134">키 개체</span><span class="sxs-lookup"><span data-stu-id="fcfd7-134">Key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcfd7-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="fcfd7-135">-KeyOps</span></span>
<span data-ttu-id="fcfd7-136">키를 사용하여 수행할 수 있는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-136">The operations that can be performed with the key.</span></span>
<span data-ttu-id="fcfd7-137">지정하지 않으면 키의 기존 키 작업은 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-137">If not specified, the existing key operations of the key remain unchanged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcfd7-138">-Name</span><span class="sxs-lookup"><span data-stu-id="fcfd7-138">-Name</span></span>
<span data-ttu-id="fcfd7-139">키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-139">Key name.</span></span>
<span data-ttu-id="fcfd7-140">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 키 이름의 키의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-140">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HsmInteractive
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcfd7-141">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="fcfd7-141">-NotBefore</span></span>
<span data-ttu-id="fcfd7-142">키를 사용할 수 없는 UTC 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-142">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="fcfd7-143">지정하지 않으면 키의 기존 NotBefore 특성은 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-143">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcfd7-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcfd7-144">-PassThru</span></span>
<span data-ttu-id="fcfd7-145">Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-145">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="fcfd7-146">이 스위치가 지정되어 있는 경우 업데이트된 키 번들 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-146">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="fcfd7-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="fcfd7-147">-Tag</span></span>
<span data-ttu-id="fcfd7-148">해시테이블은 키 태그를 나타내고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-148">A hashtable represents key tags.</span></span>
<span data-ttu-id="fcfd7-149">지정하지 않으면 키의 기존 태그는 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-149">If not specified, the existings tags of the key remain unchanged.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcfd7-150">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fcfd7-150">-VaultName</span></span>
<span data-ttu-id="fcfd7-151">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-151">Vault name.</span></span>
<span data-ttu-id="fcfd7-152">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-152">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcfd7-153">-Version</span><span class="sxs-lookup"><span data-stu-id="fcfd7-153">-Version</span></span>
<span data-ttu-id="fcfd7-154">키 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-154">Key version.</span></span>
<span data-ttu-id="fcfd7-155">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경, 키 이름 및 키 버전에서 키의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-155">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcfd7-156">-확인</span><span class="sxs-lookup"><span data-stu-id="fcfd7-156">-Confirm</span></span>
<span data-ttu-id="fcfd7-157">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcfd7-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcfd7-158">-WhatIf</span></span>
<span data-ttu-id="fcfd7-159">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcfd7-160">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcfd7-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcfd7-161">CommonParameters</span></span>
<span data-ttu-id="fcfd7-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fcfd7-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcfd7-163">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fcfd7-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcfd7-164">입력</span><span class="sxs-lookup"><span data-stu-id="fcfd7-164">INPUTS</span></span>

### <span data-ttu-id="fcfd7-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="fcfd7-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="fcfd7-166">출력</span><span class="sxs-lookup"><span data-stu-id="fcfd7-166">OUTPUTS</span></span>

### <span data-ttu-id="fcfd7-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fcfd7-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="fcfd7-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fcfd7-168">NOTES</span></span>

## <span data-ttu-id="fcfd7-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fcfd7-169">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: bfdd237ecadadae181d9e9dd3a201580537097f0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878470"
---
# <span data-ttu-id="44111-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="44111-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="44111-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44111-102">SYNOPSIS</span></span>
<span data-ttu-id="44111-103">키 볼트에서 키를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="44111-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="44111-104">구문과</span><span class="sxs-lookup"><span data-stu-id="44111-104">SYNTAX</span></span>

### <span data-ttu-id="44111-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="44111-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44111-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="44111-106">ByInputObject</span></span>
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44111-107">설명은</span><span class="sxs-lookup"><span data-stu-id="44111-107">DESCRIPTION</span></span>
<span data-ttu-id="44111-108">Remove-AzKeyVaultKey cmdlet은 키 자격 증명 모음에서 키를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="44111-108">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="44111-109">키를 실수로 삭제 한 경우 특정 ' 복구 ' 권한이 있는 사용자가 Undo-AzKeyVaultKeyRemoval를 사용 하 여 키를 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44111-109">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="44111-110">이 cmdlet의 값은 ' a/or **영향** ' 속성에 대해 high입니다.</span><span class="sxs-lookup"><span data-stu-id="44111-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="44111-111">예제의</span><span class="sxs-lookup"><span data-stu-id="44111-111">EXAMPLES</span></span>

### <span data-ttu-id="44111-112">예제 1: 키 보관소에서 키 제거</span><span class="sxs-lookup"><span data-stu-id="44111-112">Example 1: Remove a key from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -PassThru

Vault Name           : contoso
Name                 : key2
Id                   : https://contoso.vault.azure.net:443/keys/itsoftware/fdad15793ba0437e960497908ef9eb32
Deleted Date         : 5/24/2018 11:28:25 PM
Scheduled Purge Date : 8/22/2018 11:28:25 PM
Enabled              : False
Expires              : 10/11/2018 11:32:49 PM
Not Before           : 4/11/2018 11:22:49 PM
Created              : 4/12/2018 10:16:38 PM
Updated              : 4/12/2018 10:16:38 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="44111-113">이 명령은 Contoso 라는 키 보관소에서 ITSoftware 라는 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="44111-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="44111-114">예제 2: 사용자 확인 없이 키 제거</span><span class="sxs-lookup"><span data-stu-id="44111-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="44111-115">이 명령은 Contoso 라는 키 보관소에서 ITSoftware 라는 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="44111-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="44111-116">명령에서 *Force* 매개 변수를 지정 하므로 cmdlet이 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44111-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="44111-117">예제 3: 키 보관소에서 삭제 된 키를 영구적으로 제거</span><span class="sxs-lookup"><span data-stu-id="44111-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="44111-118">이 명령은 Contoso 라는 키 자격 증명 모음에서 ITSoftware 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="44111-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="44111-119">이 cmdlet을 실행 하려면 ' 제거 ' 권한이 필요 하며이 키 보관소에 대해 사용자에 게 명시적으로 부여 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="44111-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="44111-120">예제 4: 파이프라인 연산자를 사용 하 여 키 제거</span><span class="sxs-lookup"><span data-stu-id="44111-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="44111-121">이 명령은 Contoso 라는 키 보관소의 모든 키를 가져와 파이프라인 연산자를 사용 하 여 **Where-개체** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="44111-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="44111-122">해당 cmdlet은 **Enabled** 특성에 대 한 $False 값을 갖는 키를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="44111-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="44111-123">해당 cmdlet은 해당 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="44111-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="44111-124">변수</span><span class="sxs-lookup"><span data-stu-id="44111-124">PARAMETERS</span></span>

### <span data-ttu-id="44111-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44111-125">-DefaultProfile</span></span>
<span data-ttu-id="44111-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="44111-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44111-127">-Force</span><span class="sxs-lookup"><span data-stu-id="44111-127">-Force</span></span>
<span data-ttu-id="44111-128">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="44111-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="44111-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44111-129">-InputObject</span></span>
<span data-ttu-id="44111-130">KeyBundle 개체</span><span class="sxs-lookup"><span data-stu-id="44111-130">KeyBundle Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44111-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="44111-131">-InRemovedState</span></span>
<span data-ttu-id="44111-132">이전에 삭제 된 키를 영구적으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="44111-132">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="44111-133">-이름</span><span class="sxs-lookup"><span data-stu-id="44111-133">-Name</span></span>
<span data-ttu-id="44111-134">제거할 키의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44111-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="44111-135">이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 키의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="44111-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44111-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44111-136">-PassThru</span></span>
<span data-ttu-id="44111-137">이 cmdlet이 **Microsoft PSKeyVaultKey** 개체를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="44111-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="44111-138">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44111-138">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="44111-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="44111-139">-VaultName</span></span>
<span data-ttu-id="44111-140">키를 제거할 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44111-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="44111-141">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="44111-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44111-142">-확인</span><span class="sxs-lookup"><span data-stu-id="44111-142">-Confirm</span></span>
<span data-ttu-id="44111-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="44111-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44111-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44111-144">-WhatIf</span></span>
<span data-ttu-id="44111-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="44111-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44111-146">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="44111-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44111-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44111-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44111-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44111-148">CommonParameters</span></span>
<span data-ttu-id="44111-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44111-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44111-150">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="44111-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44111-151">입력</span><span class="sxs-lookup"><span data-stu-id="44111-151">INPUTS</span></span>

### <span data-ttu-id="44111-152">Microsoft. KeyVault. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="44111-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="44111-153">출력</span><span class="sxs-lookup"><span data-stu-id="44111-153">OUTPUTS</span></span>

### <span data-ttu-id="44111-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="44111-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="44111-155">상속자</span><span class="sxs-lookup"><span data-stu-id="44111-155">NOTES</span></span>

## <span data-ttu-id="44111-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44111-156">RELATED LINKS</span></span>

[<span data-ttu-id="44111-157">추가-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="44111-157">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="44111-158">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="44111-158">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="44111-159">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="44111-159">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

[<span data-ttu-id="44111-160">실행 취소-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="44111-160">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsmKey.md
ms.openlocfilehash: 79d01f96fe776432f650d827b16ba83f48b84ddd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219038"
---
# <span data-ttu-id="b31fb-101">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="b31fb-101">Update-AzManagedHsmKey</span></span>

## <span data-ttu-id="b31fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b31fb-102">SYNOPSIS</span></span>
<span data-ttu-id="b31fb-103">관리 되는 HSM에서 키의 특성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-103">Updates the attributes of a key in a managed HSM.</span></span>

## <span data-ttu-id="b31fb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b31fb-104">SYNTAX</span></span>

### <span data-ttu-id="b31fb-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b31fb-105">Default (Default)</span></span>
```
Update-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b31fb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b31fb-106">InputObject</span></span>
```
Update-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b31fb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b31fb-107">DESCRIPTION</span></span>
<span data-ttu-id="b31fb-108">**업데이트 AzManagedHsmKey** cmdlet은 관리 되는 HSM에서 키의 편집 가능한 특성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-108">The **Update-AzManagedHsmKey** cmdlet updates the editable attributes of a key in a managed HSM.</span></span>

## <span data-ttu-id="b31fb-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b31fb-109">EXAMPLES</span></span>

### <span data-ttu-id="b31fb-110">예제 1: 키를 수정 하 여 사용 하도록 설정 하 고 만료 날짜와 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzManagedHsmKey -HsmName testmhsm -Name testkey001 -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 49b74a39dab605bd336628dc094dc31b
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/49b74a39dab605bd336628dc094dc31b
Enabled        : True
Expires        : 10/14/2022 9:46:55 AM
Not Before     :
Created        : 10/14/2020 3:39:16 AM
Updated        : 10/14/2020 9:47:06 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="b31fb-111">첫 번째 명령은 **데이터 가져오기** cmdlet을 사용 하 여 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="b31fb-112">이 개체는 앞으로 2 년 동안 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="b31fb-113">이 명령은 $Expires 변수에 해당 날짜를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="b31fb-114">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="b31fb-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="b31fb-115">두 번째 명령은 높은 심각도와 계정의 태그 값을 저장 하는 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="b31fb-116">마지막 명령은 testkey001 이라는 키를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-116">The final command modifies a key named testkey001.</span></span> <span data-ttu-id="b31fb-117">이 명령은 키를 설정 하 고 만료 시간을 $Expires에 저장 된 시간으로 설정 하 고 $Tags에 저장 된 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

## <span data-ttu-id="b31fb-118">변수</span><span class="sxs-lookup"><span data-stu-id="b31fb-118">PARAMETERS</span></span>

### <span data-ttu-id="b31fb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b31fb-119">-DefaultProfile</span></span>
<span data-ttu-id="b31fb-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b31fb-121">-사용</span><span class="sxs-lookup"><span data-stu-id="b31fb-121">-Enable</span></span>
<span data-ttu-id="b31fb-122">True 값을 사용 하면 키와 false disabless 값이 키에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-122">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="b31fb-123">지정 하지 않으면 기존의 enabled/disabled 상태가 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-123">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="b31fb-124">-만료</span><span class="sxs-lookup"><span data-stu-id="b31fb-124">-Expires</span></span>
<span data-ttu-id="b31fb-125">UTC 시간 키의 만료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-125">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="b31fb-126">지정 하지 않은 경우 키의 기존 만료 시간은 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-126">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="b31fb-127">-HsmName</span><span class="sxs-lookup"><span data-stu-id="b31fb-127">-HsmName</span></span>
<span data-ttu-id="b31fb-128">HSM 이름.</span><span class="sxs-lookup"><span data-stu-id="b31fb-128">HSM name.</span></span> <span data-ttu-id="b31fb-129">Cmdlet은 이름 및 현재 선택 된 환경에 따라 관리 되는 HSM의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-129">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b31fb-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b31fb-130">-InputObject</span></span>
<span data-ttu-id="b31fb-131">Key 개체</span><span class="sxs-lookup"><span data-stu-id="b31fb-131">Key object</span></span>

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

### <span data-ttu-id="b31fb-132">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="b31fb-132">-KeyOps</span></span>
<span data-ttu-id="b31fb-133">키를 사용 하 여 수행할 수 있는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-133">The operations that can be performed with the key.</span></span>
<span data-ttu-id="b31fb-134">지정 하지 않으면 키의 기존 키 작업이 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-134">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="b31fb-135">-이름</span><span class="sxs-lookup"><span data-stu-id="b31fb-135">-Name</span></span>
<span data-ttu-id="b31fb-136">키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-136">Key name.</span></span>
<span data-ttu-id="b31fb-137">Cmdlet은 관리 되는 HSM 이름, 현재 선택 된 환경 및 키 이름에서 키의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-137">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b31fb-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="b31fb-138">-NotBefore</span></span>
<span data-ttu-id="b31fb-139">키를 사용할 수 없는 UTC 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-139">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="b31fb-140">지정 하지 않으면 키의 기존 NotBefore 특성이 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-140">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="b31fb-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b31fb-141">-PassThru</span></span>
<span data-ttu-id="b31fb-142">Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b31fb-143">이 스위치가 지정 된 경우 업데이트 된 키 번들 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-143">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="b31fb-144">태그</span><span class="sxs-lookup"><span data-stu-id="b31fb-144">-Tag</span></span>
<span data-ttu-id="b31fb-145">Hashtable는 키 태그를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-145">A hashtable represents key tags.</span></span>
<span data-ttu-id="b31fb-146">지정 하지 않으면 키의 existings 태그가 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-146">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="b31fb-147">-버전</span><span class="sxs-lookup"><span data-stu-id="b31fb-147">-Version</span></span>
<span data-ttu-id="b31fb-148">키 버전.</span><span class="sxs-lookup"><span data-stu-id="b31fb-148">Key version.</span></span>
<span data-ttu-id="b31fb-149">Cmdlet은 관리 되는 HSM 이름, 현재 선택 된 환경, 키 이름 및 키 버전에서 키의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-149">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="b31fb-150">-확인</span><span class="sxs-lookup"><span data-stu-id="b31fb-150">-Confirm</span></span>
<span data-ttu-id="b31fb-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b31fb-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b31fb-152">-WhatIf</span></span>
<span data-ttu-id="b31fb-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b31fb-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b31fb-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b31fb-155">CommonParameters</span></span>
<span data-ttu-id="b31fb-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b31fb-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b31fb-157">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b31fb-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b31fb-158">입력</span><span class="sxs-lookup"><span data-stu-id="b31fb-158">INPUTS</span></span>

### <span data-ttu-id="b31fb-159">Microsoft. KeyVault. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b31fb-159">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="b31fb-160">출력</span><span class="sxs-lookup"><span data-stu-id="b31fb-160">OUTPUTS</span></span>

### <span data-ttu-id="b31fb-161">Microsoft. KeyVault. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b31fb-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="b31fb-162">상속자</span><span class="sxs-lookup"><span data-stu-id="b31fb-162">NOTES</span></span>

## <span data-ttu-id="b31fb-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b31fb-163">RELATED LINKS</span></span>

[<span data-ttu-id="b31fb-164">추가-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="b31fb-164">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="b31fb-165">백업-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="b31fb-165">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="b31fb-166">제거-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="b31fb-166">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="b31fb-167">실행 취소-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="b31fb-167">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="b31fb-168">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="b31fb-168">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="b31fb-169">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="b31fb-169">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)
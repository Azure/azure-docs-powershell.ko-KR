---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmKey.md
ms.openlocfilehash: 38e0dbf124643a7d669c1787314790166e88f6a9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226919"
---
# <span data-ttu-id="7e4de-101">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="7e4de-101">Restore-AzManagedHsmKey</span></span>

## <span data-ttu-id="7e4de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e4de-102">SYNOPSIS</span></span>
<span data-ttu-id="7e4de-103">백업 된 키에서 관리 되는 HSM의 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7e4de-103">Creates a key in a managed HSM from a backed-up key.</span></span>

## <span data-ttu-id="7e4de-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e4de-104">SYNTAX</span></span>

### <span data-ttu-id="7e4de-105">ByHsmName (기본값)</span><span class="sxs-lookup"><span data-stu-id="7e4de-105">ByHsmName (Default)</span></span>
```
Restore-AzManagedHsmKey [-HsmName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e4de-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7e4de-106">ByInputObject</span></span>
```
Restore-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e4de-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7e4de-107">ByResourceId</span></span>
```
Restore-AzManagedHsmKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e4de-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7e4de-108">DESCRIPTION</span></span>
<span data-ttu-id="7e4de-109">**Restore-AzManagedHsmKey** cmdlet은 지정 된 관리 되는 HSM에서 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7e4de-109">The **Restore-AzManagedHsmKey** cmdlet creates a key in the specified managed HSM.</span></span>
<span data-ttu-id="7e4de-110">이 키는 입력 파일의 백업 키 복제본 이며 원래 키와 같은 이름을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="7e4de-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="7e4de-111">관리 되는 HSM에 같은 이름의 키가 이미 있으면 원본 키를 덮어쓰는 대신이 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e4de-111">If the managed HSM already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="7e4de-112">백업에 여러 버전의 키가 포함 되어 있으면 모든 버전이 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e4de-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="7e4de-113">키를 복원 하는 관리 되는 HSM은 해당 키를 백업한 관리 되는 HSM과 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e4de-113">The managed HSM that you restore the key into can be different from the managed HSM that you backed up the key from.</span></span>
<span data-ttu-id="7e4de-114">그러나 관리 되는 HSM은 동일한 구독을 사용 해야 하며 동일한 지리 (예: 북미)의 Azure 지역에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e4de-114">However, the managed HSM must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="7e4de-115"> https://azure.microsoft.com/support/trust-center/)Azure 지역을 지역에 매핑하는 Microsoft Azure 보안 센터를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7e4de-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="7e4de-116">예제의</span><span class="sxs-lookup"><span data-stu-id="7e4de-116">EXAMPLES</span></span>

### <span data-ttu-id="7e4de-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="7e4de-117">Example 1</span></span>
```powershell
PS C:\> Restore-AzManagedHsmKey -HsmName testmhsm -InputFile "C:\Backup.blob"

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 7cff8510da04433b98144a3e33ad2bae
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/7cff8510da04433b98144a3e33ad2bae
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 10:13:03 AM
Updated        : 10/14/2020 10:13:03 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="7e4de-118">이 명령은 Backup. a m a i a m a i m a의 모든 버전을 포함 하는 키를 testmhsm 이라는 관리 되는 HSM에 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e4de-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the managed HSM named testmhsm.</span></span>

## <span data-ttu-id="7e4de-119">변수</span><span class="sxs-lookup"><span data-stu-id="7e4de-119">PARAMETERS</span></span>

### <span data-ttu-id="7e4de-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e4de-120">-DefaultProfile</span></span>
<span data-ttu-id="7e4de-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e4de-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e4de-122">-HsmName</span><span class="sxs-lookup"><span data-stu-id="7e4de-122">-HsmName</span></span>
<span data-ttu-id="7e4de-123">HSM 이름.</span><span class="sxs-lookup"><span data-stu-id="7e4de-123">HSM name.</span></span> <span data-ttu-id="7e4de-124">Cmdlet은 이름 및 현재 선택 된 환경에 따라 관리 되는 HSM의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e4de-124">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHsmName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e4de-125">-InputFile</span><span class="sxs-lookup"><span data-stu-id="7e4de-125">-InputFile</span></span>
<span data-ttu-id="7e4de-126">입력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="7e4de-126">Input file.</span></span>
<span data-ttu-id="7e4de-127">백업 된 blob을 포함 하는 입력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="7e4de-127">The input file containing the backed-up blob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e4de-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e4de-128">-InputObject</span></span>
<span data-ttu-id="7e4de-129">HSM 개체</span><span class="sxs-lookup"><span data-stu-id="7e4de-129">HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4de-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e4de-130">-ResourceId</span></span>
<span data-ttu-id="7e4de-131">HSM 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="7e4de-131">HSM Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4de-132">-확인</span><span class="sxs-lookup"><span data-stu-id="7e4de-132">-Confirm</span></span>
<span data-ttu-id="7e4de-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e4de-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e4de-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e4de-134">-WhatIf</span></span>
<span data-ttu-id="7e4de-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7e4de-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e4de-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e4de-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e4de-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e4de-137">CommonParameters</span></span>
<span data-ttu-id="7e4de-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e4de-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e4de-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7e4de-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e4de-140">입력</span><span class="sxs-lookup"><span data-stu-id="7e4de-140">INPUTS</span></span>

### <span data-ttu-id="7e4de-141">Microsoft. KeyVault. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7e4de-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="7e4de-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7e4de-142">System.String</span></span>

## <span data-ttu-id="7e4de-143">출력</span><span class="sxs-lookup"><span data-stu-id="7e4de-143">OUTPUTS</span></span>

### <span data-ttu-id="7e4de-144">Microsoft. KeyVault. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7e4de-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="7e4de-145">상속자</span><span class="sxs-lookup"><span data-stu-id="7e4de-145">NOTES</span></span>

## <span data-ttu-id="7e4de-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e4de-146">RELATED LINKS</span></span>

[<span data-ttu-id="7e4de-147">추가-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="7e4de-147">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="7e4de-148">백업-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="7e4de-148">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="7e4de-149">제거-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="7e4de-149">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="7e4de-150">실행 취소-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="7e4de-150">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="7e4de-151">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="7e4de-151">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="7e4de-152">업데이트-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="7e4de-152">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)
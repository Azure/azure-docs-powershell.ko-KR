---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 958aeb36ba047284085d471f73aadad78b756839
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185532"
---
# <span data-ttu-id="75252-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75252-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="75252-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75252-102">SYNOPSIS</span></span>
<span data-ttu-id="75252-103">백업 키에서 키 자격 증명 모음에 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75252-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="75252-104">구문</span><span class="sxs-lookup"><span data-stu-id="75252-104">SYNTAX</span></span>

### <span data-ttu-id="75252-105">ByVaultName(기본값)</span><span class="sxs-lookup"><span data-stu-id="75252-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75252-106">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="75252-106">HsmByVaultName</span></span>
```
Restore-AzKeyVaultKey -HsmName <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75252-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="75252-107">ByInputObject</span></span>
```
Restore-AzKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75252-108">HsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="75252-108">HsmByInputObject</span></span>
```
Restore-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75252-109">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="75252-109">ByResourceId</span></span>
```
Restore-AzKeyVaultKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75252-110">HsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="75252-110">HsmByResourceId</span></span>
```
Restore-AzKeyVaultKey -HsmResourceId <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75252-111">설명</span><span class="sxs-lookup"><span data-stu-id="75252-111">DESCRIPTION</span></span>
<span data-ttu-id="75252-112">**Restore-AzKeyVaultKey** cmdlet은 지정된 키 자격 증명 모음에 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75252-112">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="75252-113">이 키는 입력 파일의 백업 키 복제본으로, 원래 키와 이름이 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="75252-113">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="75252-114">Key Vault에 동일한 이름의 키가 이미 있는 경우 이 cmdlet은 원래 키를 덮어써는 대신 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="75252-114">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="75252-115">백업에 여러 버전의 키가 포함되어 있는 경우 모든 버전이 복원됩니다.</span><span class="sxs-lookup"><span data-stu-id="75252-115">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="75252-116">키를 복원하는 키 자격 증명 모음은 키를 백업한 키 자격 증명 모음과 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75252-116">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="75252-117">그러나 Key Vault는 동일한 구독을 사용하며 동일한 지역(예: 북아메리카)의 Azure 지역에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75252-117">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="75252-118">Azure 지역을 지역에 매핑하는 경우 Microsoft Azure 보안 센터를 https://azure.microsoft.com/support/trust-center/) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="75252-118">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="75252-119">예제</span><span class="sxs-lookup"><span data-stu-id="75252-119">EXAMPLES</span></span>

### <span data-ttu-id="75252-120">예제 1: 백업 키 복원</span><span class="sxs-lookup"><span data-stu-id="75252-120">Example 1: Restore a backed-up key</span></span>
```powershell
PS C:\> Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Vault Name     : MyKeyVault
Name           : key1
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://mykeyvault.vault.azure.net:443/keys/key1/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        :
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 4/6/2018 11:35:04 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="75252-121">이 명령은 Backup.blob이라는 백업 파일에서 MyKeyVault라는 키 자격 증명 모음으로 모든 버전을 포함한 키를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="75252-121">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="75252-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75252-122">PARAMETERS</span></span>

### <span data-ttu-id="75252-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75252-123">-DefaultProfile</span></span>
<span data-ttu-id="75252-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="75252-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75252-125">-HsmName</span><span class="sxs-lookup"><span data-stu-id="75252-125">-HsmName</span></span>
<span data-ttu-id="75252-126">HSM 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75252-126">HSM name.</span></span> <span data-ttu-id="75252-127">Cmdlet은 이름 및 현재 선택한 환경에 따라 관리되는 HSM의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="75252-127">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75252-128">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="75252-128">-HsmObject</span></span>
<span data-ttu-id="75252-129">HSM 개체</span><span class="sxs-lookup"><span data-stu-id="75252-129">HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75252-130">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="75252-130">-HsmResourceId</span></span>
<span data-ttu-id="75252-131">Hsm 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="75252-131">Hsm Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75252-132">-InputFile</span><span class="sxs-lookup"><span data-stu-id="75252-132">-InputFile</span></span>
<span data-ttu-id="75252-133">복원할 키의 백업이 포함된 입력 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75252-133">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="75252-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75252-134">-InputObject</span></span>
<span data-ttu-id="75252-135">KeyVault 개체</span><span class="sxs-lookup"><span data-stu-id="75252-135">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75252-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75252-136">-ResourceId</span></span>
<span data-ttu-id="75252-137">KeyVault 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="75252-137">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="75252-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="75252-138">-VaultName</span></span>
<span data-ttu-id="75252-139">키를 복원할 키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75252-139">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="75252-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75252-140">-Confirm</span></span>
<span data-ttu-id="75252-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="75252-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75252-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75252-142">-WhatIf</span></span>
<span data-ttu-id="75252-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="75252-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75252-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75252-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75252-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75252-145">CommonParameters</span></span>
<span data-ttu-id="75252-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="75252-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75252-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="75252-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75252-148">입력</span><span class="sxs-lookup"><span data-stu-id="75252-148">INPUTS</span></span>

### <span data-ttu-id="75252-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="75252-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="75252-150">System.String</span><span class="sxs-lookup"><span data-stu-id="75252-150">System.String</span></span>

## <span data-ttu-id="75252-151">출력</span><span class="sxs-lookup"><span data-stu-id="75252-151">OUTPUTS</span></span>

### <span data-ttu-id="75252-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75252-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="75252-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="75252-153">NOTES</span></span>

## <span data-ttu-id="75252-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75252-154">RELATED LINKS</span></span>

[<span data-ttu-id="75252-155">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75252-155">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="75252-156">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75252-156">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="75252-157">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75252-157">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="75252-158">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75252-158">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)


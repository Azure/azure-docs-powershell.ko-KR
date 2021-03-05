---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDisk.md
ms.openlocfilehash: 1337482e880bca353e4824a00b73aef831db6b32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983328"
---
# <span data-ttu-id="00e26-101">New-AzDisk</span><span class="sxs-lookup"><span data-stu-id="00e26-101">New-AzDisk</span></span>

## <span data-ttu-id="00e26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00e26-102">SYNOPSIS</span></span>
<span data-ttu-id="00e26-103">관리 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00e26-103">Creates a managed disk.</span></span>

## <span data-ttu-id="00e26-104">구문</span><span class="sxs-lookup"><span data-stu-id="00e26-104">SYNTAX</span></span>

```
New-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00e26-105">설명</span><span class="sxs-lookup"><span data-stu-id="00e26-105">DESCRIPTION</span></span>
<span data-ttu-id="00e26-106">**New-AzDisk** cmdlet은 관리 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00e26-106">The **New-AzDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="00e26-107">예제</span><span class="sxs-lookup"><span data-stu-id="00e26-107">EXAMPLES</span></span>

### <span data-ttu-id="00e26-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="00e26-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="00e26-109">첫 번째 명령은 저장소 계정 유형에 크기가 5GB인 로컬 Standard_LRS 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00e26-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="00e26-110">또한 Windows OS 유형을 설정하고 암호화 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00e26-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="00e26-111">두 번째 및 세 번째 명령은 디스크 개체에 대한 디스크 암호화 키 및 키 암호화 키 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="00e26-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="00e26-112">마지막 명령은 디스크 개체를 사용하여 리소스 그룹 'ResourceGroup01'에서 'Disk01'의 이름이 있는 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00e26-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="00e26-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="00e26-113">Example 2</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $diskConfig.EncryptionSettingsCollection = New-Object Microsoft.Azure.Management.Compute.Models.EncryptionSettingsCollection

PS C:\> $encryptionSettingsElement1 = New-Object Microsoft.Azure.Management.Compute.Models.EncryptionSettingsElement
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey.SourceVault.Id = $disk_encryption_key_id_1
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey.SecretUrl = $disk_encryption_secret_url_1
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey.SourceVault.Id = $key_encryption_key_id_1
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey.KeyUrl = $key_encryption_key_url_1

PS C:\> $encryptionSettingsElement2 = New-Object Microsoft.Azure.Management.Compute.Models.EncryptionSettingsElement
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey.SourceVault.Id = $disk_encryption_key_id_2
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey.SecretUrl = $disk_encryption_secret_url_2
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey.SourceVault.Id = $key_encryption_key_id_2
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey.KeyUrl = $key_encryption_key_url_2

PS C:\> $diskConfig.EncryptionSettingsCollection.EncryptionSettings += $encryptionSettingsElement1
PS C:\> $diskConfig.EncryptionSettingsCollection.EncryptionSettings += $encryptionSettingsElement2
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="00e26-114">위의 명령은 두 개의 암호화 설정이 있는 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00e26-114">The above command creates a disk with two encryption settings.</span></span>

## <span data-ttu-id="00e26-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="00e26-115">PARAMETERS</span></span>

### <span data-ttu-id="00e26-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00e26-116">-AsJob</span></span>
<span data-ttu-id="00e26-117">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="00e26-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="00e26-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00e26-118">-DefaultProfile</span></span>
<span data-ttu-id="00e26-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00e26-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00e26-120">-Disk</span><span class="sxs-lookup"><span data-stu-id="00e26-120">-Disk</span></span>
<span data-ttu-id="00e26-121">로컬 디스크 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="00e26-121">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00e26-122">-DiskName</span><span class="sxs-lookup"><span data-stu-id="00e26-122">-DiskName</span></span>
<span data-ttu-id="00e26-123">디스크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="00e26-123">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00e26-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00e26-124">-ResourceGroupName</span></span>
<span data-ttu-id="00e26-125">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="00e26-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00e26-126">-확인</span><span class="sxs-lookup"><span data-stu-id="00e26-126">-Confirm</span></span>
<span data-ttu-id="00e26-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="00e26-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00e26-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00e26-128">-WhatIf</span></span>
<span data-ttu-id="00e26-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="00e26-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00e26-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00e26-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00e26-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00e26-131">CommonParameters</span></span>
<span data-ttu-id="00e26-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="00e26-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00e26-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00e26-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00e26-134">입력</span><span class="sxs-lookup"><span data-stu-id="00e26-134">INPUTS</span></span>

### <span data-ttu-id="00e26-135">System.String</span><span class="sxs-lookup"><span data-stu-id="00e26-135">System.String</span></span>

### <span data-ttu-id="00e26-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="00e26-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="00e26-137">출력</span><span class="sxs-lookup"><span data-stu-id="00e26-137">OUTPUTS</span></span>

### <span data-ttu-id="00e26-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="00e26-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="00e26-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="00e26-139">NOTES</span></span>

## <span data-ttu-id="00e26-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00e26-140">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: a738ec606fc982573c4062879e9da4becee43df2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496046"
---
# <span data-ttu-id="ad2c7-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="ad2c7-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="ad2c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad2c7-102">SYNOPSIS</span></span>
<span data-ttu-id="ad2c7-103">구성 가능한 디스크 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="ad2c7-104">구문</span><span class="sxs-lookup"><span data-stu-id="ad2c7-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-Tier <String>] [-DiskIOPSReadOnly <Int64>]
 [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad2c7-105">설명</span><span class="sxs-lookup"><span data-stu-id="ad2c7-105">DESCRIPTION</span></span>
<span data-ttu-id="ad2c7-106">**New-AzDiskUpdateConfig** cmdlet은 구성 가능한 디스크 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="ad2c7-107">예제</span><span class="sxs-lookup"><span data-stu-id="ad2c7-107">EXAMPLES</span></span>

### <span data-ttu-id="ad2c7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ad2c7-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="ad2c7-109">첫 번째 명령은 저장소 계정 유형에서 크기가 10GB인 로컬 빈 Premium_LRS 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="ad2c7-110">또한 Windows OS 유형을 설정하고 암호화 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="ad2c7-111">두 번째 및 세 번째 명령은 디스크 업데이트 개체에 대한 디스크 암호화 키 및 키 암호화 키 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="ad2c7-112">마지막 명령은 디스크 업데이트 개체를 사용하며 리소스 그룹 'ResourceGroup01'에서 'Disk01'으로 기존 디스크를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ad2c7-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="ad2c7-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="ad2c7-114">이 명령은 리소스 그룹 'ResourceGroup01'에서 이름이 'Disk01'인 기존 디스크를 10GB 디스크 크기로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="ad2c7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad2c7-115">PARAMETERS</span></span>

### <span data-ttu-id="ad2c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad2c7-116">-DefaultProfile</span></span>
<span data-ttu-id="ad2c7-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad2c7-118">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="ad2c7-118">-DiskAccessId</span></span>
<span data-ttu-id="ad2c7-119">{{ DiskAccessId 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="ad2c7-119">{{ Fill DiskAccessId Description }}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2c7-120">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ad2c7-120">-DiskEncryptionKey</span></span>
<span data-ttu-id="ad2c7-121">디스크의 디스크 암호화 키 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-121">Specifies the disk encryption key object on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2c7-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="ad2c7-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="ad2c7-123">미사용 암호화를 사용하도록 설정하는 데 사용할 디스크 암호화 집합의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-123">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2c7-124">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="ad2c7-124">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="ad2c7-125">공유 디스크를 ReadOnly로 탑재하는 모든 VM에서 허용되는 총 IOPS 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-125">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="ad2c7-126">하나의 작업은 4k에서 256k bytes 사이를 전송할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-126">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2c7-127">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="ad2c7-127">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="ad2c7-128">이 디스크에 허용되는 IOPS 수입니다. UltraSSD 디스크에만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-128">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="ad2c7-129">하나의 작업은 4k에서 256k bytes 사이를 전송할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-129">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2c7-130">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="ad2c7-130">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="ad2c7-131">공유 디스크를 ReadOnly로 탑재하는 모든 VM에서 허용되는 총 데이터량(MBps)입니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-131">The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="ad2c7-132">MBps는 초당 수백만의 byte를 의미합니다. 여기서 MB는 10의 거버전의 ISO 의미를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-132">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2c7-133">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="ad2c7-133">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="ad2c7-134">이 디스크에 허용되는 대역폭입니다. UltraSSD 디스크에만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-134">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="ad2c7-135">MBps는 초당 수백만의 byte를 의미합니다. 여기서 MB는 10의 거버전의 ISO 의미를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-135">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2c7-136">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="ad2c7-136">-DiskSizeGB</span></span>
<span data-ttu-id="ad2c7-137">디스크 크기를 GB로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-137">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2c7-138">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="ad2c7-138">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="ad2c7-139">암호화 설정을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="ad2c7-139">Enable encryption settings.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2c7-140">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="ad2c7-140">-EncryptionType</span></span>
<span data-ttu-id="ad2c7-141">디스크의 데이터를 암호화하는 데 사용되는 키 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-141">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="ad2c7-142">사용 가능한 값은 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'입니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-142">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2c7-143">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ad2c7-143">-KeyEncryptionKey</span></span>
<span data-ttu-id="ad2c7-144">디스크의 키 암호화 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-144">Specifies the Key encryption key on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2c7-145">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="ad2c7-145">-MaxSharesCount</span></span>
<span data-ttu-id="ad2c7-146">디스크에 동시에 연결할 수 있는 최대 VM 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-146">The maximum number of VMs that can attach to the disk at the same time.</span></span> <span data-ttu-id="ad2c7-147">두 개 이상의 값은 여러 VM에 동시에 탑재할 수 있는 디스크를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-147">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2c7-148">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ad2c7-148">-NetworkAccessPolicy</span></span>
<span data-ttu-id="ad2c7-149">{{ NetworkAccessPolicy 설명 }} 채우기</span><span class="sxs-lookup"><span data-stu-id="ad2c7-149">{{ Fill NetworkAccessPolicy Description }}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2c7-150">-OsType</span><span class="sxs-lookup"><span data-stu-id="ad2c7-150">-OsType</span></span>
<span data-ttu-id="ad2c7-151">OS 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-151">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2c7-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ad2c7-152">-SkuName</span></span>
<span data-ttu-id="ad2c7-153">저장소 계정의 SKU 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-153">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="ad2c7-154">사용 가능한 값은 Standard_LRS, Premium_LRS, StandardSSD_LRS 및 UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-154">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="ad2c7-155">UltraSSD_LRS CreateOption 매개 변수에 대한 빈 값과 함께 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-155">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2c7-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="ad2c7-156">-Tag</span></span>
<span data-ttu-id="ad2c7-157">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-157">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ad2c7-158">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="ad2c7-158">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2c7-159">-Tier</span><span class="sxs-lookup"><span data-stu-id="ad2c7-159">-Tier</span></span>
<span data-ttu-id="ad2c7-160">디스크의 성능 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-160">Performance tier of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2c7-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad2c7-161">-Confirm</span></span>
<span data-ttu-id="ad2c7-162">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad2c7-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad2c7-163">-WhatIf</span></span>
<span data-ttu-id="ad2c7-164">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ad2c7-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad2c7-165">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad2c7-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad2c7-166">CommonParameters</span></span>
<span data-ttu-id="ad2c7-167">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad2c7-168">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ad2c7-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad2c7-169">입력</span><span class="sxs-lookup"><span data-stu-id="ad2c7-169">INPUTS</span></span>

### <span data-ttu-id="ad2c7-170">System.String</span><span class="sxs-lookup"><span data-stu-id="ad2c7-170">System.String</span></span>

### <span data-ttu-id="ad2c7-171">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ad2c7-171">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ad2c7-172">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ad2c7-172">System.Int32</span></span>

### <span data-ttu-id="ad2c7-173">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ad2c7-173">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ad2c7-174">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ad2c7-174">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ad2c7-175">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="ad2c7-175">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="ad2c7-176">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="ad2c7-176">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="ad2c7-177">출력</span><span class="sxs-lookup"><span data-stu-id="ad2c7-177">OUTPUTS</span></span>

### <span data-ttu-id="ad2c7-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="ad2c7-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="ad2c7-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ad2c7-179">NOTES</span></span>

## <span data-ttu-id="ad2c7-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad2c7-180">RELATED LINKS</span></span>

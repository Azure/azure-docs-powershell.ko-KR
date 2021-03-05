---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 8407cb1f8968d1e7d9e469b4ca3ccd1cb49742a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007104"
---
# <span data-ttu-id="14773-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="14773-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="14773-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14773-102">SYNOPSIS</span></span>
<span data-ttu-id="14773-103">구성 가능한 스냅숏 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14773-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="14773-104">구문</span><span class="sxs-lookup"><span data-stu-id="14773-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Incremental] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14773-105">설명</span><span class="sxs-lookup"><span data-stu-id="14773-105">DESCRIPTION</span></span>
<span data-ttu-id="14773-106">**New-AzSnapshotConfig** cmdlet은 구성 가능한 스냅숏 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14773-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="14773-107">예제</span><span class="sxs-lookup"><span data-stu-id="14773-107">EXAMPLES</span></span>

### <span data-ttu-id="14773-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="14773-108">Example 1</span></span>
```powershell
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="14773-109">첫 번째 명령은 저장소 계정 유형에 크기가 5GB인 로컬 빈 스냅숏 개체를 Standard_LRS 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14773-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="14773-110">또한 Windows OS 유형을 설정하고 암호화 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14773-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="14773-111">두 번째 및 세 번째 명령은 스냅숏 개체에 대한 디스크 암호화 키 및 키 암호화 키 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="14773-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="14773-112">마지막 명령은 스냅숏 개체를 만들고 리소스 그룹 'ResourceGroup01'에서 '스냅숏01'을 사용하여 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14773-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="14773-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="14773-113">Example 2</span></span>

<span data-ttu-id="14773-114">구성 가능한 스냅숏 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14773-114">Creates a configurable snapshot object.</span></span> <span data-ttu-id="14773-115">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="14773-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzSnapshotConfig -CreateOption Empty -Location 'Central US' -SourceUri 'https://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd'
```

## <span data-ttu-id="14773-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="14773-116">PARAMETERS</span></span>

### <span data-ttu-id="14773-117">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="14773-117">-CreateOption</span></span>
<span data-ttu-id="14773-118">이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만들고, 빈 디스크를 생성하거나, 기존 디스크를 연결하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14773-118">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="14773-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14773-119">-DefaultProfile</span></span>
<span data-ttu-id="14773-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14773-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14773-121">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="14773-121">-DiskEncryptionKey</span></span>
<span data-ttu-id="14773-122">스냅숏에서 디스크 암호화 키 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14773-122">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="14773-123">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="14773-123">-DiskEncryptionSetId</span></span>
<span data-ttu-id="14773-124">미사용 암호화를 사용하도록 설정하는 데 사용할 디스크 암호화 집합의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14773-124">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="14773-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="14773-125">-DiskSizeGB</span></span>
<span data-ttu-id="14773-126">디스크 크기를 GB로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14773-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="14773-127">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="14773-127">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="14773-128">암호화 설정을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="14773-128">Enable encryption settings.</span></span>

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

### <span data-ttu-id="14773-129">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="14773-129">-EncryptionType</span></span>
<span data-ttu-id="14773-130">디스크의 데이터를 암호화하는 데 사용되는 키 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="14773-130">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="14773-131">사용 가능한 값은 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'입니다.</span><span class="sxs-lookup"><span data-stu-id="14773-131">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="14773-132">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="14773-132">-DiskAccessId</span></span>
<span data-ttu-id="14773-133">개인 엔드포인트를 ARM DiskAccess 리소스의 id를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="14773-133">Gets or sets ARM id of the DiskAccess resource for using private endpoints on.</span></span>

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

### <span data-ttu-id="14773-134">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="14773-134">-NetworkAccessPolicy</span></span>
<span data-ttu-id="14773-135">네트워크 액세스 정책은 네트워크 액세스 정책을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="14773-135">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="14773-136">가능한 값은 다음과 같습니다. 'AllowAll', 'AllowPrivate', 'DenyAll'</span><span class="sxs-lookup"><span data-stu-id="14773-136">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="14773-137">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="14773-137">-HyperVGeneration</span></span>
<span data-ttu-id="14773-138">Virtual Machine의 하이퍼바이서 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="14773-138">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="14773-139">OS 디스크에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14773-139">Applicable to OS disks only.</span></span>  <span data-ttu-id="14773-140">허용되는 값은 V1 및 V2입니다.</span><span class="sxs-lookup"><span data-stu-id="14773-140">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="14773-141">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="14773-141">-ImageReference</span></span>
<span data-ttu-id="14773-142">스냅숏에서 이미지 참조를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14773-142">Specifies the image reference on a snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14773-143">-증분</span><span class="sxs-lookup"><span data-stu-id="14773-143">-Incremental</span></span>
<span data-ttu-id="14773-144">증분 스냅숏을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14773-144">Specifies an incremental snapshot.</span></span> <span data-ttu-id="14773-145">동일한 디스크의 증분 스냅숏은 전체 스냅숏보다 공간을 적게 차지하며, 확산될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14773-145">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14773-146">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="14773-146">-KeyEncryptionKey</span></span>
<span data-ttu-id="14773-147">스냅숏의 키 암호화 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14773-147">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="14773-148">-Location</span><span class="sxs-lookup"><span data-stu-id="14773-148">-Location</span></span>
<span data-ttu-id="14773-149">위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14773-149">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14773-150">-OsType</span><span class="sxs-lookup"><span data-stu-id="14773-150">-OsType</span></span>
<span data-ttu-id="14773-151">OS 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14773-151">Specifies the OS type.</span></span>

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

### <span data-ttu-id="14773-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="14773-152">-SkuName</span></span>
<span data-ttu-id="14773-153">저장소 계정의 Sku 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14773-153">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="14773-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="14773-154">-SourceResourceId</span></span>
<span data-ttu-id="14773-155">원본 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14773-155">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="14773-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="14773-156">-SourceUri</span></span>
<span data-ttu-id="14773-157">원본 Uri를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14773-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="14773-158">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="14773-158">-StorageAccountId</span></span>
<span data-ttu-id="14773-159">저장소 계정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14773-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="14773-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="14773-160">-Tag</span></span>
<span data-ttu-id="14773-161">해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="14773-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="14773-162">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="14773-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14773-163">-확인</span><span class="sxs-lookup"><span data-stu-id="14773-163">-Confirm</span></span>
<span data-ttu-id="14773-164">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="14773-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14773-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14773-165">-WhatIf</span></span>
<span data-ttu-id="14773-166">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="14773-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14773-167">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14773-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14773-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14773-168">CommonParameters</span></span>
<span data-ttu-id="14773-169">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="14773-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14773-170">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14773-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14773-171">입력</span><span class="sxs-lookup"><span data-stu-id="14773-171">INPUTS</span></span>

### <span data-ttu-id="14773-172">System.String</span><span class="sxs-lookup"><span data-stu-id="14773-172">System.String</span></span>

### <span data-ttu-id="14773-173">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="14773-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="14773-174">System.Int32</span><span class="sxs-lookup"><span data-stu-id="14773-174">System.Int32</span></span>

### <span data-ttu-id="14773-175">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="14773-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="14773-176">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="14773-176">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="14773-177">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="14773-177">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="14773-178">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="14773-178">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="14773-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="14773-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="14773-180">출력</span><span class="sxs-lookup"><span data-stu-id="14773-180">OUTPUTS</span></span>

### <span data-ttu-id="14773-181">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="14773-181">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="14773-182">참고 사항</span><span class="sxs-lookup"><span data-stu-id="14773-182">NOTES</span></span>

## <span data-ttu-id="14773-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14773-183">RELATED LINKS</span></span>

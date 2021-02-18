---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 12ebf45a0428b170f40edce6129d76dd7fcbd601
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181641"
---
# <span data-ttu-id="a5166-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="a5166-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="a5166-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5166-102">SYNOPSIS</span></span>
<span data-ttu-id="a5166-103">구성 가능한 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="a5166-104">구문</span><span class="sxs-lookup"><span data-stu-id="a5166-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [-Tier <String>] [-LogicalSectorSize <Int32>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Location] <String>]
 [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>]
 [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-Tag <Hashtable>]
 [-CreateOption <String>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-BurstingEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5166-105">설명</span><span class="sxs-lookup"><span data-stu-id="a5166-105">DESCRIPTION</span></span>
<span data-ttu-id="a5166-106">**New-AzDiskConfig** cmdlet은 구성 가능한 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="a5166-107">예제</span><span class="sxs-lookup"><span data-stu-id="a5166-107">EXAMPLES</span></span>

### <span data-ttu-id="a5166-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a5166-108">Example 1</span></span>
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

<span data-ttu-id="a5166-109">첫 번째 명령은 저장소 계정 유형에 크기가 5GB인 로컬 빈 Standard_LRS 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="a5166-110">또한 Windows OS 유형을 설정하고 암호화 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="a5166-111">두 번째 및 세 번째 명령은 디스크 개체에 대한 디스크 암호화 키 및 키 암호화 키 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="a5166-112">마지막 명령은 디스크 개체를 사용하며 리소스 그룹 'ResourceGroup01'에 'Disk01'으로 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="a5166-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="a5166-113">Example 2</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
PS C:\> $diskSas = Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DurationInSecond 86400 -Access 'Write'
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ReadyToUpload'
PS C:\> AzCopy /Source:https://myaccount.blob.core.windows.net/mycontainer1 /Dest:$diskSas
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ActiveUpload'
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="a5166-114">첫 번째 명령은 업로드를 위한 로컬 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="a5166-115">두 번째 명령은 디스크 개체를 사용하며 리소스 그룹 'ResourceGroup01'에 'Disk01'으로 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="a5166-116">세 번째 명령은 디스크에 대한 SAS URL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="a5166-117">네 번째 명령은 디스크의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="a5166-118">디스크 상태가 'ReadyToUpload'인 경우 사용자는 AzCopy를 사용하여 Blob Storage에서 디스크 SAS URL로 디스크를 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="a5166-119">업로드하는 동안 디스크 상태가 'ActiveUpload'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="a5166-120">마지막 명령은 SAS URL에 대한 디스크 액세스를 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="a5166-121">예제 3</span><span class="sxs-lookup"><span data-stu-id="a5166-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="a5166-122">공유 갤러리 이미지 버전에서 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="a5166-123">ID는 공유 갤러리 이미지 버전의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="a5166-124">원본이 데이터 디스크인 경우 Lun이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="a5166-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5166-125">PARAMETERS</span></span>

### <span data-ttu-id="a5166-126">-BurstingEnabled</span><span class="sxs-lookup"><span data-stu-id="a5166-126">-BurstingEnabled</span></span>
<span data-ttu-id="a5166-127">디스크의 프로비전된 성능 목표 이상으로 버스팅을 가능하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-127">Enables bursting beyond the provisioned performance target of the disk.</span></span> <span data-ttu-id="a5166-128">버스팅은 기본적으로 사용하지 않도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-128">Bursting is disabled by default.</span></span> <span data-ttu-id="a5166-129">Ultra 디스크에는 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-129">Does not apply to Ultra disks.</span></span>

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

### <span data-ttu-id="a5166-130">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="a5166-130">-CreateOption</span></span>
<span data-ttu-id="a5166-131">이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만드는지, 빈 디스크를 만드는지 또는 기존 디스크를 연결할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-131">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="a5166-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5166-132">-DefaultProfile</span></span>
<span data-ttu-id="a5166-133">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5166-134">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="a5166-134">-DiskAccessId</span></span>
<span data-ttu-id="a5166-135">개인 엔드포인트를 ARM DiskAccess 리소스의 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-135">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="a5166-136">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a5166-136">-DiskEncryptionKey</span></span>
<span data-ttu-id="a5166-137">디스크의 디스크 암호화 키 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-137">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="a5166-138">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="a5166-138">-DiskEncryptionSetId</span></span>
<span data-ttu-id="a5166-139">미사용 암호화를 사용하도록 설정하는 데 사용할 디스크 암호화 집합의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-139">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="a5166-140">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="a5166-140">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="a5166-141">공유 디스크를 ReadOnly로 탑재하는 모든 VM에서 허용되는 총 IOPS 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-141">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="a5166-142">한 작업은 4k에서 256k bytes 사이를 전송할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-142">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5166-143">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="a5166-143">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="a5166-144">이 디스크에 허용되는 IOPS 수입니다. UltraSSD 디스크에만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-144">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="a5166-145">한 작업은 4k에서 256k bytes 사이를 전송할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-145">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5166-146">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="a5166-146">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="a5166-147">"description": "공유 디스크를 ReadOnly로 탑재하는 모든 VM에서 허용되는 총 MBps(총 데이터량)입니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-147">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="a5166-148">MBps는 초당 수백만의 byte를 의미합니다. 여기서 MB는 10의 거버전의 ISO 의미를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-148">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5166-149">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="a5166-149">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="a5166-150">이 디스크에 허용되는 대역폭입니다. UltraSSD 디스크에만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-150">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="a5166-151">MBps는 초당 수백만의 byte를 의미합니다. 여기서 MB는 10의 거버전의 ISO 의미를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-151">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5166-152">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="a5166-152">-DiskSizeGB</span></span>
<span data-ttu-id="a5166-153">디스크 크기를 GB로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-153">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="a5166-154">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="a5166-154">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="a5166-155">암호화 설정을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="a5166-155">Enable encryption settings.</span></span>

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

### <span data-ttu-id="a5166-156">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="a5166-156">-EncryptionType</span></span>
<span data-ttu-id="a5166-157">디스크의 데이터를 암호화하는 데 사용되는 키 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-157">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="a5166-158">사용 가능한 값은 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'입니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-158">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="a5166-159">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="a5166-159">-GalleryImageReference</span></span>
<span data-ttu-id="a5166-160">GalleryImageReference 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-160">The GalleryImageReference object.</span></span>  <span data-ttu-id="a5166-161">갤러리 이미지에서 만드는 경우 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-161">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="a5166-162">ID는 디스크를 ARM 공유 galley 이미지 버전의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-162">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="a5166-163">복사 원본이 갤러리 이미지의 데이터 디스크 중 하나인 경우 lun이 필요합니다. null이면 이미지의 OS 디스크가 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-163">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

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

### <span data-ttu-id="a5166-164">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="a5166-164">-HyperVGeneration</span></span>
<span data-ttu-id="a5166-165">Virtual Machine의 하이퍼바이서 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-165">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="a5166-166">OS 디스크에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-166">Applicable to OS disks only.</span></span>  <span data-ttu-id="a5166-167">허용되는 값은 V1 및 V2입니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-167">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="a5166-168">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="a5166-168">-ImageReference</span></span>
<span data-ttu-id="a5166-169">디스크의 이미지 참조를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-169">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="a5166-170">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a5166-170">-KeyEncryptionKey</span></span>
<span data-ttu-id="a5166-171">디스크의 키 암호화 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-171">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="a5166-172">-Location</span><span class="sxs-lookup"><span data-stu-id="a5166-172">-Location</span></span>
<span data-ttu-id="a5166-173">위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-173">Specifies a location.</span></span>

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

### <span data-ttu-id="a5166-174">-LogicalSectorSize</span><span class="sxs-lookup"><span data-stu-id="a5166-174">-LogicalSectorSize</span></span>
<span data-ttu-id="a5166-175">Ultra 디스크에 대한 논리 섹터 크기(byte)입니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-175">Logical sector size in bytes for Ultra disks.</span></span> 

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

### <span data-ttu-id="a5166-176">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="a5166-176">-MaxSharesCount</span></span>
<span data-ttu-id="a5166-177">디스크에 동시에 연결할 수 있는 최대 VM 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-177">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="a5166-178">두 개보다 큰 값은 여러 VM에 동시에 탑재할 수 있는 디스크를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-178">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="a5166-179">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a5166-179">-NetworkAccessPolicy</span></span>
<span data-ttu-id="a5166-180">네트워크 액세스 정책은 네트워크 액세스 정책을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-180">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="a5166-181">가능한 값은 'AllowAll', 'AllowPrivate', 'DenyAll'입니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-181">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="a5166-182">-OsType</span><span class="sxs-lookup"><span data-stu-id="a5166-182">-OsType</span></span>
<span data-ttu-id="a5166-183">OS 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-183">Specifies the OS type.</span></span>

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

### <span data-ttu-id="a5166-184">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a5166-184">-SkuName</span></span>
<span data-ttu-id="a5166-185">저장소 계정의 SKU 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-185">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="a5166-186">사용 가능한 값은 Standard_LRS, Premium_LRS, StandardSSD_LRS 및 UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="a5166-186">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="a5166-187">UltraSSD_LRS CreateOption 매개 변수에 대한 빈 값과 함께 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-187">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="a5166-188">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="a5166-188">-SourceResourceId</span></span>
<span data-ttu-id="a5166-189">원본 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-189">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="a5166-190">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="a5166-190">-SourceUri</span></span>
<span data-ttu-id="a5166-191">원본 Uri를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-191">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="a5166-192">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a5166-192">-StorageAccountId</span></span>
<span data-ttu-id="a5166-193">저장소 계정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-193">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="a5166-194">-Tag</span><span class="sxs-lookup"><span data-stu-id="a5166-194">-Tag</span></span>
<span data-ttu-id="a5166-195">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-195">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a5166-196">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="a5166-196">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a5166-197">-Tier</span><span class="sxs-lookup"><span data-stu-id="a5166-197">-Tier</span></span>
<span data-ttu-id="a5166-198">디스크의 성능 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-198">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="a5166-199">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="a5166-199">-UploadSizeInBytes</span></span>
<span data-ttu-id="a5166-200">CreateOption이 업로드 중일 때 VHD 발판을 포함하여 업로드 내용의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-200">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="a5166-201">이 값은 20972032(VHD 발판의 경우 20 MiB + 512비트)와 35183298347520비트(VHD의 경우 32 TiB + 512비트)입니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-201">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5166-202">-Zone</span><span class="sxs-lookup"><span data-stu-id="a5166-202">-Zone</span></span>
<span data-ttu-id="a5166-203">디스크에 대한 논리 영역 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-203">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5166-204">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5166-204">-Confirm</span></span>
<span data-ttu-id="a5166-205">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5166-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5166-206">-WhatIf</span></span>
<span data-ttu-id="a5166-207">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a5166-207">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5166-208">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5166-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5166-209">CommonParameters</span></span>
<span data-ttu-id="a5166-210">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a5166-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5166-211">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a5166-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5166-212">입력</span><span class="sxs-lookup"><span data-stu-id="a5166-212">INPUTS</span></span>

### <span data-ttu-id="a5166-213">System.String</span><span class="sxs-lookup"><span data-stu-id="a5166-213">System.String</span></span>

### <span data-ttu-id="a5166-214">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a5166-214">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="a5166-215">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a5166-215">System.Int32</span></span>

### <span data-ttu-id="a5166-216">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a5166-216">System.String[]</span></span>

### <span data-ttu-id="a5166-217">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a5166-217">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a5166-218">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="a5166-218">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="a5166-219">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a5166-219">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a5166-220">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="a5166-220">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="a5166-221">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="a5166-221">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="a5166-222">출력</span><span class="sxs-lookup"><span data-stu-id="a5166-222">OUTPUTS</span></span>

### <span data-ttu-id="a5166-223">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="a5166-223">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="a5166-224">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a5166-224">NOTES</span></span>

## <span data-ttu-id="a5166-225">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5166-225">RELATED LINKS</span></span>

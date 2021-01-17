---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: ec4d0444ad88fa7536fbf1ee050dc8dcb6a76af3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340622"
---
# <span data-ttu-id="1f7c3-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="1f7c3-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="1f7c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f7c3-102">SYNOPSIS</span></span>
<span data-ttu-id="1f7c3-103">구성 가능한 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="1f7c3-104">구문</span><span class="sxs-lookup"><span data-stu-id="1f7c3-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [-Tier <String>] [-LogicalSectorSize <Int32>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>]
 [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>]
 [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-Tag <Hashtable>]
 [-CreateOption <String>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f7c3-105">설명</span><span class="sxs-lookup"><span data-stu-id="1f7c3-105">DESCRIPTION</span></span>
<span data-ttu-id="1f7c3-106">**New-AzDiskConfig** cmdlet은 구성 가능한 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="1f7c3-107">예제</span><span class="sxs-lookup"><span data-stu-id="1f7c3-107">EXAMPLES</span></span>

### <span data-ttu-id="1f7c3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1f7c3-108">Example 1</span></span>
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

<span data-ttu-id="1f7c3-109">첫 번째 명령은 저장소 계정 유형에 크기가 5GB인 로컬 빈 Standard_LRS 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="1f7c3-110">또한 Windows OS 유형을 설정하고 암호화 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="1f7c3-111">두 번째 및 세 번째 명령은 디스크 개체에 대한 디스크 암호화 키 및 키 암호화 키 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="1f7c3-112">마지막 명령은 디스크 개체를 사용하며 리소스 그룹 'ResourceGroup01'에 'Disk01'으로 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="1f7c3-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="1f7c3-113">Example 2</span></span>
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

<span data-ttu-id="1f7c3-114">첫 번째 명령은 업로드를 위한 로컬 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="1f7c3-115">두 번째 명령은 디스크 개체를 사용하며 리소스 그룹 'ResourceGroup01'에 'Disk01'으로 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="1f7c3-116">세 번째 명령은 디스크에 대한 SAS URL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="1f7c3-117">네 번째 명령은 디스크의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="1f7c3-118">디스크 상태가 'ReadyToUpload'인 경우 사용자는 AzCopy를 사용하여 Blob Storage에서 디스크 SAS URL로 디스크를 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="1f7c3-119">업로드하는 동안 디스크 상태가 'ActiveUpload'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="1f7c3-120">마지막 명령은 SAS URL에 대한 디스크 액세스를 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="1f7c3-121">예제 3</span><span class="sxs-lookup"><span data-stu-id="1f7c3-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="1f7c3-122">공유 갤러리 이미지 버전에서 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="1f7c3-123">ID는 공유 갤러리 이미지 버전의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="1f7c3-124">원본이 데이터 디스크인 경우 Lun이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="1f7c3-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f7c3-125">PARAMETERS</span></span>

### <span data-ttu-id="1f7c3-126">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="1f7c3-126">-CreateOption</span></span>
<span data-ttu-id="1f7c3-127">이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만드는지, 빈 디스크를 만드는지 또는 기존 디스크를 연결할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-127">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="1f7c3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f7c3-128">-DefaultProfile</span></span>
<span data-ttu-id="1f7c3-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f7c3-130">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="1f7c3-130">-DiskAccessId</span></span>
<span data-ttu-id="1f7c3-131">개인 엔드포인트를 ARM DiskAccess 리소스의 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-131">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="1f7c3-132">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1f7c3-132">-DiskEncryptionKey</span></span>
<span data-ttu-id="1f7c3-133">디스크의 디스크 암호화 키 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-133">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="1f7c3-134">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="1f7c3-134">-DiskEncryptionSetId</span></span>
<span data-ttu-id="1f7c3-135">미사용 암호화를 사용하도록 설정하는 데 사용할 디스크 암호화 집합의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-135">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="1f7c3-136">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="1f7c3-136">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="1f7c3-137">공유 디스크를 ReadOnly로 탑재하는 모든 VM에서 허용되는 총 IOPS 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-137">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="1f7c3-138">하나의 작업은 4k에서 256k bytes 사이를 전송할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-138">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="1f7c3-139">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="1f7c3-139">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="1f7c3-140">이 디스크에 허용되는 IOPS 수입니다. UltraSSD 디스크에만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-140">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="1f7c3-141">하나의 작업은 4k에서 256k bytes 사이를 전송할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-141">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="1f7c3-142">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="1f7c3-142">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="1f7c3-143">"description": "공유 디스크를 ReadOnly로 탑재하는 모든 VM에서 허용되는 총 MBps(총 데이터량)입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-143">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="1f7c3-144">MBps는 초당 수백만의 byte를 의미합니다. 여기서 MB는 10의 거버전의 ISO 의미를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-144">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="1f7c3-145">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="1f7c3-145">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="1f7c3-146">이 디스크에 허용되는 대역폭입니다. UltraSSD 디스크에만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-146">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="1f7c3-147">MBps는 초당 수백만의 byte를 의미합니다. 여기서 MB는 10의 거버전의 ISO 의미를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-147">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="1f7c3-148">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="1f7c3-148">-DiskSizeGB</span></span>
<span data-ttu-id="1f7c3-149">디스크 크기를 GB로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-149">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="1f7c3-150">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="1f7c3-150">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="1f7c3-151">암호화 설정을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="1f7c3-151">Enable encryption settings.</span></span>

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

### <span data-ttu-id="1f7c3-152">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="1f7c3-152">-EncryptionType</span></span>
<span data-ttu-id="1f7c3-153">디스크의 데이터를 암호화하는 데 사용되는 키 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-153">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="1f7c3-154">사용 가능한 값은 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-154">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="1f7c3-155">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="1f7c3-155">-GalleryImageReference</span></span>
<span data-ttu-id="1f7c3-156">GalleryImageReference 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-156">The GalleryImageReference object.</span></span>  <span data-ttu-id="1f7c3-157">갤러리 이미지에서 만드는 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-157">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="1f7c3-158">ID는 디스크를 ARM 공유 galley 이미지 버전의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-158">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="1f7c3-159">복사 원본이 갤러리 이미지의 데이터 디스크 중 하나인 경우 lun이 필요합니다. null이면 이미지의 OS 디스크가 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-159">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

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

### <span data-ttu-id="1f7c3-160">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="1f7c3-160">-HyperVGeneration</span></span>
<span data-ttu-id="1f7c3-161">Virtual Machine의 하이퍼바이서 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-161">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="1f7c3-162">OS 디스크에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-162">Applicable to OS disks only.</span></span>  <span data-ttu-id="1f7c3-163">허용되는 값은 V1 및 V2입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-163">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="1f7c3-164">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="1f7c3-164">-ImageReference</span></span>
<span data-ttu-id="1f7c3-165">디스크의 이미지 참조를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-165">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="1f7c3-166">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1f7c3-166">-KeyEncryptionKey</span></span>
<span data-ttu-id="1f7c3-167">디스크의 키 암호화 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-167">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="1f7c3-168">-Location</span><span class="sxs-lookup"><span data-stu-id="1f7c3-168">-Location</span></span>
<span data-ttu-id="1f7c3-169">위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-169">Specifies a location.</span></span>

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

### <span data-ttu-id="1f7c3-170">-LogicalSectorSize</span><span class="sxs-lookup"><span data-stu-id="1f7c3-170">-LogicalSectorSize</span></span>
<span data-ttu-id="1f7c3-171">Ultra 디스크에 대한 논리 섹터 크기(byte)입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-171">Logical sector size in bytes for Ultra disks.</span></span> 

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

### <span data-ttu-id="1f7c3-172">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="1f7c3-172">-MaxSharesCount</span></span>
<span data-ttu-id="1f7c3-173">디스크에 동시에 연결할 수 있는 최대 VM 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-173">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="1f7c3-174">두 개 이상의 값은 여러 VM에 동시에 탑재할 수 있는 디스크를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-174">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="1f7c3-175">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1f7c3-175">-NetworkAccessPolicy</span></span>
<span data-ttu-id="1f7c3-176">네트워크 액세스 정책은 네트워크 액세스 정책을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-176">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="1f7c3-177">가능한 값은 'AllowAll', 'AllowPrivate', 'DenyAll'입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-177">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="1f7c3-178">-OsType</span><span class="sxs-lookup"><span data-stu-id="1f7c3-178">-OsType</span></span>
<span data-ttu-id="1f7c3-179">OS 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-179">Specifies the OS type.</span></span>

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

### <span data-ttu-id="1f7c3-180">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1f7c3-180">-SkuName</span></span>
<span data-ttu-id="1f7c3-181">저장소 계정의 SKU 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-181">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="1f7c3-182">사용 가능한 값은 Standard_LRS, Premium_LRS, StandardSSD_LRS 및 UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-182">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="1f7c3-183">UltraSSD_LRS CreateOption 매개 변수에 대한 빈 값과 함께 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-183">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="1f7c3-184">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="1f7c3-184">-SourceResourceId</span></span>
<span data-ttu-id="1f7c3-185">원본 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-185">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="1f7c3-186">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="1f7c3-186">-SourceUri</span></span>
<span data-ttu-id="1f7c3-187">원본 Uri를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-187">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="1f7c3-188">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1f7c3-188">-StorageAccountId</span></span>
<span data-ttu-id="1f7c3-189">저장소 계정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-189">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="1f7c3-190">-Tag</span><span class="sxs-lookup"><span data-stu-id="1f7c3-190">-Tag</span></span>
<span data-ttu-id="1f7c3-191">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-191">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1f7c3-192">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="1f7c3-192">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1f7c3-193">-Tier</span><span class="sxs-lookup"><span data-stu-id="1f7c3-193">-Tier</span></span>
<span data-ttu-id="1f7c3-194">디스크의 성능 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-194">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="1f7c3-195">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="1f7c3-195">-UploadSizeInBytes</span></span>
<span data-ttu-id="1f7c3-196">CreateOption이 업로드 중일 때 VHD 발판을 포함하여 업로드 내용의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-196">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="1f7c3-197">이 값은 20972032(VHD 발판의 경우 20 MiB + 512비트)와 35183298347520비트(VHD의 경우 32 TiB + 512비트)입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-197">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="1f7c3-198">-Zone</span><span class="sxs-lookup"><span data-stu-id="1f7c3-198">-Zone</span></span>
<span data-ttu-id="1f7c3-199">디스크에 대한 논리 영역 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-199">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="1f7c3-200">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f7c3-200">-Confirm</span></span>
<span data-ttu-id="1f7c3-201">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-201">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f7c3-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f7c3-202">-WhatIf</span></span>
<span data-ttu-id="1f7c3-203">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1f7c3-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f7c3-204">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-204">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f7c3-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f7c3-205">CommonParameters</span></span>
<span data-ttu-id="1f7c3-206">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f7c3-207">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1f7c3-207">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f7c3-208">입력</span><span class="sxs-lookup"><span data-stu-id="1f7c3-208">INPUTS</span></span>

### <span data-ttu-id="1f7c3-209">System.String</span><span class="sxs-lookup"><span data-stu-id="1f7c3-209">System.String</span></span>

### <span data-ttu-id="1f7c3-210">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="1f7c3-210">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="1f7c3-211">System.Int32</span><span class="sxs-lookup"><span data-stu-id="1f7c3-211">System.Int32</span></span>

### <span data-ttu-id="1f7c3-212">System.String[]</span><span class="sxs-lookup"><span data-stu-id="1f7c3-212">System.String[]</span></span>

### <span data-ttu-id="1f7c3-213">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1f7c3-213">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1f7c3-214">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="1f7c3-214">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="1f7c3-215">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1f7c3-215">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1f7c3-216">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="1f7c3-216">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="1f7c3-217">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="1f7c3-217">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="1f7c3-218">출력</span><span class="sxs-lookup"><span data-stu-id="1f7c3-218">OUTPUTS</span></span>

### <span data-ttu-id="1f7c3-219">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="1f7c3-219">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="1f7c3-220">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1f7c3-220">NOTES</span></span>

## <span data-ttu-id="1f7c3-221">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f7c3-221">RELATED LINKS</span></span>

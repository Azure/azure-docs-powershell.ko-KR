---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 4e2e09597cc52431657001e20ca34ad6e77aa40f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213104"
---
# <span data-ttu-id="352d5-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="352d5-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="352d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="352d5-102">SYNOPSIS</span></span>
<span data-ttu-id="352d5-103">구성 가능한 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="352d5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="352d5-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>]
 [-DiskMBpsReadWrite <Int64>] [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>]
 [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="352d5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="352d5-105">DESCRIPTION</span></span>
<span data-ttu-id="352d5-106">**AzDiskConfig** cmdlet은 구성 가능한 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="352d5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="352d5-107">EXAMPLES</span></span>

### <span data-ttu-id="352d5-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="352d5-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="352d5-109">첫 번째 명령은 Standard_LRS 저장소 계정 유형의 크기가 5GB 인 로컬 빈 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="352d5-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="352d5-111">두 번째 및 세 번째 명령은 disk 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="352d5-112">마지막 명령은 disk 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '에 이름이 ' Disk01 ' 인 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="352d5-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="352d5-113">Example 2</span></span>
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

<span data-ttu-id="352d5-114">첫 번째 명령은 업로드에 대 한 로컬 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="352d5-115">두 번째 명령은 disk 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '에 이름이 ' Disk01 ' 인 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="352d5-116">세 번째 명령은 디스크에 대 한 SAS Url을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="352d5-117">네 번째 명령은 디스크의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="352d5-118">디스크 상태가 ' ReadyToUpload ' 인 경우 사용자는 AzCopy를 사용 하 여 blob 저장소의 디스크를 디스크 SA Url로 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="352d5-119">업로드 하는 동안 디스크 상태가 ' ActiveUpload '로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="352d5-120">마지막 명령은 SAS Url에 대 한 디스크 액세스를 해지 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="352d5-121">예제 3</span><span class="sxs-lookup"><span data-stu-id="352d5-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="352d5-122">공유 갤러리 이미지 버전에서 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="352d5-123">Id는 공유 갤러리 이미지 버전의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="352d5-124">Lun은 원본이 데이터 디스크인 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="352d5-125">변수</span><span class="sxs-lookup"><span data-stu-id="352d5-125">PARAMETERS</span></span>

### <span data-ttu-id="352d5-126">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="352d5-126">-CreateOption</span></span>
<span data-ttu-id="352d5-127">이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만들거나, 빈 디스크를 만들거나, 기존 디스크를 연결 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-127">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="352d5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="352d5-128">-DefaultProfile</span></span>
<span data-ttu-id="352d5-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="352d5-130">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="352d5-130">-DiskEncryptionKey</span></span>
<span data-ttu-id="352d5-131">디스크의 디스크 암호화 키 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-131">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="352d5-132">-Disk. Setid</span><span class="sxs-lookup"><span data-stu-id="352d5-132">-DiskEncryptionSetId</span></span>
<span data-ttu-id="352d5-133">나머지 암호화를 사용 하는 데 사용할 디스크 암호화 집합의 리소스 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-133">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="352d5-134">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="352d5-134">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="352d5-135">공유 디스크를 읽기 전용으로 탑재 하는 모든 Vm에서 허용 되는 총 IOPS 수입니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-135">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="352d5-136">1 개의 작업은 4k와 256k 바이트 간에 전송할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-136">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="352d5-137">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="352d5-137">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="352d5-138">이 디스크에 허용 되는 IOPS 수입니다. UltraSSD 디스크에만 설정 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-138">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="352d5-139">1 개의 작업은 4k와 256k 바이트 간에 전송할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-139">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="352d5-140">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="352d5-140">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="352d5-141">"설명": "공유 디스크를 읽기 전용으로 탑재 하는 모든 Vm에서 허용 되는 총 처리량 (MBps)입니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-141">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="352d5-142">MBps는 초당 수백만 바이트의 수를 의미 합니다. 여기서는 ISO 표기법을 10의 거듭제곱으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-142">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="352d5-143">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="352d5-143">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="352d5-144">이 디스크에 허용 되는 대역폭 UltraSSD 디스크에만 설정 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-144">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="352d5-145">MBps는 초당 수백만 바이트의 수를 의미 합니다. 여기서는 ISO 표기법을 10의 거듭제곱으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-145">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="352d5-146">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="352d5-146">-DiskSizeGB</span></span>
<span data-ttu-id="352d5-147">디스크 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-147">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="352d5-148">-# Settingsenabled</span><span class="sxs-lookup"><span data-stu-id="352d5-148">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="352d5-149">암호화 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-149">Enable encryption settings.</span></span>

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

### <span data-ttu-id="352d5-150">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="352d5-150">-DiskAccessId</span></span>
<span data-ttu-id="352d5-151">개인 끝점을 사용 하는 데 사용할 DiskAccess 리소스의 ARM ID를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-151">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="352d5-152">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="352d5-152">-NetworkAccessPolicy</span></span>
<span data-ttu-id="352d5-153">네트워크 액세스 정책은 네트워크 액세스 정책을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-153">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="352d5-154">사용할 수 있는 값은 다음과 같습니다. ' AllowAll ', ' Allowall ', ' DenyAll '</span><span class="sxs-lookup"><span data-stu-id="352d5-154">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="352d5-155">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="352d5-155">-EncryptionType</span></span>
<span data-ttu-id="352d5-156">디스크의 데이터를 암호화 하는 데 사용 되는 키 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-156">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="352d5-157">사용 가능한 값은 ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '입니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-157">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="352d5-158">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="352d5-158">-GalleryImageReference</span></span>
<span data-ttu-id="352d5-159">GalleryImageReference 개체</span><span class="sxs-lookup"><span data-stu-id="352d5-159">The GalleryImageReference object.</span></span>  <span data-ttu-id="352d5-160">갤러리 이미지에서 만드는 경우 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-160">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="352d5-161">이 id는 디스크를 만들 공유 교정쇄 이미지 버전의 ARM id입니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-161">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="352d5-162">Lun은 복사본의 원본이 갤러리 이미지의 데이터 디스크 중 하나에 해당 하는 경우에 필요 합니다. null 이면 이미지의 OS 디스크가 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-162">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

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

### <span data-ttu-id="352d5-163">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="352d5-163">-HyperVGeneration</span></span>
<span data-ttu-id="352d5-164">가상 컴퓨터의 하이퍼바이저 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-164">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="352d5-165">OS 디스크에만 적용 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-165">Applicable to OS disks only.</span></span>  <span data-ttu-id="352d5-166">허용 되는 값은 V1 및 V2입니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-166">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="352d5-167">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="352d5-167">-ImageReference</span></span>
<span data-ttu-id="352d5-168">디스크에 대 한 이미지 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-168">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="352d5-169">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="352d5-169">-KeyEncryptionKey</span></span>
<span data-ttu-id="352d5-170">디스크의 키 암호화 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-170">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="352d5-171">-위치</span><span class="sxs-lookup"><span data-stu-id="352d5-171">-Location</span></span>
<span data-ttu-id="352d5-172">위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-172">Specifies a location.</span></span>

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

### <span data-ttu-id="352d5-173">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="352d5-173">-MaxSharesCount</span></span>
<span data-ttu-id="352d5-174">디스크에 동시에 연결할 수 있는 최대 Vm 수입니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-174">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="352d5-175">값이 1 보다 크면 여러 Vm에 동시에 탑재할 수 있는 디스크가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-175">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="352d5-176">-OsType</span><span class="sxs-lookup"><span data-stu-id="352d5-176">-OsType</span></span>
<span data-ttu-id="352d5-177">OS 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-177">Specifies the OS type.</span></span>

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

### <span data-ttu-id="352d5-178">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="352d5-178">-SkuName</span></span>
<span data-ttu-id="352d5-179">저장소 계정의 Sku 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-179">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="352d5-180">사용할 수 있는 값은 Standard_LRS, Premium_LRS, StandardSSD_LRS, UltraSSD_LRS입니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-180">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="352d5-181">UltraSSD_LRS는 CreateOption 매개 변수에 대해 빈 값 으로만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-181">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="352d5-182">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="352d5-182">-SourceResourceId</span></span>
<span data-ttu-id="352d5-183">원본 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-183">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="352d5-184">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="352d5-184">-SourceUri</span></span>
<span data-ttu-id="352d5-185">원본 Uri를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-185">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="352d5-186">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="352d5-186">-StorageAccountId</span></span>
<span data-ttu-id="352d5-187">저장소 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-187">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="352d5-188">태그</span><span class="sxs-lookup"><span data-stu-id="352d5-188">-Tag</span></span>
<span data-ttu-id="352d5-189">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-189">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="352d5-190">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="352d5-190">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="352d5-191">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="352d5-191">-UploadSizeInBytes</span></span>
<span data-ttu-id="352d5-192">CreateOption 업로드가 때 VHD 바닥글을 포함 하 여 업로드 콘텐츠의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-192">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="352d5-193">이 값은 20972032 (VHD 바닥글의 경우 20 MiB + 512 바이트) 및 35183298347520 바이트 (VHD 바닥글에 대 한 32 TiB + 512 바이트) 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-193">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="352d5-194">-Zone</span><span class="sxs-lookup"><span data-stu-id="352d5-194">-Zone</span></span>
<span data-ttu-id="352d5-195">디스크에 대 한 논리 영역 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-195">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="352d5-196">-확인</span><span class="sxs-lookup"><span data-stu-id="352d5-196">-Confirm</span></span>
<span data-ttu-id="352d5-197">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="352d5-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="352d5-198">-WhatIf</span></span>
<span data-ttu-id="352d5-199">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-199">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="352d5-200">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="352d5-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="352d5-201">CommonParameters</span></span>
<span data-ttu-id="352d5-202">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="352d5-203">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="352d5-203">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="352d5-204">입력</span><span class="sxs-lookup"><span data-stu-id="352d5-204">INPUTS</span></span>

### <span data-ttu-id="352d5-205">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="352d5-205">System.String</span></span>

### <span data-ttu-id="352d5-206">시스템 Null 허용 ' 1 [[OperatingSystemTypes, Microsoft azure. 23.0.0.0, Version =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="352d5-206">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="352d5-207">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="352d5-207">System.Int32</span></span>

### <span data-ttu-id="352d5-208">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="352d5-208">System.String[]</span></span>

### <span data-ttu-id="352d5-209">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="352d5-209">System.Collections.Hashtable</span></span>

### <span data-ttu-id="352d5-210">Microsoft. 관리. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="352d5-210">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="352d5-211">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="352d5-211">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="352d5-212">KeyVaultAndSecretReference를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-212">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="352d5-213">KeyVaultAndKeyReference를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="352d5-213">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="352d5-214">출력</span><span class="sxs-lookup"><span data-stu-id="352d5-214">OUTPUTS</span></span>

### <span data-ttu-id="352d5-215">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="352d5-215">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="352d5-216">상속자</span><span class="sxs-lookup"><span data-stu-id="352d5-216">NOTES</span></span>

## <span data-ttu-id="352d5-217">관련 링크</span><span class="sxs-lookup"><span data-stu-id="352d5-217">RELATED LINKS</span></span>

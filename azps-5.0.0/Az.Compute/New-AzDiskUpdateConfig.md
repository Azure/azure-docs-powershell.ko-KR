---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: a738ec606fc982573c4062879e9da4becee43df2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216244"
---
# <span data-ttu-id="eee00-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="eee00-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="eee00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eee00-102">SYNOPSIS</span></span>
<span data-ttu-id="eee00-103">구성 가능한 디스크 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="eee00-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eee00-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-Tier <String>] [-DiskIOPSReadOnly <Int64>]
 [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eee00-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eee00-105">DESCRIPTION</span></span>
<span data-ttu-id="eee00-106">**AzDiskUpdateConfig** cmdlet은 구성 가능한 디스크 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="eee00-107">예제의</span><span class="sxs-lookup"><span data-stu-id="eee00-107">EXAMPLES</span></span>

### <span data-ttu-id="eee00-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="eee00-108">Example 1</span></span>
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

<span data-ttu-id="eee00-109">첫 번째 명령은 Premium_LRS 저장소 계정 유형에 서 크기가 10GB 인 로컬 빈 디스크 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="eee00-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="eee00-111">두 번째 및 세 번째 명령은 디스크 업데이트 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="eee00-112">마지막 명령은 disk update 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '의 이름이 ' Disk01 ' 인 기존 디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="eee00-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="eee00-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="eee00-114">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 10gb 디스크 크기로 이름이 ' Disk01 ' 인 기존 디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="eee00-115">변수</span><span class="sxs-lookup"><span data-stu-id="eee00-115">PARAMETERS</span></span>

### <span data-ttu-id="eee00-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eee00-116">-DefaultProfile</span></span>
<span data-ttu-id="eee00-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eee00-118">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="eee00-118">-DiskAccessId</span></span>
<span data-ttu-id="eee00-119">{{Fill DiskAccessId Description}}</span><span class="sxs-lookup"><span data-stu-id="eee00-119">{{ Fill DiskAccessId Description }}</span></span>

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

### <span data-ttu-id="eee00-120">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="eee00-120">-DiskEncryptionKey</span></span>
<span data-ttu-id="eee00-121">디스크의 디스크 암호화 키 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-121">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="eee00-122">-Disk. Setid</span><span class="sxs-lookup"><span data-stu-id="eee00-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="eee00-123">나머지 암호화를 사용 하는 데 사용할 디스크 암호화 집합의 리소스 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-123">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="eee00-124">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="eee00-124">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="eee00-125">공유 디스크를 읽기 전용으로 탑재 하는 모든 Vm에서 허용 되는 총 IOPS 수입니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-125">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="eee00-126">1 개의 작업은 4k와 256k 바이트 간에 전송할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-126">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="eee00-127">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="eee00-127">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="eee00-128">이 디스크에 허용 되는 IOPS 수입니다. UltraSSD 디스크에만 설정 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-128">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="eee00-129">1 개의 작업은 4k와 256k 바이트 간에 전송할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-129">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="eee00-130">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="eee00-130">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="eee00-131">공유 디스크를 읽기 전용으로 탑재 하는 모든 Vm에서 허용 되는 총 처리량 (MBps)입니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-131">The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="eee00-132">MBps는 초당 수백만 바이트의 수를 의미 합니다. 여기서는 ISO 표기법을 10의 거듭제곱으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-132">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="eee00-133">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="eee00-133">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="eee00-134">이 디스크에 허용 되는 대역폭 UltraSSD 디스크에만 설정 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-134">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="eee00-135">MBps는 초당 수백만 바이트의 수를 의미 합니다. 여기서는 ISO 표기법을 10의 거듭제곱으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-135">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="eee00-136">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="eee00-136">-DiskSizeGB</span></span>
<span data-ttu-id="eee00-137">디스크 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-137">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="eee00-138">-# Settingsenabled</span><span class="sxs-lookup"><span data-stu-id="eee00-138">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="eee00-139">암호화 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-139">Enable encryption settings.</span></span>

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

### <span data-ttu-id="eee00-140">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="eee00-140">-EncryptionType</span></span>
<span data-ttu-id="eee00-141">디스크의 데이터를 암호화 하는 데 사용 되는 키 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-141">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="eee00-142">사용 가능한 값은 ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '입니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-142">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="eee00-143">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="eee00-143">-KeyEncryptionKey</span></span>
<span data-ttu-id="eee00-144">디스크의 키 암호화 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-144">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="eee00-145">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="eee00-145">-MaxSharesCount</span></span>
<span data-ttu-id="eee00-146">디스크에 동시에 연결할 수 있는 최대 Vm 수입니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-146">The maximum number of VMs that can attach to the disk at the same time.</span></span> <span data-ttu-id="eee00-147">값이 1 보다 크면 여러 Vm에 동시에 탑재할 수 있는 디스크가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-147">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="eee00-148">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eee00-148">-NetworkAccessPolicy</span></span>
<span data-ttu-id="eee00-149">{{NetworkAccessPolicy 채우기 설명}}</span><span class="sxs-lookup"><span data-stu-id="eee00-149">{{ Fill NetworkAccessPolicy Description }}</span></span>

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

### <span data-ttu-id="eee00-150">-OsType</span><span class="sxs-lookup"><span data-stu-id="eee00-150">-OsType</span></span>
<span data-ttu-id="eee00-151">OS 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-151">Specifies the OS type.</span></span>

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

### <span data-ttu-id="eee00-152">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="eee00-152">-SkuName</span></span>
<span data-ttu-id="eee00-153">저장소 계정의 Sku 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-153">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="eee00-154">사용할 수 있는 값은 Standard_LRS, Premium_LRS, StandardSSD_LRS, UltraSSD_LRS입니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-154">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="eee00-155">UltraSSD_LRS는 CreateOption 매개 변수에 대해 빈 값 으로만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-155">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="eee00-156">태그</span><span class="sxs-lookup"><span data-stu-id="eee00-156">-Tag</span></span>
<span data-ttu-id="eee00-157">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-157">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="eee00-158">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="eee00-158">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="eee00-159">-티어</span><span class="sxs-lookup"><span data-stu-id="eee00-159">-Tier</span></span>
<span data-ttu-id="eee00-160">디스크의 성능 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-160">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="eee00-161">-확인</span><span class="sxs-lookup"><span data-stu-id="eee00-161">-Confirm</span></span>
<span data-ttu-id="eee00-162">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eee00-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eee00-163">-WhatIf</span></span>
<span data-ttu-id="eee00-164">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eee00-165">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eee00-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eee00-166">CommonParameters</span></span>
<span data-ttu-id="eee00-167">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eee00-168">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eee00-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eee00-169">입력</span><span class="sxs-lookup"><span data-stu-id="eee00-169">INPUTS</span></span>

### <span data-ttu-id="eee00-170">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eee00-170">System.String</span></span>

### <span data-ttu-id="eee00-171">시스템 Null 허용 ' 1 [[OperatingSystemTypes, Microsoft azure. 23.0.0.0, Version =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="eee00-171">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="eee00-172">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="eee00-172">System.Int32</span></span>

### <span data-ttu-id="eee00-173">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="eee00-173">System.Collections.Hashtable</span></span>

### <span data-ttu-id="eee00-174">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="eee00-174">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="eee00-175">KeyVaultAndSecretReference를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-175">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="eee00-176">KeyVaultAndKeyReference를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="eee00-176">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="eee00-177">출력</span><span class="sxs-lookup"><span data-stu-id="eee00-177">OUTPUTS</span></span>

### <span data-ttu-id="eee00-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="eee00-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="eee00-179">상속자</span><span class="sxs-lookup"><span data-stu-id="eee00-179">NOTES</span></span>

## <span data-ttu-id="eee00-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eee00-180">RELATED LINKS</span></span>

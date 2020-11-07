---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskConfig.md
ms.openlocfilehash: 693d121bac5a618c5ad588cf4d34f63d8c6d0fd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703003"
---
# <span data-ttu-id="ec38f-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="ec38f-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="ec38f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec38f-102">SYNOPSIS</span></span>
<span data-ttu-id="ec38f-103">구성 가능한 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec38f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec38f-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-DiskIOPSReadWrite <Int32>] [-DiskMBpsReadWrite <Int32>]
 [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec38f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ec38f-105">DESCRIPTION</span></span>
<span data-ttu-id="ec38f-106">**AzureRmDiskConfig** cmdlet은 구성 가능한 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="ec38f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ec38f-107">EXAMPLES</span></span>

### <span data-ttu-id="ec38f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ec38f-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="ec38f-109">첫 번째 명령은 Standard_LRS 저장소 계정 유형의 크기가 5GB 인 로컬 빈 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="ec38f-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="ec38f-111">두 번째 및 세 번째 명령은 disk 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="ec38f-112">마지막 명령은 disk 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '에 이름이 ' Disk01 ' 인 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ec38f-113">변수</span><span class="sxs-lookup"><span data-stu-id="ec38f-113">PARAMETERS</span></span>

### <span data-ttu-id="ec38f-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="ec38f-114">-CreateOption</span></span>
<span data-ttu-id="ec38f-115">이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만들거나, 빈 디스크를 만들거나, 기존 디스크를 연결 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="ec38f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec38f-116">-DefaultProfile</span></span>
<span data-ttu-id="ec38f-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec38f-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ec38f-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="ec38f-119">디스크의 디스크 암호화 키 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="ec38f-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="ec38f-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="ec38f-121">이 디스크에 허용 되는 IOPS 수입니다. UltraSSD 디스크에만 설정 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-121">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="ec38f-122">1 개의 작업은 4k와 256k 바이트 간에 전송할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-122">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="ec38f-123">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="ec38f-123">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="ec38f-124">이 디스크에 허용 되는 대역폭 UltraSSD 디스크에만 설정 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-124">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="ec38f-125">MBps는 초당 수백만 바이트의 수를 의미 합니다. 여기서는 ISO 표기법을 10의 거듭제곱으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-125">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="ec38f-126">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="ec38f-126">-DiskSizeGB</span></span>
<span data-ttu-id="ec38f-127">디스크 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-127">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="ec38f-128">-# Settingsenabled</span><span class="sxs-lookup"><span data-stu-id="ec38f-128">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="ec38f-129">암호화 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-129">Enable encryption settings.</span></span>

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

### <span data-ttu-id="ec38f-130">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="ec38f-130">-ImageReference</span></span>
<span data-ttu-id="ec38f-131">디스크에 대 한 이미지 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-131">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="ec38f-132">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ec38f-132">-KeyEncryptionKey</span></span>
<span data-ttu-id="ec38f-133">디스크의 키 암호화 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-133">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="ec38f-134">-위치</span><span class="sxs-lookup"><span data-stu-id="ec38f-134">-Location</span></span>
<span data-ttu-id="ec38f-135">위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-135">Specifies a location.</span></span>

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

### <span data-ttu-id="ec38f-136">-OsType</span><span class="sxs-lookup"><span data-stu-id="ec38f-136">-OsType</span></span>
<span data-ttu-id="ec38f-137">OS 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-137">Specifies the OS type.</span></span>

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

### <span data-ttu-id="ec38f-138">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="ec38f-138">-SkuName</span></span>
<span data-ttu-id="ec38f-139">저장소 계정의 Sku 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-139">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="ec38f-140">사용할 수 있는 값은 Standard_LRS, Premium_LRS, StandardSSD_LRS, UltraSSD_LRS입니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-140">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="ec38f-141">UltraSSD_LRS는 CreateOption 매개 변수에 대해 빈 값 으로만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-141">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="ec38f-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="ec38f-142">-SourceResourceId</span></span>
<span data-ttu-id="ec38f-143">원본 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-143">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="ec38f-144">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="ec38f-144">-SourceUri</span></span>
<span data-ttu-id="ec38f-145">원본 Uri를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-145">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="ec38f-146">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ec38f-146">-StorageAccountId</span></span>
<span data-ttu-id="ec38f-147">저장소 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-147">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="ec38f-148">태그</span><span class="sxs-lookup"><span data-stu-id="ec38f-148">-Tag</span></span>
<span data-ttu-id="ec38f-149">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ec38f-150">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ec38f-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ec38f-151">-Zone</span><span class="sxs-lookup"><span data-stu-id="ec38f-151">-Zone</span></span>
<span data-ttu-id="ec38f-152">디스크에 대 한 논리 영역 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-152">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="ec38f-153">-확인</span><span class="sxs-lookup"><span data-stu-id="ec38f-153">-Confirm</span></span>
<span data-ttu-id="ec38f-154">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec38f-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec38f-155">-WhatIf</span></span>
<span data-ttu-id="ec38f-156">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec38f-157">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec38f-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec38f-158">CommonParameters</span></span>
<span data-ttu-id="ec38f-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec38f-160">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec38f-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec38f-161">입력</span><span class="sxs-lookup"><span data-stu-id="ec38f-161">INPUTS</span></span>

### <span data-ttu-id="ec38f-162">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ec38f-162">System.String</span></span>

### <span data-ttu-id="ec38f-163">시스템 Null 허용 ' 1 [[OperatingSystemTypes, Microsoft azure. 21.0.0.0, Version =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ec38f-163">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ec38f-164">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="ec38f-164">System.Int32</span></span>

### <span data-ttu-id="ec38f-165">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="ec38f-165">System.String[]</span></span>

### <span data-ttu-id="ec38f-166">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="ec38f-166">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ec38f-167">Microsoft. 관리. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="ec38f-167">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="ec38f-168">시스템 Null 허용 ' 1 [[b77a5c561934e089] [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="ec38f-168">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ec38f-169">KeyVaultAndSecretReference를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-169">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="ec38f-170">KeyVaultAndKeyReference를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec38f-170">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="ec38f-171">출력</span><span class="sxs-lookup"><span data-stu-id="ec38f-171">OUTPUTS</span></span>

### <span data-ttu-id="ec38f-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="ec38f-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="ec38f-173">상속자</span><span class="sxs-lookup"><span data-stu-id="ec38f-173">NOTES</span></span>

## <span data-ttu-id="ec38f-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec38f-174">RELATED LINKS</span></span>

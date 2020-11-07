---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 293e894704509fe1b869ca23bd726c49f400de48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701309"
---
# <span data-ttu-id="b8e1a-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="b8e1a-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="b8e1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8e1a-102">SYNOPSIS</span></span>
<span data-ttu-id="b8e1a-103">구성 가능한 스냅숏 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="b8e1a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8e1a-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8e1a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b8e1a-105">DESCRIPTION</span></span>
<span data-ttu-id="b8e1a-106">**AzSnapshotConfig** cmdlet은 구성할 수 있는 스냅숏 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="b8e1a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b8e1a-107">EXAMPLES</span></span>

### <span data-ttu-id="b8e1a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b8e1a-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="b8e1a-109">첫 번째 명령은 Standard_LRS 저장소 계정 형식의 크기가 5GB 인 로컬 빈 스냅숏 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="b8e1a-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="b8e1a-111">두 번째 및 세 번째 명령은 snapshot 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="b8e1a-112">마지막 명령은 snapshot 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '에 이름이 ' Snapshot01 ' 인 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b8e1a-113">변수</span><span class="sxs-lookup"><span data-stu-id="b8e1a-113">PARAMETERS</span></span>

### <span data-ttu-id="b8e1a-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="b8e1a-114">-CreateOption</span></span>
<span data-ttu-id="b8e1a-115">이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만들거나, 빈 디스크를 만들거나, 기존 디스크를 연결 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="b8e1a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8e1a-116">-DefaultProfile</span></span>
<span data-ttu-id="b8e1a-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8e1a-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b8e1a-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="b8e1a-119">스냅숏에 대 한 디스크 암호화 키 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="b8e1a-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="b8e1a-120">-DiskSizeGB</span></span>
<span data-ttu-id="b8e1a-121">디스크 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="b8e1a-122">-# Settingsenabled</span><span class="sxs-lookup"><span data-stu-id="b8e1a-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="b8e1a-123">암호화 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="b8e1a-124">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="b8e1a-124">-HyperVGeneration</span></span>
<span data-ttu-id="b8e1a-125">가상 컴퓨터의 하이퍼바이저 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-125">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="b8e1a-126">OS 디스크에만 적용 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-126">Applicable to OS disks only.</span></span>  <span data-ttu-id="b8e1a-127">허용 되는 값은 V1 및 V2입니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-127">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="b8e1a-128">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="b8e1a-128">-ImageReference</span></span>
<span data-ttu-id="b8e1a-129">스냅숏에 대 한 이미지 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-129">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="b8e1a-130">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b8e1a-130">-KeyEncryptionKey</span></span>
<span data-ttu-id="b8e1a-131">스냅숏에 대 한 키 암호화 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-131">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="b8e1a-132">-위치</span><span class="sxs-lookup"><span data-stu-id="b8e1a-132">-Location</span></span>
<span data-ttu-id="b8e1a-133">위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-133">Specifies a location.</span></span>

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

### <span data-ttu-id="b8e1a-134">-OsType</span><span class="sxs-lookup"><span data-stu-id="b8e1a-134">-OsType</span></span>
<span data-ttu-id="b8e1a-135">OS 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-135">Specifies the OS type.</span></span>

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

### <span data-ttu-id="b8e1a-136">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="b8e1a-136">-SkuName</span></span>
<span data-ttu-id="b8e1a-137">저장소 계정의 Sku 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-137">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="b8e1a-138">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="b8e1a-138">-SourceResourceId</span></span>
<span data-ttu-id="b8e1a-139">원본 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-139">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="b8e1a-140">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="b8e1a-140">-SourceUri</span></span>
<span data-ttu-id="b8e1a-141">원본 Uri를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-141">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="b8e1a-142">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b8e1a-142">-StorageAccountId</span></span>
<span data-ttu-id="b8e1a-143">저장소 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-143">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="b8e1a-144">태그</span><span class="sxs-lookup"><span data-stu-id="b8e1a-144">-Tag</span></span>
<span data-ttu-id="b8e1a-145">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b8e1a-146">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b8e1a-146">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b8e1a-147">-확인</span><span class="sxs-lookup"><span data-stu-id="b8e1a-147">-Confirm</span></span>
<span data-ttu-id="b8e1a-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8e1a-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8e1a-149">-WhatIf</span></span>
<span data-ttu-id="b8e1a-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8e1a-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8e1a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8e1a-152">CommonParameters</span></span>
<span data-ttu-id="b8e1a-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8e1a-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8e1a-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8e1a-155">입력</span><span class="sxs-lookup"><span data-stu-id="b8e1a-155">INPUTS</span></span>

### <span data-ttu-id="b8e1a-156">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b8e1a-156">System.String</span></span>

### <span data-ttu-id="b8e1a-157">시스템 Null 허용 ' 1 [[OperatingSystemTypes, Microsoft azure. 23.0.0.0, Version =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b8e1a-157">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b8e1a-158">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-158">System.Int32</span></span>

### <span data-ttu-id="b8e1a-159">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="b8e1a-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b8e1a-160">Microsoft. 관리. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="b8e1a-160">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="b8e1a-161">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b8e1a-161">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b8e1a-162">KeyVaultAndSecretReference를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-162">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="b8e1a-163">KeyVaultAndKeyReference를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8e1a-163">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="b8e1a-164">출력</span><span class="sxs-lookup"><span data-stu-id="b8e1a-164">OUTPUTS</span></span>

### <span data-ttu-id="b8e1a-165">Microsoft. a. a. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="b8e1a-165">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="b8e1a-166">상속자</span><span class="sxs-lookup"><span data-stu-id="b8e1a-166">NOTES</span></span>

## <span data-ttu-id="b8e1a-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8e1a-167">RELATED LINKS</span></span>

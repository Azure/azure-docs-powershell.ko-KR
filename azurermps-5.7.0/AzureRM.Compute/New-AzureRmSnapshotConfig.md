---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotConfig.md
ms.openlocfilehash: ee3dd849a8f3877ac19ce86a7257d28fc18575c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702755"
---
# <span data-ttu-id="5edae-101">New-AzureRmSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="5edae-101">New-AzureRmSnapshotConfig</span></span>

## <span data-ttu-id="5edae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5edae-102">SYNOPSIS</span></span>
<span data-ttu-id="5edae-103">구성 가능한 스냅숏 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-103">Creates a configurable snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5edae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5edae-104">SYNTAX</span></span>

```
New-AzureRmSnapshotConfig [-SkuName <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5edae-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5edae-105">DESCRIPTION</span></span>
<span data-ttu-id="5edae-106">**AzureRmSnapshotConfig** cmdlet은 구성할 수 있는 스냅숏 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-106">The **New-AzureRmSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="5edae-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5edae-107">EXAMPLES</span></span>

### <span data-ttu-id="5edae-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5edae-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="5edae-109">첫 번째 명령은 Standard_LRS 저장소 계정 형식의 크기가 5GB 인 로컬 빈 스냅숏 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="5edae-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="5edae-111">두 번째 및 세 번째 명령은 snapshot 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="5edae-112">마지막 명령은 snapshot 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '에 이름이 ' Snapshot01 ' 인 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="5edae-113">변수</span><span class="sxs-lookup"><span data-stu-id="5edae-113">PARAMETERS</span></span>

### <span data-ttu-id="5edae-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="5edae-114">-CreateOption</span></span>
<span data-ttu-id="5edae-115">이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만들거나, 빈 디스크를 만들거나, 기존 디스크를 연결 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: DiskCreateOption
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy, Restore

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-116">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5edae-116">-DiskEncryptionKey</span></span>
<span data-ttu-id="5edae-117">스냅숏에 대 한 디스크 암호화 키 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-117">Specifies the disk encryption key object on a snapshot.</span></span>

```yaml
Type: KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-118">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="5edae-118">-DiskSizeGB</span></span>
<span data-ttu-id="5edae-119">디스크 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-119">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-120">-# Settingsenabled</span><span class="sxs-lookup"><span data-stu-id="5edae-120">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="5edae-121">암호화 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-121">Enable encryption settings.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-122">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="5edae-122">-ImageReference</span></span>
<span data-ttu-id="5edae-123">스냅숏에 대 한 이미지 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-123">Specifies the image reference on a snapshot.</span></span>

```yaml
Type: ImageDiskReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5edae-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="5edae-125">스냅숏에 대 한 키 암호화 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-125">Specifies the Key encryption key on a snapshot.</span></span>

```yaml
Type: KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-126">-위치</span><span class="sxs-lookup"><span data-stu-id="5edae-126">-Location</span></span>
<span data-ttu-id="5edae-127">위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-127">Specifies a location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="5edae-128">-OsType</span></span>
<span data-ttu-id="5edae-129">OS 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-129">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-130">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="5edae-130">-SkuName</span></span>
<span data-ttu-id="5edae-131">저장소 계정의 Sku 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-131">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-132">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="5edae-132">-SourceResourceId</span></span>
<span data-ttu-id="5edae-133">원본 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-133">Specifies the source resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-134">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="5edae-134">-SourceUri</span></span>
<span data-ttu-id="5edae-135">원본 Uri를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-135">Specifies the source Uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-136">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="5edae-136">-StorageAccountId</span></span>
<span data-ttu-id="5edae-137">저장소 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-137">Specifies the storage account ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-138">태그</span><span class="sxs-lookup"><span data-stu-id="5edae-138">-Tag</span></span>
<span data-ttu-id="5edae-139">리소스 및 리소스 그룹에 이름-값 쌍 집합을 태깅 할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-139">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-140">-확인</span><span class="sxs-lookup"><span data-stu-id="5edae-140">-Confirm</span></span>
<span data-ttu-id="5edae-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5edae-142">-WhatIf</span></span>
<span data-ttu-id="5edae-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5edae-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edae-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5edae-145">CommonParameters</span></span>
<span data-ttu-id="5edae-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5edae-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5edae-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5edae-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5edae-148">입력</span><span class="sxs-lookup"><span data-stu-id="5edae-148">INPUTS</span></span>

### <span data-ttu-id="5edae-149">시스템 Null 허용 ' 1 [[14.0.0.0]. StorageAccountTypes, Microsoft Azure. 관리., Version = 31bf3856ad364e35, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="5edae-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="5edae-150">시스템. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[system. Int32, mscorlib, Version = 4.0.0.0, Culture = 중립적인, PublicKeyToken = b77a5c561934e089]] system.webserver 시스템.. a `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, Mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]] microsoft azure. \* \*. \* \*. i i. 관리.</span><span class="sxs-lookup"><span data-stu-id="5edae-150">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="5edae-151">출력</span><span class="sxs-lookup"><span data-stu-id="5edae-151">OUTPUTS</span></span>

### <span data-ttu-id="5edae-152">Microsoft. 관리. 스냅샷</span><span class="sxs-lookup"><span data-stu-id="5edae-152">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="5edae-153">상속자</span><span class="sxs-lookup"><span data-stu-id="5edae-153">NOTES</span></span>

## <span data-ttu-id="5edae-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5edae-154">RELATED LINKS</span></span>


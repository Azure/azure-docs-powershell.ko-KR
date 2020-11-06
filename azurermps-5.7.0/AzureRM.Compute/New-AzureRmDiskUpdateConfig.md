---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskUpdateConfig.md
ms.openlocfilehash: 68a6e53e6ad024411c0775a21bbdbb0d0b8c75f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529914"
---
# <span data-ttu-id="3bb28-101">New-AzureRmDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="3bb28-101">New-AzureRmDiskUpdateConfig</span></span>

## <span data-ttu-id="3bb28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bb28-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb28-103">구성 가능한 디스크 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-103">Creates a configurable disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bb28-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3bb28-104">SYNTAX</span></span>

```
New-AzureRmDiskUpdateConfig [-SkuName <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bb28-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3bb28-105">DESCRIPTION</span></span>
<span data-ttu-id="3bb28-106">**AzureRmDiskUpdateConfig** cmdlet은 구성 가능한 디스크 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-106">The **New-AzureRmDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="3bb28-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3bb28-107">EXAMPLES</span></span>

### <span data-ttu-id="3bb28-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3bb28-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="3bb28-109">첫 번째 명령은 Premium_LRS 저장소 계정 유형에 서 크기가 10GB 인 로컬 빈 디스크 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="3bb28-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="3bb28-111">두 번째 및 세 번째 명령은 디스크 업데이트 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="3bb28-112">마지막 명령은 disk update 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '의 이름이 ' Disk01 ' 인 기존 디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="3bb28-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="3bb28-113">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="3bb28-114">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 10gb 디스크 크기로 이름이 ' Disk01 ' 인 기존 디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="3bb28-115">변수</span><span class="sxs-lookup"><span data-stu-id="3bb28-115">PARAMETERS</span></span>

### <span data-ttu-id="3bb28-116">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="3bb28-116">-CreateOption</span></span>
<span data-ttu-id="3bb28-117">이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만들거나, 빈 디스크를 만들거나, 기존 디스크를 연결 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-117">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="3bb28-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3bb28-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="3bb28-119">디스크의 디스크 암호화 키 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="3bb28-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="3bb28-120">-DiskSizeGB</span></span>
<span data-ttu-id="3bb28-121">디스크 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="3bb28-122">-# Settingsenabled</span><span class="sxs-lookup"><span data-stu-id="3bb28-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="3bb28-123">암호화 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="3bb28-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="3bb28-124">-ImageReference</span></span>
<span data-ttu-id="3bb28-125">디스크에 대 한 이미지 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-125">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="3bb28-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3bb28-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="3bb28-127">디스크의 키 암호화 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-127">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="3bb28-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="3bb28-128">-OsType</span></span>
<span data-ttu-id="3bb28-129">OS 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-129">Specifies the OS type.</span></span>

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

### <span data-ttu-id="3bb28-130">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="3bb28-130">-SkuName</span></span>
<span data-ttu-id="3bb28-131">저장소 계정의 Sku 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-131">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="3bb28-132">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="3bb28-132">-SourceResourceId</span></span>
<span data-ttu-id="3bb28-133">원본 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-133">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="3bb28-134">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="3bb28-134">-SourceUri</span></span>
<span data-ttu-id="3bb28-135">원본 Uri를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-135">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="3bb28-136">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3bb28-136">-StorageAccountId</span></span>
<span data-ttu-id="3bb28-137">저장소 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-137">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="3bb28-138">태그</span><span class="sxs-lookup"><span data-stu-id="3bb28-138">-Tag</span></span>
<span data-ttu-id="3bb28-139">리소스 및 리소스 그룹에 이름-값 쌍 집합을 태깅 할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-139">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bb28-140">-확인</span><span class="sxs-lookup"><span data-stu-id="3bb28-140">-Confirm</span></span>
<span data-ttu-id="3bb28-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bb28-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bb28-142">-WhatIf</span></span>
<span data-ttu-id="3bb28-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3bb28-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bb28-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb28-145">CommonParameters</span></span>
<span data-ttu-id="3bb28-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bb28-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb28-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bb28-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb28-148">입력</span><span class="sxs-lookup"><span data-stu-id="3bb28-148">INPUTS</span></span>

### <span data-ttu-id="3bb28-149">시스템 Null 허용 ' 1 [[14.0.0.0]. StorageAccountTypes, Microsoft Azure. 관리., Version = 31bf3856ad364e35, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="3bb28-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="3bb28-150">시스템. Null 허용 `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[b77a5c561934e089, mscorlib, version = 4.0.0.0, culture = 중립, publickeytoken =]] system.webserver/Hashtable 시스템. Null 허용 `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[[시스템], 부울, Mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]] microsoft azure.</span><span class="sxs-lookup"><span data-stu-id="3bb28-150">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="3bb28-151">출력</span><span class="sxs-lookup"><span data-stu-id="3bb28-151">OUTPUTS</span></span>

### <span data-ttu-id="3bb28-152">Microsoft. 관리. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="3bb28-152">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="3bb28-153">상속자</span><span class="sxs-lookup"><span data-stu-id="3bb28-153">NOTES</span></span>

## <span data-ttu-id="3bb28-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3bb28-154">RELATED LINKS</span></span>


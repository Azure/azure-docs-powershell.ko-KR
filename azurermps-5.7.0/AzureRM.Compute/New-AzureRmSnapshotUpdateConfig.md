---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotUpdateConfig.md
ms.openlocfilehash: 97bfd93babc75b09f87e53f62c60cd4fb08ea599
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531096"
---
# <span data-ttu-id="6e490-101">New-AzureRmSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="6e490-101">New-AzureRmSnapshotUpdateConfig</span></span>

## <span data-ttu-id="6e490-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e490-102">SYNOPSIS</span></span>
<span data-ttu-id="6e490-103">구성 가능한 스냅숏 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-103">Creates a configurable snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e490-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e490-104">SYNTAX</span></span>

```
New-AzureRmSnapshotUpdateConfig [-SkuName <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e490-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6e490-105">DESCRIPTION</span></span>
<span data-ttu-id="6e490-106">**AzureRmSnapshotUpdateConfig** cmdlet은 구성할 수 있는 스냅숏 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-106">The **New-AzureRmSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="6e490-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6e490-107">EXAMPLES</span></span>

### <span data-ttu-id="6e490-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6e490-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="6e490-109">첫 번째 명령은 Premium_LRS 저장소 계정 유형에 서 크기가 10GB 인 로컬 빈 스냅샷 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="6e490-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="6e490-111">두 번째 및 세 번째 명령은 스냅샷 업데이트 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="6e490-112">마지막 명령은 snapshot update 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '의 이름이 ' Snapshot01 ' 인 기존 스냅숏을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="6e490-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="6e490-113">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="6e490-114">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 10gb 디스크 크기로 이름이 ' Snapshot01 ' 인 기존 스냅숏을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="6e490-115">변수</span><span class="sxs-lookup"><span data-stu-id="6e490-115">PARAMETERS</span></span>

### <span data-ttu-id="6e490-116">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="6e490-116">-CreateOption</span></span>
<span data-ttu-id="6e490-117">이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 컴퓨터에 스냅숏을 만들지, 빈 디스크를 만들지 아니면 기존 디스크를 연결 하는지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-117">Specifies whether this cmdlet creates a snapshot in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="6e490-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6e490-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="6e490-119">스냅숏에 대 한 디스크 암호화 키 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="6e490-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="6e490-120">-DiskSizeGB</span></span>
<span data-ttu-id="6e490-121">디스크 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="6e490-122">-# Settingsenabled</span><span class="sxs-lookup"><span data-stu-id="6e490-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="6e490-123">암호화 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="6e490-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="6e490-124">-ImageReference</span></span>
<span data-ttu-id="6e490-125">스냅숏에 대 한 이미지 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-125">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="6e490-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6e490-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="6e490-127">스냅숏에 대 한 키 암호화 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="6e490-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="6e490-128">-OsType</span></span>
<span data-ttu-id="6e490-129">OS 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-129">Specifies the OS type.</span></span>

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

### <span data-ttu-id="6e490-130">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="6e490-130">-SkuName</span></span>
<span data-ttu-id="6e490-131">저장소 계정의 Sku 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-131">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="6e490-132">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="6e490-132">-SourceResourceId</span></span>
<span data-ttu-id="6e490-133">원본 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-133">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="6e490-134">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="6e490-134">-SourceUri</span></span>
<span data-ttu-id="6e490-135">원본 Uri를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-135">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="6e490-136">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6e490-136">-StorageAccountId</span></span>
<span data-ttu-id="6e490-137">저장소 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-137">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="6e490-138">태그</span><span class="sxs-lookup"><span data-stu-id="6e490-138">-Tag</span></span>
<span data-ttu-id="6e490-139">리소스 및 리소스 그룹에 이름-값 쌍 집합을 태깅 할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-139">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

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

### <span data-ttu-id="6e490-140">-확인</span><span class="sxs-lookup"><span data-stu-id="6e490-140">-Confirm</span></span>
<span data-ttu-id="6e490-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e490-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e490-142">-WhatIf</span></span>
<span data-ttu-id="6e490-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e490-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e490-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e490-145">CommonParameters</span></span>
<span data-ttu-id="6e490-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e490-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e490-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e490-148">입력</span><span class="sxs-lookup"><span data-stu-id="6e490-148">INPUTS</span></span>

### <span data-ttu-id="6e490-149">시스템 Null 허용 ' 1 [[14.0.0.0]. StorageAccountTypes, Microsoft Azure. 관리., Version = 31bf3856ad364e35, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="6e490-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="6e490-150">시스템. Null 허용 `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[b77a5c561934e089, mscorlib, version = 4.0.0.0, culture = 중립, publickeytoken =]] system.webserver/Hashtable 시스템. Null 허용 `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[[시스템], 부울, Mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]] microsoft azure.</span><span class="sxs-lookup"><span data-stu-id="6e490-150">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="6e490-151">출력</span><span class="sxs-lookup"><span data-stu-id="6e490-151">OUTPUTS</span></span>

### <span data-ttu-id="6e490-152">SnapshotUpdate를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e490-152">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="6e490-153">상속자</span><span class="sxs-lookup"><span data-stu-id="6e490-153">NOTES</span></span>

## <span data-ttu-id="6e490-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e490-154">RELATED LINKS</span></span>


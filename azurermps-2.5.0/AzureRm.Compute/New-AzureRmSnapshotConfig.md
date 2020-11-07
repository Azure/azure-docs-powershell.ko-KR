---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshotconfig
schema: 2.0.0
ms.openlocfilehash: a18eb8513e419d174efac9179cb65fe175d12dd1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882689"
---
# <span data-ttu-id="3ee9c-101">New-AzureRmSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="3ee9c-101">New-AzureRmSnapshotConfig</span></span>

## <span data-ttu-id="3ee9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ee9c-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee9c-103">구성 가능한 스냅숏 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-103">Creates a configurable snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ee9c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3ee9c-104">SYNTAX</span></span>

```
New-AzureRmSnapshotConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ee9c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3ee9c-105">DESCRIPTION</span></span>
<span data-ttu-id="3ee9c-106">**AzureRmSnapshotConfig** cmdlet은 구성할 수 있는 스냅숏 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-106">The **New-AzureRmSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="3ee9c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3ee9c-107">EXAMPLES</span></span>

### <span data-ttu-id="3ee9c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3ee9c-108">Example 1</span></span>
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

<span data-ttu-id="3ee9c-109">첫 번째 명령은 Standard_LRS 저장소 계정 형식의 크기가 5GB 인 로컬 빈 스냅숏 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="3ee9c-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="3ee9c-111">두 번째 및 세 번째 명령은 snapshot 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="3ee9c-112">마지막 명령은 snapshot 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '에 이름이 ' Snapshot01 ' 인 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3ee9c-113">변수</span><span class="sxs-lookup"><span data-stu-id="3ee9c-113">PARAMETERS</span></span>

### <span data-ttu-id="3ee9c-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="3ee9c-114">-CreateOption</span></span>
<span data-ttu-id="3ee9c-115">이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만들거나, 빈 디스크를 만들거나, 기존 디스크를 연결 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: DiskCreateOption
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee9c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee9c-116">-DefaultProfile</span></span>
<span data-ttu-id="3ee9c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee9c-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3ee9c-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="3ee9c-119">스냅숏에 대 한 디스크 암호화 키 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="3ee9c-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="3ee9c-120">-DiskSizeGB</span></span>
<span data-ttu-id="3ee9c-121">디스크 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="3ee9c-122">-# Settingsenabled</span><span class="sxs-lookup"><span data-stu-id="3ee9c-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="3ee9c-123">암호화 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="3ee9c-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="3ee9c-124">-ImageReference</span></span>
<span data-ttu-id="3ee9c-125">스냅숏에 대 한 이미지 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-125">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="3ee9c-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3ee9c-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="3ee9c-127">스냅숏에 대 한 키 암호화 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="3ee9c-128">-위치</span><span class="sxs-lookup"><span data-stu-id="3ee9c-128">-Location</span></span>
<span data-ttu-id="3ee9c-129">위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-129">Specifies a location.</span></span>

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

### <span data-ttu-id="3ee9c-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="3ee9c-130">-OsType</span></span>
<span data-ttu-id="3ee9c-131">OS 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="3ee9c-132">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="3ee9c-132">-SkuName</span></span>
<span data-ttu-id="3ee9c-133">저장소 계정의 Sku 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-133">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee9c-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="3ee9c-134">-SourceResourceId</span></span>
<span data-ttu-id="3ee9c-135">원본 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="3ee9c-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="3ee9c-136">-SourceUri</span></span>
<span data-ttu-id="3ee9c-137">원본 Uri를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="3ee9c-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3ee9c-138">-StorageAccountId</span></span>
<span data-ttu-id="3ee9c-139">저장소 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="3ee9c-140">태그</span><span class="sxs-lookup"><span data-stu-id="3ee9c-140">-Tag</span></span>
<span data-ttu-id="3ee9c-141">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3ee9c-142">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="3ee9c-142">For example:</span></span>

<span data-ttu-id="3ee9c-143">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="3ee9c-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3ee9c-144">-확인</span><span class="sxs-lookup"><span data-stu-id="3ee9c-144">-Confirm</span></span>
<span data-ttu-id="3ee9c-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ee9c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ee9c-146">-WhatIf</span></span>
<span data-ttu-id="3ee9c-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ee9c-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ee9c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee9c-149">CommonParameters</span></span>
<span data-ttu-id="3ee9c-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee9c-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ee9c-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee9c-152">입력</span><span class="sxs-lookup"><span data-stu-id="3ee9c-152">INPUTS</span></span>

### <span data-ttu-id="3ee9c-153">않아야</span><span class="sxs-lookup"><span data-stu-id="3ee9c-153">None</span></span>
<span data-ttu-id="3ee9c-154">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ee9c-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ee9c-155">출력</span><span class="sxs-lookup"><span data-stu-id="3ee9c-155">OUTPUTS</span></span>

### <span data-ttu-id="3ee9c-156">Microsoft. a. a. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="3ee9c-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="3ee9c-157">상속자</span><span class="sxs-lookup"><span data-stu-id="3ee9c-157">NOTES</span></span>

## <span data-ttu-id="3ee9c-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ee9c-158">RELATED LINKS</span></span>


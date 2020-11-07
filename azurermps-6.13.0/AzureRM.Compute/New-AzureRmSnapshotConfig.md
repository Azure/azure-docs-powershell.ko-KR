---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmSnapshotConfig.md
ms.openlocfilehash: 2050536a39c8ebcd5a1269709d25af100cc251b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703002"
---
# <span data-ttu-id="79e20-101">New-AzureRmSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="79e20-101">New-AzureRmSnapshotConfig</span></span>

## <span data-ttu-id="79e20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79e20-102">SYNOPSIS</span></span>
<span data-ttu-id="79e20-103">구성 가능한 스냅숏 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-103">Creates a configurable snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79e20-104">구문과</span><span class="sxs-lookup"><span data-stu-id="79e20-104">SYNTAX</span></span>

```
New-AzureRmSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79e20-105">설명은</span><span class="sxs-lookup"><span data-stu-id="79e20-105">DESCRIPTION</span></span>
<span data-ttu-id="79e20-106">**AzureRmSnapshotConfig** cmdlet은 구성할 수 있는 스냅숏 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-106">The **New-AzureRmSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="79e20-107">예제의</span><span class="sxs-lookup"><span data-stu-id="79e20-107">EXAMPLES</span></span>

### <span data-ttu-id="79e20-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="79e20-108">Example 1</span></span>
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

<span data-ttu-id="79e20-109">첫 번째 명령은 Standard_LRS 저장소 계정 형식의 크기가 5GB 인 로컬 빈 스냅숏 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="79e20-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="79e20-111">두 번째 및 세 번째 명령은 snapshot 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="79e20-112">마지막 명령은 snapshot 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '에 이름이 ' Snapshot01 ' 인 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="79e20-113">변수</span><span class="sxs-lookup"><span data-stu-id="79e20-113">PARAMETERS</span></span>

### <span data-ttu-id="79e20-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="79e20-114">-CreateOption</span></span>
<span data-ttu-id="79e20-115">이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만들거나, 빈 디스크를 만들거나, 기존 디스크를 연결 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="79e20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79e20-116">-DefaultProfile</span></span>
<span data-ttu-id="79e20-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79e20-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="79e20-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="79e20-119">스냅숏에 대 한 디스크 암호화 키 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="79e20-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="79e20-120">-DiskSizeGB</span></span>
<span data-ttu-id="79e20-121">디스크 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="79e20-122">-# Settingsenabled</span><span class="sxs-lookup"><span data-stu-id="79e20-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="79e20-123">암호화 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="79e20-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="79e20-124">-ImageReference</span></span>
<span data-ttu-id="79e20-125">스냅숏에 대 한 이미지 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-125">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="79e20-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="79e20-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="79e20-127">스냅숏에 대 한 키 암호화 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="79e20-128">-위치</span><span class="sxs-lookup"><span data-stu-id="79e20-128">-Location</span></span>
<span data-ttu-id="79e20-129">위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-129">Specifies a location.</span></span>

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

### <span data-ttu-id="79e20-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="79e20-130">-OsType</span></span>
<span data-ttu-id="79e20-131">OS 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="79e20-132">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="79e20-132">-SkuName</span></span>
<span data-ttu-id="79e20-133">저장소 계정의 Sku 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="79e20-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="79e20-134">-SourceResourceId</span></span>
<span data-ttu-id="79e20-135">원본 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="79e20-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="79e20-136">-SourceUri</span></span>
<span data-ttu-id="79e20-137">원본 Uri를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="79e20-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="79e20-138">-StorageAccountId</span></span>
<span data-ttu-id="79e20-139">저장소 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="79e20-140">태그</span><span class="sxs-lookup"><span data-stu-id="79e20-140">-Tag</span></span>
<span data-ttu-id="79e20-141">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="79e20-142">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="79e20-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="79e20-143">-확인</span><span class="sxs-lookup"><span data-stu-id="79e20-143">-Confirm</span></span>
<span data-ttu-id="79e20-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79e20-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79e20-145">-WhatIf</span></span>
<span data-ttu-id="79e20-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79e20-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79e20-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79e20-148">CommonParameters</span></span>
<span data-ttu-id="79e20-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79e20-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79e20-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79e20-151">입력</span><span class="sxs-lookup"><span data-stu-id="79e20-151">INPUTS</span></span>

### <span data-ttu-id="79e20-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="79e20-152">System.String</span></span>

### <span data-ttu-id="79e20-153">시스템 Null 허용 ' 1 [[OperatingSystemTypes, Microsoft azure. 21.0.0.0, Version =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="79e20-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="79e20-154">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="79e20-154">System.Int32</span></span>

### <span data-ttu-id="79e20-155">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="79e20-155">System.Collections.Hashtable</span></span>

### <span data-ttu-id="79e20-156">Microsoft. 관리. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="79e20-156">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="79e20-157">시스템 Null 허용 ' 1 [[b77a5c561934e089] [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="79e20-157">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="79e20-158">KeyVaultAndSecretReference를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-158">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="79e20-159">KeyVaultAndKeyReference를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e20-159">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="79e20-160">출력</span><span class="sxs-lookup"><span data-stu-id="79e20-160">OUTPUTS</span></span>

### <span data-ttu-id="79e20-161">Microsoft. a. a. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="79e20-161">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="79e20-162">상속자</span><span class="sxs-lookup"><span data-stu-id="79e20-162">NOTES</span></span>

## <span data-ttu-id="79e20-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79e20-163">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: 82d7c1768b9e7f702b87a2bd23afcc76257b937f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969243"
---
# <span data-ttu-id="27c83-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="27c83-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="27c83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27c83-102">SYNOPSIS</span></span>
<span data-ttu-id="27c83-103">구성 가능한 스냅숏 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="27c83-104">구문</span><span class="sxs-lookup"><span data-stu-id="27c83-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DiskEncryptionSetId <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27c83-105">설명</span><span class="sxs-lookup"><span data-stu-id="27c83-105">DESCRIPTION</span></span>
<span data-ttu-id="27c83-106">**New-AzSnapshotUpdateConfig** cmdlet은 구성 가능한 스냅숏 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="27c83-107">예제</span><span class="sxs-lookup"><span data-stu-id="27c83-107">EXAMPLES</span></span>

### <span data-ttu-id="27c83-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="27c83-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="27c83-109">첫 번째 명령은 저장소 계정 유형에 크기가 10GB인 로컬 빈 스냅숏 Premium_LRS 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="27c83-110">또한 Windows OS 유형을 설정하고 암호화 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="27c83-111">두 번째 및 세 번째 명령은 스냅숏 업데이트 개체에 대한 디스크 암호화 키 및 키 암호화 키 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="27c83-112">마지막 명령은 스냅숏 업데이트 개체를 사용하여 리소스 그룹 'ResourceGroup01'에서 '스냅숏01'으로 기존 스냅숏을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="27c83-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="27c83-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="27c83-114">이 명령은 리소스 그룹 'ResourceGroup01'에서 이름 '스냅숏01'을 사용하여 기존 스냅숏을 10GB 디스크 크기로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="27c83-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="27c83-115">PARAMETERS</span></span>

### <span data-ttu-id="27c83-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27c83-116">-DefaultProfile</span></span>
<span data-ttu-id="27c83-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27c83-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="27c83-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="27c83-119">스냅숏에서 디스크 암호화 키 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="27c83-120">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="27c83-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="27c83-121">미사용 암호화를 사용하도록 설정하는 데 사용할 디스크 암호화 집합의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="27c83-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="27c83-122">-DiskSizeGB</span></span>
<span data-ttu-id="27c83-123">디스크 크기를 GB로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="27c83-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="27c83-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="27c83-125">암호화 설정을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="27c83-126">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="27c83-126">-EncryptionType</span></span>
<span data-ttu-id="27c83-127">디스크의 데이터를 암호화하는 데 사용되는 키 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-127">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="27c83-128">사용 가능한 값은 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'입니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-128">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="27c83-129">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="27c83-129">-KeyEncryptionKey</span></span>
<span data-ttu-id="27c83-130">스냅숏의 키 암호화 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-130">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="27c83-131">-OsType</span><span class="sxs-lookup"><span data-stu-id="27c83-131">-OsType</span></span>
<span data-ttu-id="27c83-132">OS 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-132">Specifies the OS type.</span></span>

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

### <span data-ttu-id="27c83-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="27c83-133">-SkuName</span></span>
<span data-ttu-id="27c83-134">저장소 계정의 Sku 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-134">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="27c83-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="27c83-135">-Tag</span></span>
<span data-ttu-id="27c83-136">해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="27c83-137">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="27c83-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="27c83-138">-확인</span><span class="sxs-lookup"><span data-stu-id="27c83-138">-Confirm</span></span>
<span data-ttu-id="27c83-139">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27c83-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27c83-140">-WhatIf</span></span>
<span data-ttu-id="27c83-141">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27c83-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27c83-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27c83-143">CommonParameters</span></span>
<span data-ttu-id="27c83-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="27c83-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27c83-145">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27c83-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27c83-146">입력</span><span class="sxs-lookup"><span data-stu-id="27c83-146">INPUTS</span></span>

### <span data-ttu-id="27c83-147">System.String</span><span class="sxs-lookup"><span data-stu-id="27c83-147">System.String</span></span>

### <span data-ttu-id="27c83-148">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="27c83-148">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="27c83-149">System.Int32</span><span class="sxs-lookup"><span data-stu-id="27c83-149">System.Int32</span></span>

### <span data-ttu-id="27c83-150">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="27c83-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="27c83-151">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="27c83-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="27c83-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="27c83-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="27c83-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="27c83-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="27c83-154">출력</span><span class="sxs-lookup"><span data-stu-id="27c83-154">OUTPUTS</span></span>

### <span data-ttu-id="27c83-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="27c83-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="27c83-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="27c83-156">NOTES</span></span>

## <span data-ttu-id="27c83-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27c83-157">RELATED LINKS</span></span>

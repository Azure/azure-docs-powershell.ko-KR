---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: 1a90a1ff260d143cf4df52ad160b4c05e781bd2e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056747"
---
# <span data-ttu-id="ab6b2-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="ab6b2-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="ab6b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab6b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ab6b2-103">구성 가능한 스냅숏 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="ab6b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab6b2-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DiskEncryptionSetId <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab6b2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ab6b2-105">DESCRIPTION</span></span>
<span data-ttu-id="ab6b2-106">**AzSnapshotUpdateConfig** cmdlet은 구성할 수 있는 스냅숏 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="ab6b2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ab6b2-107">EXAMPLES</span></span>

### <span data-ttu-id="ab6b2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ab6b2-108">Example 1</span></span>
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

<span data-ttu-id="ab6b2-109">첫 번째 명령은 Premium_LRS 저장소 계정 유형에 서 크기가 10GB 인 로컬 빈 스냅샷 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="ab6b2-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="ab6b2-111">두 번째 및 세 번째 명령은 스냅샷 업데이트 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="ab6b2-112">마지막 명령은 snapshot update 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '의 이름이 ' Snapshot01 ' 인 기존 스냅숏을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ab6b2-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="ab6b2-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="ab6b2-114">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 10gb 디스크 크기로 이름이 ' Snapshot01 ' 인 기존 스냅숏을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="ab6b2-115">변수</span><span class="sxs-lookup"><span data-stu-id="ab6b2-115">PARAMETERS</span></span>

### <span data-ttu-id="ab6b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab6b2-116">-DefaultProfile</span></span>
<span data-ttu-id="ab6b2-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab6b2-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ab6b2-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="ab6b2-119">스냅숏에 대 한 디스크 암호화 키 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="ab6b2-120">-Disk. Setid</span><span class="sxs-lookup"><span data-stu-id="ab6b2-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="ab6b2-121">나머지 암호화를 사용 하는 데 사용할 디스크 암호화 집합의 리소스 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="ab6b2-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="ab6b2-122">-DiskSizeGB</span></span>
<span data-ttu-id="ab6b2-123">디스크 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="ab6b2-124">-# Settingsenabled</span><span class="sxs-lookup"><span data-stu-id="ab6b2-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="ab6b2-125">암호화 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="ab6b2-126">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="ab6b2-126">-EncryptionType</span></span>
<span data-ttu-id="ab6b2-127">디스크의 데이터를 암호화 하는 데 사용 되는 키 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-127">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="ab6b2-128">사용 가능한 값은 ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '입니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-128">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="ab6b2-129">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ab6b2-129">-KeyEncryptionKey</span></span>
<span data-ttu-id="ab6b2-130">스냅숏에 대 한 키 암호화 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-130">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="ab6b2-131">-OsType</span><span class="sxs-lookup"><span data-stu-id="ab6b2-131">-OsType</span></span>
<span data-ttu-id="ab6b2-132">OS 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-132">Specifies the OS type.</span></span>

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

### <span data-ttu-id="ab6b2-133">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="ab6b2-133">-SkuName</span></span>
<span data-ttu-id="ab6b2-134">저장소 계정의 Sku 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-134">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="ab6b2-135">태그</span><span class="sxs-lookup"><span data-stu-id="ab6b2-135">-Tag</span></span>
<span data-ttu-id="ab6b2-136">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ab6b2-137">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ab6b2-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ab6b2-138">-확인</span><span class="sxs-lookup"><span data-stu-id="ab6b2-138">-Confirm</span></span>
<span data-ttu-id="ab6b2-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab6b2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab6b2-140">-WhatIf</span></span>
<span data-ttu-id="ab6b2-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab6b2-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab6b2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab6b2-143">CommonParameters</span></span>
<span data-ttu-id="ab6b2-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab6b2-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab6b2-146">입력</span><span class="sxs-lookup"><span data-stu-id="ab6b2-146">INPUTS</span></span>

### <span data-ttu-id="ab6b2-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ab6b2-147">System.String</span></span>

### <span data-ttu-id="ab6b2-148">시스템 Null 허용 ' 1 [[OperatingSystemTypes, Microsoft azure. 23.0.0.0, Version =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ab6b2-148">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ab6b2-149">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-149">System.Int32</span></span>

### <span data-ttu-id="ab6b2-150">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="ab6b2-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ab6b2-151">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ab6b2-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ab6b2-152">KeyVaultAndSecretReference를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="ab6b2-153">KeyVaultAndKeyReference를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="ab6b2-154">출력</span><span class="sxs-lookup"><span data-stu-id="ab6b2-154">OUTPUTS</span></span>

### <span data-ttu-id="ab6b2-155">PSSnapshotUpdate의. m a.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="ab6b2-156">상속자</span><span class="sxs-lookup"><span data-stu-id="ab6b2-156">NOTES</span></span>

## <span data-ttu-id="ab6b2-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab6b2-157">RELATED LINKS</span></span>

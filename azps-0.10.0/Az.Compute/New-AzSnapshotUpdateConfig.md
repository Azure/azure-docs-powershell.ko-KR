---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: c2c17fe3329170d65d61e5439e614717a8119f26
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877003"
---
# <span data-ttu-id="adc7b-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="adc7b-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="adc7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adc7b-102">SYNOPSIS</span></span>
<span data-ttu-id="adc7b-103">구성 가능한 스냅숏 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adc7b-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="adc7b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="adc7b-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adc7b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="adc7b-105">DESCRIPTION</span></span>
<span data-ttu-id="adc7b-106">**AzSnapshotUpdateConfig** cmdlet은 구성할 수 있는 스냅숏 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adc7b-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="adc7b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="adc7b-107">EXAMPLES</span></span>

### <span data-ttu-id="adc7b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="adc7b-108">Example 1</span></span>
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

<span data-ttu-id="adc7b-109">첫 번째 명령은 Premium_LRS 저장소 계정 유형에 서 크기가 10GB 인 로컬 빈 스냅샷 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adc7b-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="adc7b-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc7b-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="adc7b-111">두 번째 및 세 번째 명령은 스냅샷 업데이트 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc7b-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="adc7b-112">마지막 명령은 snapshot update 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '의 이름이 ' Snapshot01 ' 인 기존 스냅숏을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc7b-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="adc7b-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="adc7b-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="adc7b-114">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 10gb 디스크 크기로 이름이 ' Snapshot01 ' 인 기존 스냅숏을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc7b-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="adc7b-115">변수</span><span class="sxs-lookup"><span data-stu-id="adc7b-115">PARAMETERS</span></span>

### <span data-ttu-id="adc7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc7b-116">-DefaultProfile</span></span>
<span data-ttu-id="adc7b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="adc7b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adc7b-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="adc7b-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="adc7b-119">스냅숏에 대 한 디스크 암호화 키 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc7b-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="adc7b-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="adc7b-120">-DiskSizeGB</span></span>
<span data-ttu-id="adc7b-121">디스크 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc7b-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="adc7b-122">-# Settingsenabled</span><span class="sxs-lookup"><span data-stu-id="adc7b-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="adc7b-123">암호화 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc7b-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="adc7b-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="adc7b-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="adc7b-125">스냅숏에 대 한 키 암호화 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc7b-125">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="adc7b-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="adc7b-126">-OsType</span></span>
<span data-ttu-id="adc7b-127">OS 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc7b-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="adc7b-128">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="adc7b-128">-SkuName</span></span>
<span data-ttu-id="adc7b-129">저장소 계정의 Sku 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc7b-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="adc7b-130">태그</span><span class="sxs-lookup"><span data-stu-id="adc7b-130">-Tag</span></span>
<span data-ttu-id="adc7b-131">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="adc7b-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="adc7b-132">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="adc7b-132">For example:</span></span>

<span data-ttu-id="adc7b-133">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="adc7b-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="adc7b-134">-확인</span><span class="sxs-lookup"><span data-stu-id="adc7b-134">-Confirm</span></span>
<span data-ttu-id="adc7b-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc7b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adc7b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adc7b-136">-WhatIf</span></span>
<span data-ttu-id="adc7b-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="adc7b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="adc7b-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="adc7b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adc7b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc7b-139">CommonParameters</span></span>
<span data-ttu-id="adc7b-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc7b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc7b-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adc7b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc7b-142">입력</span><span class="sxs-lookup"><span data-stu-id="adc7b-142">INPUTS</span></span>

### <span data-ttu-id="adc7b-143">않아야</span><span class="sxs-lookup"><span data-stu-id="adc7b-143">None</span></span>
<span data-ttu-id="adc7b-144">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="adc7b-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="adc7b-145">출력</span><span class="sxs-lookup"><span data-stu-id="adc7b-145">OUTPUTS</span></span>

### <span data-ttu-id="adc7b-146">PSSnapshotUpdate의. m a.</span><span class="sxs-lookup"><span data-stu-id="adc7b-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="adc7b-147">상속자</span><span class="sxs-lookup"><span data-stu-id="adc7b-147">NOTES</span></span>

## <span data-ttu-id="adc7b-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="adc7b-148">RELATED LINKS</span></span>


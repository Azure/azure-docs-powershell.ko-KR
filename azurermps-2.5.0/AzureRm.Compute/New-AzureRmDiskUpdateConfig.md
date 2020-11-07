---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskupdateconfig
schema: 2.0.0
ms.openlocfilehash: 790d366ced8b9466a906df2d3f1717ad9277ca9f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882377"
---
# <span data-ttu-id="6008a-101">New-AzureRmDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="6008a-101">New-AzureRmDiskUpdateConfig</span></span>

## <span data-ttu-id="6008a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6008a-102">SYNOPSIS</span></span>
<span data-ttu-id="6008a-103">구성 가능한 디스크 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6008a-103">Creates a configurable disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6008a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6008a-104">SYNTAX</span></span>

```
New-AzureRmDiskUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6008a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6008a-105">DESCRIPTION</span></span>
<span data-ttu-id="6008a-106">**AzureRmDiskUpdateConfig** cmdlet은 구성 가능한 디스크 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6008a-106">The **New-AzureRmDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="6008a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6008a-107">EXAMPLES</span></span>

### <span data-ttu-id="6008a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6008a-108">Example 1</span></span>
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

<span data-ttu-id="6008a-109">첫 번째 명령은 Premium_LRS 저장소 계정 유형에 서 크기가 10GB 인 로컬 빈 디스크 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6008a-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="6008a-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6008a-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="6008a-111">두 번째 및 세 번째 명령은 디스크 업데이트 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6008a-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="6008a-112">마지막 명령은 disk update 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '의 이름이 ' Disk01 ' 인 기존 디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6008a-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="6008a-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="6008a-113">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="6008a-114">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 10gb 디스크 크기로 이름이 ' Disk01 ' 인 기존 디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6008a-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="6008a-115">변수</span><span class="sxs-lookup"><span data-stu-id="6008a-115">PARAMETERS</span></span>

### <span data-ttu-id="6008a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6008a-116">-DefaultProfile</span></span>
<span data-ttu-id="6008a-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6008a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6008a-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6008a-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="6008a-119">디스크의 디스크 암호화 키 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6008a-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="6008a-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="6008a-120">-DiskSizeGB</span></span>
<span data-ttu-id="6008a-121">디스크 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6008a-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="6008a-122">-# Settingsenabled</span><span class="sxs-lookup"><span data-stu-id="6008a-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="6008a-123">암호화 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6008a-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="6008a-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6008a-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="6008a-125">디스크의 키 암호화 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6008a-125">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="6008a-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="6008a-126">-OsType</span></span>
<span data-ttu-id="6008a-127">OS 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6008a-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="6008a-128">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="6008a-128">-SkuName</span></span>
<span data-ttu-id="6008a-129">저장소 계정의 Sku 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6008a-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="6008a-130">태그</span><span class="sxs-lookup"><span data-stu-id="6008a-130">-Tag</span></span>
<span data-ttu-id="6008a-131">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="6008a-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6008a-132">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="6008a-132">For example:</span></span>

<span data-ttu-id="6008a-133">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6008a-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6008a-134">-확인</span><span class="sxs-lookup"><span data-stu-id="6008a-134">-Confirm</span></span>
<span data-ttu-id="6008a-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6008a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6008a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6008a-136">-WhatIf</span></span>
<span data-ttu-id="6008a-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6008a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6008a-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6008a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6008a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6008a-139">CommonParameters</span></span>
<span data-ttu-id="6008a-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6008a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6008a-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6008a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6008a-142">입력</span><span class="sxs-lookup"><span data-stu-id="6008a-142">INPUTS</span></span>

### <span data-ttu-id="6008a-143">않아야</span><span class="sxs-lookup"><span data-stu-id="6008a-143">None</span></span>
<span data-ttu-id="6008a-144">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6008a-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6008a-145">출력</span><span class="sxs-lookup"><span data-stu-id="6008a-145">OUTPUTS</span></span>

### <span data-ttu-id="6008a-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="6008a-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="6008a-147">상속자</span><span class="sxs-lookup"><span data-stu-id="6008a-147">NOTES</span></span>

## <span data-ttu-id="6008a-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6008a-148">RELATED LINKS</span></span>


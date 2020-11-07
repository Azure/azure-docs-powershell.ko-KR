---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermdisk
schema: 2.0.0
ms.openlocfilehash: 06cd8d41fcdaaed6a05f7f7a137cbf75542be62b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883098"
---
# <span data-ttu-id="3c7c9-101">Update-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="3c7c9-101">Update-AzureRmDisk</span></span>

## <span data-ttu-id="3c7c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c7c9-102">SYNOPSIS</span></span>
<span data-ttu-id="3c7c9-103">디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c9-103">Updates a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c7c9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3c7c9-104">SYNTAX</span></span>

### <span data-ttu-id="3c7c9-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="3c7c9-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c7c9-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="3c7c9-106">FriendMethod</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c7c9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3c7c9-107">DESCRIPTION</span></span>
<span data-ttu-id="3c7c9-108">**업데이트 AzureRmDisk** cmdlet은 디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c9-108">The **Update-AzureRmDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="3c7c9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3c7c9-109">EXAMPLES</span></span>

### <span data-ttu-id="3c7c9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3c7c9-110">Example 1</span></span>
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

<span data-ttu-id="3c7c9-111">첫 번째 명령은 Premium_LRS 저장소 계정 유형에 서 크기가 10GB 인 로컬 빈 디스크 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c9-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="3c7c9-112">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c9-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="3c7c9-113">두 번째 및 세 번째 명령은 디스크 업데이트 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c9-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="3c7c9-114">마지막 명령은 disk update 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '의 이름이 ' Disk01 ' 인 기존 디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c9-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="3c7c9-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="3c7c9-115">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="3c7c9-116">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 10gb 디스크 크기로 이름이 ' Disk01 ' 인 기존 디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c9-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="3c7c9-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="3c7c9-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="3c7c9-118">또한이 명령은 리소스 그룹 ' ResourceGroup01 '에서 10gb 디스크 크기로 이름이 ' Disk01 ' 인 기존 디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c9-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="3c7c9-119">변수</span><span class="sxs-lookup"><span data-stu-id="3c7c9-119">PARAMETERS</span></span>

### <span data-ttu-id="3c7c9-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c7c9-120">-AsJob</span></span>
<span data-ttu-id="3c7c9-121">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c9-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c7c9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c7c9-122">-DefaultProfile</span></span>
<span data-ttu-id="3c7c9-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c7c9-124">-디스크</span><span class="sxs-lookup"><span data-stu-id="3c7c9-124">-Disk</span></span>
<span data-ttu-id="3c7c9-125">로컬 디스크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c9-125">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7c9-126">-DiskName</span><span class="sxs-lookup"><span data-stu-id="3c7c9-126">-DiskName</span></span>
<span data-ttu-id="3c7c9-127">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c9-127">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7c9-128">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="3c7c9-128">-DiskUpdate</span></span>
<span data-ttu-id="3c7c9-129">로컬 디스크 업데이트 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c9-129">Specifies a local disk update object.</span></span>

```yaml
Type: PSDiskUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7c9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c7c9-130">-ResourceGroupName</span></span>
<span data-ttu-id="3c7c9-131">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c9-131">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7c9-132">-확인</span><span class="sxs-lookup"><span data-stu-id="3c7c9-132">-Confirm</span></span>
<span data-ttu-id="3c7c9-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c7c9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c7c9-134">-WhatIf</span></span>
<span data-ttu-id="3c7c9-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c7c9-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c7c9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c7c9-137">CommonParameters</span></span>
<span data-ttu-id="3c7c9-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c7c9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c7c9-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c7c9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c7c9-140">입력</span><span class="sxs-lookup"><span data-stu-id="3c7c9-140">INPUTS</span></span>

### <span data-ttu-id="3c7c9-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3c7c9-141">System.String</span></span>
<span data-ttu-id="3c7c9-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="3c7c9-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="3c7c9-143">출력</span><span class="sxs-lookup"><span data-stu-id="3c7c9-143">OUTPUTS</span></span>

### <span data-ttu-id="3c7c9-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="3c7c9-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="3c7c9-145">상속자</span><span class="sxs-lookup"><span data-stu-id="3c7c9-145">NOTES</span></span>

## <span data-ttu-id="3c7c9-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c7c9-146">RELATED LINKS</span></span>


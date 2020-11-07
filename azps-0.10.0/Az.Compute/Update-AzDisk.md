---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzDisk.md
ms.openlocfilehash: 8925e294b329b76f996a21d24597a4a8b5388a74
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875986"
---
# <span data-ttu-id="0de74-101">Update-AzDisk</span><span class="sxs-lookup"><span data-stu-id="0de74-101">Update-AzDisk</span></span>

## <span data-ttu-id="0de74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0de74-102">SYNOPSIS</span></span>
<span data-ttu-id="0de74-103">디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0de74-103">Updates a disk.</span></span>

## <span data-ttu-id="0de74-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0de74-104">SYNTAX</span></span>

### <span data-ttu-id="0de74-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="0de74-105">DefaultParameter (Default)</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0de74-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="0de74-106">FriendMethod</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0de74-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0de74-107">DESCRIPTION</span></span>
<span data-ttu-id="0de74-108">**업데이트 AzDisk** cmdlet은 디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0de74-108">The **Update-AzDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="0de74-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0de74-109">EXAMPLES</span></span>

### <span data-ttu-id="0de74-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0de74-110">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="0de74-111">첫 번째 명령은 Premium_LRS 저장소 계정 유형에 서 크기가 10GB 인 로컬 빈 디스크 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0de74-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="0de74-112">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0de74-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="0de74-113">두 번째 및 세 번째 명령은 디스크 업데이트 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0de74-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="0de74-114">마지막 명령은 disk update 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '의 이름이 ' Disk01 ' 인 기존 디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0de74-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="0de74-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="0de74-115">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="0de74-116">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 10gb 디스크 크기로 이름이 ' Disk01 ' 인 기존 디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0de74-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="0de74-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="0de74-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="0de74-118">또한이 명령은 리소스 그룹 ' ResourceGroup01 '에서 10gb 디스크 크기로 이름이 ' Disk01 ' 인 기존 디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0de74-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="0de74-119">변수</span><span class="sxs-lookup"><span data-stu-id="0de74-119">PARAMETERS</span></span>

### <span data-ttu-id="0de74-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0de74-120">-AsJob</span></span>
<span data-ttu-id="0de74-121">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="0de74-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0de74-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0de74-122">-DefaultProfile</span></span>
<span data-ttu-id="0de74-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0de74-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0de74-124">-디스크</span><span class="sxs-lookup"><span data-stu-id="0de74-124">-Disk</span></span>
<span data-ttu-id="0de74-125">로컬 디스크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0de74-125">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="0de74-126">-DiskName</span><span class="sxs-lookup"><span data-stu-id="0de74-126">-DiskName</span></span>
<span data-ttu-id="0de74-127">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0de74-127">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="0de74-128">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="0de74-128">-DiskUpdate</span></span>
<span data-ttu-id="0de74-129">로컬 디스크 업데이트 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0de74-129">Specifies a local disk update object.</span></span>

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

### <span data-ttu-id="0de74-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0de74-130">-ResourceGroupName</span></span>
<span data-ttu-id="0de74-131">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0de74-131">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0de74-132">-확인</span><span class="sxs-lookup"><span data-stu-id="0de74-132">-Confirm</span></span>
<span data-ttu-id="0de74-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0de74-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0de74-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0de74-134">-WhatIf</span></span>
<span data-ttu-id="0de74-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0de74-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0de74-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0de74-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0de74-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0de74-137">CommonParameters</span></span>
<span data-ttu-id="0de74-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0de74-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0de74-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0de74-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0de74-140">입력</span><span class="sxs-lookup"><span data-stu-id="0de74-140">INPUTS</span></span>

### <span data-ttu-id="0de74-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0de74-141">System.String</span></span>
<span data-ttu-id="0de74-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="0de74-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="0de74-143">출력</span><span class="sxs-lookup"><span data-stu-id="0de74-143">OUTPUTS</span></span>

### <span data-ttu-id="0de74-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="0de74-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="0de74-145">상속자</span><span class="sxs-lookup"><span data-stu-id="0de74-145">NOTES</span></span>

## <span data-ttu-id="0de74-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0de74-146">RELATED LINKS</span></span>


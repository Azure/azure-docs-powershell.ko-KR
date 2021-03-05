---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
ms.openlocfilehash: c8ab3583fed5c65468bccf5282b5fae44a4a5c20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009787"
---
# <span data-ttu-id="9c610-101">Update-AzDisk</span><span class="sxs-lookup"><span data-stu-id="9c610-101">Update-AzDisk</span></span>

## <span data-ttu-id="9c610-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c610-102">SYNOPSIS</span></span>
<span data-ttu-id="9c610-103">디스크를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9c610-103">Updates a disk.</span></span>

## <span data-ttu-id="9c610-104">구문</span><span class="sxs-lookup"><span data-stu-id="9c610-104">SYNTAX</span></span>

### <span data-ttu-id="9c610-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="9c610-105">DefaultParameter (Default)</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c610-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="9c610-106">FriendMethod</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c610-107">설명</span><span class="sxs-lookup"><span data-stu-id="9c610-107">DESCRIPTION</span></span>
<span data-ttu-id="9c610-108">**Update-AzDisk** cmdlet은 디스크를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9c610-108">The **Update-AzDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="9c610-109">예제</span><span class="sxs-lookup"><span data-stu-id="9c610-109">EXAMPLES</span></span>

### <span data-ttu-id="9c610-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9c610-110">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="9c610-111">첫 번째 명령은 저장소 계정 유형에 크기가 10GB인 로컬 빈 디스크 Premium_LRS 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9c610-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="9c610-112">또한 Windows OS 유형을 설정하고 암호화 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c610-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="9c610-113">두 번째 및 세 번째 명령은 디스크 업데이트 개체에 대한 디스크 암호화 키 및 키 암호화 키 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c610-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="9c610-114">마지막 명령은 디스크 업데이트 개체를 사용하며 리소스 그룹 'ResourceGroup01'에서 'Disk01'으로 기존 디스크를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9c610-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="9c610-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="9c610-115">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="9c610-116">이 명령은 리소스 그룹 'ResourceGroup01'의 이름 'Disk01'을 사용하여 기존 디스크를 10GB 디스크 크기로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9c610-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="9c610-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="9c610-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="9c610-118">또한 이러한 명령은 리소스 그룹 'ResourceGroup01'의 이름 'Disk01'을 사용하여 기존 디스크를 10GB 디스크 크기로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9c610-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="9c610-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9c610-119">PARAMETERS</span></span>

### <span data-ttu-id="9c610-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c610-120">-AsJob</span></span>
<span data-ttu-id="9c610-121">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="9c610-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c610-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c610-122">-DefaultProfile</span></span>
<span data-ttu-id="9c610-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9c610-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c610-124">-Disk</span><span class="sxs-lookup"><span data-stu-id="9c610-124">-Disk</span></span>
<span data-ttu-id="9c610-125">로컬 디스크 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c610-125">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c610-126">-DiskName</span><span class="sxs-lookup"><span data-stu-id="9c610-126">-DiskName</span></span>
<span data-ttu-id="9c610-127">디스크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c610-127">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c610-128">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="9c610-128">-DiskUpdate</span></span>
<span data-ttu-id="9c610-129">로컬 디스크 업데이트 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c610-129">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c610-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c610-130">-ResourceGroupName</span></span>
<span data-ttu-id="9c610-131">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c610-131">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c610-132">-확인</span><span class="sxs-lookup"><span data-stu-id="9c610-132">-Confirm</span></span>
<span data-ttu-id="9c610-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9c610-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c610-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c610-134">-WhatIf</span></span>
<span data-ttu-id="9c610-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9c610-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c610-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9c610-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c610-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c610-137">CommonParameters</span></span>
<span data-ttu-id="9c610-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9c610-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c610-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c610-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c610-140">입력</span><span class="sxs-lookup"><span data-stu-id="9c610-140">INPUTS</span></span>

### <span data-ttu-id="9c610-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9c610-141">System.String</span></span>

### <span data-ttu-id="9c610-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="9c610-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="9c610-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="9c610-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="9c610-144">출력</span><span class="sxs-lookup"><span data-stu-id="9c610-144">OUTPUTS</span></span>

### <span data-ttu-id="9c610-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="9c610-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="9c610-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9c610-146">NOTES</span></span>

## <span data-ttu-id="9c610-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c610-147">RELATED LINKS</span></span>

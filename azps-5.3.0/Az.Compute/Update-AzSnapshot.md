---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
ms.openlocfilehash: 6cfe2fd958d74740195b0bb29d3defa34f1310a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493785"
---
# <span data-ttu-id="b02d8-101">Update-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="b02d8-101">Update-AzSnapshot</span></span>

## <span data-ttu-id="b02d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b02d8-102">SYNOPSIS</span></span>
<span data-ttu-id="b02d8-103">스냅숏을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b02d8-103">Updates a snapshot.</span></span>

## <span data-ttu-id="b02d8-104">구문</span><span class="sxs-lookup"><span data-stu-id="b02d8-104">SYNTAX</span></span>

### <span data-ttu-id="b02d8-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="b02d8-105">DefaultParameter (Default)</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-SnapshotUpdate] <PSSnapshotUpdate>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b02d8-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="b02d8-106">FriendMethod</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b02d8-107">설명</span><span class="sxs-lookup"><span data-stu-id="b02d8-107">DESCRIPTION</span></span>
<span data-ttu-id="b02d8-108">**Update-AzSnapshot** cmdlet은 스냅숏을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b02d8-108">The **Update-AzSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="b02d8-109">예제</span><span class="sxs-lookup"><span data-stu-id="b02d8-109">EXAMPLES</span></span>

### <span data-ttu-id="b02d8-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b02d8-110">Example 1</span></span>
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

<span data-ttu-id="b02d8-111">첫 번째 명령은 저장소 계정 유형에서 크기가 10GB인 로컬 빈 스냅숏 Premium_LRS 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b02d8-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="b02d8-112">또한 Windows OS 유형을 설정하고 암호화 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b02d8-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="b02d8-113">두 번째 및 세 번째 명령은 스냅숏 업데이트 개체에 대한 디스크 암호화 키 및 키 암호화 키 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b02d8-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="b02d8-114">마지막 명령은 스냅숏 업데이트 개체를 생성하고 리소스 그룹 'ResourceGroup01'에서 'Snapshot01'으로 기존 스냅숏을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b02d8-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="b02d8-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="b02d8-115">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="b02d8-116">이 명령은 리소스 그룹 'ResourceGroup01'에서 이름이 'Snapshot01'인 기존 스냅숏을 10GB 디스크 크기로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b02d8-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="b02d8-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="b02d8-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="b02d8-118">또한 이러한 명령은 리소스 그룹 'ResourceGroup01'에서 이름이 'Snapshot01'인 기존 스냅숏을 10GB 디스크 크기로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b02d8-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="b02d8-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b02d8-119">PARAMETERS</span></span>

### <span data-ttu-id="b02d8-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b02d8-120">-AsJob</span></span>
<span data-ttu-id="b02d8-121">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="b02d8-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b02d8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b02d8-122">-DefaultProfile</span></span>
<span data-ttu-id="b02d8-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b02d8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b02d8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b02d8-124">-ResourceGroupName</span></span>
<span data-ttu-id="b02d8-125">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b02d8-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b02d8-126">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="b02d8-126">-Snapshot</span></span>
<span data-ttu-id="b02d8-127">로컬 스냅숏 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b02d8-127">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b02d8-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="b02d8-128">-SnapshotName</span></span>
<span data-ttu-id="b02d8-129">스냅숏의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b02d8-129">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="b02d8-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="b02d8-130">-SnapshotUpdate</span></span>
<span data-ttu-id="b02d8-131">로컬 스냅숏 업데이트 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b02d8-131">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b02d8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b02d8-132">-Confirm</span></span>
<span data-ttu-id="b02d8-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b02d8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b02d8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b02d8-134">-WhatIf</span></span>
<span data-ttu-id="b02d8-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b02d8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b02d8-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b02d8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b02d8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b02d8-137">CommonParameters</span></span>
<span data-ttu-id="b02d8-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b02d8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b02d8-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b02d8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b02d8-140">입력</span><span class="sxs-lookup"><span data-stu-id="b02d8-140">INPUTS</span></span>

### <span data-ttu-id="b02d8-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b02d8-141">System.String</span></span>

### <span data-ttu-id="b02d8-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="b02d8-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="b02d8-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="b02d8-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="b02d8-144">출력</span><span class="sxs-lookup"><span data-stu-id="b02d8-144">OUTPUTS</span></span>

### <span data-ttu-id="b02d8-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="b02d8-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="b02d8-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b02d8-146">NOTES</span></span>

## <span data-ttu-id="b02d8-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b02d8-147">RELATED LINKS</span></span>

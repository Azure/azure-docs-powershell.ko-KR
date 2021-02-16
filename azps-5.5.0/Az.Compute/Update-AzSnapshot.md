---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
ms.openlocfilehash: 6cfe2fd958d74740195b0bb29d3defa34f1310a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177396"
---
# <span data-ttu-id="78865-101">Update-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="78865-101">Update-AzSnapshot</span></span>

## <span data-ttu-id="78865-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78865-102">SYNOPSIS</span></span>
<span data-ttu-id="78865-103">스냅숏을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="78865-103">Updates a snapshot.</span></span>

## <span data-ttu-id="78865-104">구문</span><span class="sxs-lookup"><span data-stu-id="78865-104">SYNTAX</span></span>

### <span data-ttu-id="78865-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="78865-105">DefaultParameter (Default)</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-SnapshotUpdate] <PSSnapshotUpdate>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78865-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="78865-106">FriendMethod</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78865-107">설명</span><span class="sxs-lookup"><span data-stu-id="78865-107">DESCRIPTION</span></span>
<span data-ttu-id="78865-108">**Update-AzSnapshot** cmdlet은 스냅숏을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="78865-108">The **Update-AzSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="78865-109">예제</span><span class="sxs-lookup"><span data-stu-id="78865-109">EXAMPLES</span></span>

### <span data-ttu-id="78865-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="78865-110">Example 1</span></span>
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

<span data-ttu-id="78865-111">첫 번째 명령은 저장소 계정 유형에서 크기가 10GB인 로컬 빈 스냅숏 Premium_LRS 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78865-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="78865-112">또한 Windows OS 유형을 설정하고 암호화 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78865-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="78865-113">두 번째 및 세 번째 명령은 스냅숏 업데이트 개체에 대한 디스크 암호화 키 및 키 암호화 키 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78865-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="78865-114">마지막 명령은 스냅숏 업데이트 개체를 생성하고 리소스 그룹 'ResourceGroup01'에서 'Snapshot01'으로 기존 스냅숏을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="78865-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="78865-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="78865-115">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="78865-116">이 명령은 리소스 그룹 'ResourceGroup01'에서 이름이 'Snapshot01'인 기존 스냅숏을 10GB 디스크 크기로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="78865-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="78865-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="78865-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="78865-118">또한 이러한 명령은 리소스 그룹 'ResourceGroup01'에서 이름이 'Snapshot01'인 기존 스냅숏을 10GB 디스크 크기로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="78865-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="78865-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78865-119">PARAMETERS</span></span>

### <span data-ttu-id="78865-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78865-120">-AsJob</span></span>
<span data-ttu-id="78865-121">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="78865-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="78865-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78865-122">-DefaultProfile</span></span>
<span data-ttu-id="78865-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78865-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78865-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78865-124">-ResourceGroupName</span></span>
<span data-ttu-id="78865-125">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78865-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="78865-126">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="78865-126">-Snapshot</span></span>
<span data-ttu-id="78865-127">로컬 스냅숏 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78865-127">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="78865-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="78865-128">-SnapshotName</span></span>
<span data-ttu-id="78865-129">스냅숏의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78865-129">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="78865-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="78865-130">-SnapshotUpdate</span></span>
<span data-ttu-id="78865-131">로컬 스냅숏 업데이트 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78865-131">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="78865-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78865-132">-Confirm</span></span>
<span data-ttu-id="78865-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="78865-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78865-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78865-134">-WhatIf</span></span>
<span data-ttu-id="78865-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="78865-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78865-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78865-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78865-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78865-137">CommonParameters</span></span>
<span data-ttu-id="78865-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="78865-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78865-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="78865-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78865-140">입력</span><span class="sxs-lookup"><span data-stu-id="78865-140">INPUTS</span></span>

### <span data-ttu-id="78865-141">System.String</span><span class="sxs-lookup"><span data-stu-id="78865-141">System.String</span></span>

### <span data-ttu-id="78865-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="78865-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="78865-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="78865-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="78865-144">출력</span><span class="sxs-lookup"><span data-stu-id="78865-144">OUTPUTS</span></span>

### <span data-ttu-id="78865-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="78865-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="78865-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="78865-146">NOTES</span></span>

## <span data-ttu-id="78865-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78865-147">RELATED LINKS</span></span>

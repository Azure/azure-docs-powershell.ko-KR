---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
ms.openlocfilehash: 6cfe2fd958d74740195b0bb29d3defa34f1310a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042563"
---
# <span data-ttu-id="8d2bb-101">Update-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="8d2bb-101">Update-AzSnapshot</span></span>

## <span data-ttu-id="8d2bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d2bb-102">SYNOPSIS</span></span>
<span data-ttu-id="8d2bb-103">스냅숏을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-103">Updates a snapshot.</span></span>

## <span data-ttu-id="8d2bb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d2bb-104">SYNTAX</span></span>

### <span data-ttu-id="8d2bb-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="8d2bb-105">DefaultParameter (Default)</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-SnapshotUpdate] <PSSnapshotUpdate>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d2bb-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="8d2bb-106">FriendMethod</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d2bb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8d2bb-107">DESCRIPTION</span></span>
<span data-ttu-id="8d2bb-108">**업데이트 AzSnapshot** cmdlet은 스냅숏을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-108">The **Update-AzSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="8d2bb-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8d2bb-109">EXAMPLES</span></span>

### <span data-ttu-id="8d2bb-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="8d2bb-110">Example 1</span></span>
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

<span data-ttu-id="8d2bb-111">첫 번째 명령은 Premium_LRS 저장소 계정 유형에 서 크기가 10GB 인 로컬 빈 스냅샷 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="8d2bb-112">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="8d2bb-113">두 번째 및 세 번째 명령은 스냅샷 업데이트 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="8d2bb-114">마지막 명령은 snapshot update 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '의 이름이 ' Snapshot01 ' 인 기존 스냅숏을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="8d2bb-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="8d2bb-115">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="8d2bb-116">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 10gb 디스크 크기로 이름이 ' Snapshot01 ' 인 기존 스냅숏을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="8d2bb-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="8d2bb-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="8d2bb-118">또한이 명령은 리소스 그룹 ' ResourceGroup01 '에서 10gb 디스크 크기로 이름이 ' Snapshot01 ' 인 기존 스냅샷을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="8d2bb-119">변수</span><span class="sxs-lookup"><span data-stu-id="8d2bb-119">PARAMETERS</span></span>

### <span data-ttu-id="8d2bb-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d2bb-120">-AsJob</span></span>
<span data-ttu-id="8d2bb-121">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8d2bb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d2bb-122">-DefaultProfile</span></span>
<span data-ttu-id="8d2bb-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d2bb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d2bb-124">-ResourceGroupName</span></span>
<span data-ttu-id="8d2bb-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8d2bb-126">-스냅숏</span><span class="sxs-lookup"><span data-stu-id="8d2bb-126">-Snapshot</span></span>
<span data-ttu-id="8d2bb-127">로컬 스냅숏 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-127">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="8d2bb-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="8d2bb-128">-SnapshotName</span></span>
<span data-ttu-id="8d2bb-129">스냅숏의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-129">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="8d2bb-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="8d2bb-130">-SnapshotUpdate</span></span>
<span data-ttu-id="8d2bb-131">로컬 스냅숏 업데이트 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-131">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="8d2bb-132">-확인</span><span class="sxs-lookup"><span data-stu-id="8d2bb-132">-Confirm</span></span>
<span data-ttu-id="8d2bb-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d2bb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d2bb-134">-WhatIf</span></span>
<span data-ttu-id="8d2bb-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d2bb-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d2bb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d2bb-137">CommonParameters</span></span>
<span data-ttu-id="8d2bb-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d2bb-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d2bb-140">입력</span><span class="sxs-lookup"><span data-stu-id="8d2bb-140">INPUTS</span></span>

### <span data-ttu-id="8d2bb-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8d2bb-141">System.String</span></span>

### <span data-ttu-id="8d2bb-142">PSSnapshotUpdate의. m a.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="8d2bb-143">Microsoft. a. a. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="8d2bb-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="8d2bb-144">출력</span><span class="sxs-lookup"><span data-stu-id="8d2bb-144">OUTPUTS</span></span>

### <span data-ttu-id="8d2bb-145">Microsoft. a. a. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="8d2bb-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="8d2bb-146">상속자</span><span class="sxs-lookup"><span data-stu-id="8d2bb-146">NOTES</span></span>

## <span data-ttu-id="8d2bb-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d2bb-147">RELATED LINKS</span></span>
